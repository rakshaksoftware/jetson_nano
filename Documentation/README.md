**Nvidia Jetpack Version 4.6.1, Python Version 3.6**

**Connecting Jetson Nano to Ubuntu**

1. Install Screen to Bash
2. Connect Jetson to your laptop using MicroUSB cable
3. sudo screen/dev/ttyACM0 or screen/dev/ttyACM1

**Connecting to Network**

1. Identify WiFi networks using the command: nmcli dev wifi list
2. Enter the command, sudo nmcli dev wifi connect SSID password "PASSWORD", in Jetson, replace SSID with Network name and "PASSWORD" with the Network password

**Installation of TensorRT**

TensorRT is required to run ONNX models on Jetson Nano.
Run the following commands in the terminal to install it.

`$ sudo apt update`

`$ sudo apt install nvidia-tensorrt`
