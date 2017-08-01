## OctoPrint-PanTilt-Script
Command line script that can be used with the OctoPrint [OctoPrint-PanTilt Plugin](https://github.com/Salandora/OctoPrint-PanTilt)
on the Raspberry Pi.
This script uses the [pigpio](http://abyz.co.uk/rpi/pigpio) command line interface to drive a pan/tilt servo gimbal.
The pigpio daemon must be downloaded, installed and started.


### Installation
Follow one of the download and install methods found here: http://abyz.co.uk/rpi/pigpio/download.html

Example:
```
wget abyz.co.uk/rpi/pigpio/pigpio.zip
unzip pigpio.zip
cd PIGPIO
make
sudo make install
```

The pigpio daemon needs to be started:
```
sudo pigpiod
```
The script will not work without the daemon running, so if the system is rebooted, it will need to be
started again manually, or, added as a service.

Example of service setup: https://github.com/joan2937/pigpio/tree/master/util

Copy the script *servopwm* to /home/pi/scripts or some other location on the Raspberry Pi.

Edit the file to configure the pins used for pan/tilt if needed.

Update the PanTilt plugin to point to your script.

Done.