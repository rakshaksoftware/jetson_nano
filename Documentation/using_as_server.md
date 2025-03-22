[VNC setup on personal network](https://developer.nvidia.com/embedded/learn/tutorials/vnc-setup)  

**Setup VNC server on the Jetson developer kit**
1. Enable the VNC server to start each time you log in
If you have a Jetson Nano 2GB Developer Kit (running LXDE)  

        mkdir -p ~/.config/autostart  
        cp /usr/share/applications/vino-server.desktop ~/.config/autostart/.
 
    For all other Jetson developer kits (running GNOME)

        cd /usr/lib/systemd/user/graphical-session.target.wants
        sudo ln -s ../vino-server.service ./.

1. Configure the VNC server
   
        gsettings set org.gnome.Vino prompt-enabled false
        gsettings set org.gnome.Vino require-encryption false

2. Set a password to access the VNC server

        Replace thepassword with your desired password
        gsettings set org.gnome.Vino authentication-methods "['vnc']"
        gsettings set org.gnome.Vino vnc-password $(echo -n 'thepassword'|base64)

3. Reboot the system so that the settings take effect

        sudo reboot

The VNC server is only available after you have logged in to Jetson locally. If you wish VNC to be available automatically, use the system settings application on your developer kit to enable automatic login.