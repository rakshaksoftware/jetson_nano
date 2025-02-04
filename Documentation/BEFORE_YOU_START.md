> This is because Jetson Nano comes with Python2 as default and if we try to install Python3 and run Python3 dependent programs on the same environment, it results in incompatibilities. Therefore, we had to use Docker Containers to create a separate environment where only Python3 was available in order to resolve the conflict.  
>[Source](https://dev.to/sushantnair/heres-how-i-achieved-faster-code-runs-for-running-docker-containers-in-jetson-nano-l4t-2d05)  

