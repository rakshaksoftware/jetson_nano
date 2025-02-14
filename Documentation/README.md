**Nvidia Jetpack Version 4.6.1, Python Version 3.6**

**Connecting Jetson Nano to Ubuntu**

1. Install Screen to Bash
2. Connect Jetson to your laptop using MicroUSB cable
3. sudo screen /dev/ttyACM0 or screen /dev/ttyACM1

**Connecting to Network**

1. Identify WiFi networks using the command: nmcli dev wifi list
2. Enter the command, sudo nmcli dev wifi connect SSID password "PASSWORD", in Jetson, replace SSID with Network name and "PASSWORD" with the Network password

**Installation of TensorRT**

TensorRT is required to run ONNX models on Jetson Nano.
Run the following commands in the terminal to install it.

`$ sudo apt update`

`$ sudo apt install nvidia-tensorrt`

**Connecting using SSH**  
Connect to Jetson using screen command and get it's IP address using ifconfig command.  
IP address is the **inet** code under 'wlan0'  
Connect your laptop to same network as Jetson's and run the command 
`ssh rakshak@<ip address>` 
in your terminal.

**Jetson Resources**
Jetson Support: https://developer.nvidia.com/embedded/community/support-resources  
Jetson Nano wiki: https://elinux.org/Jetson_Nano  
Script to get MAC Address of Jetson Nano: https://gist.github.com/dusty-nv/e4314241677cf38f40d556931d0c4a38  
Jetson Easy setup configurator: https://github.com/rbonghi/jetson_easy  
jetson-stats is a powerful tool to analyze your board: https://github.com/rbonghi/jetson_stats  

**Projects**
https://developer.nvidia.com/embedded/community/jetson-projects/hello_ai_world
