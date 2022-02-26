# RaspberryPi LED Matrix Display

## Setup

In my case I'm using a Raspberry Pi 3B+ with the "Adafruit RBG Matrix Bonnet" and the "Quality" Option with GPIO4 and GPIO18 connected.
In my tests this gives me the best quality.
The Matrix Display itself is a 64x64 one. After a little try and error I got the connection with the display right.
Be advised - in my case I cannot use the standard wire because the Bonnet needs a different orientation of 2 wires.

## Installation

In order to install/connect everything the correct way you have to use this guide:
https://learn.adafruit.com/adafruit-rgb-matrix-plus-real-time-clock-hat-for-raspberry-pi/driving-matrices

As stated in the documentation you can use these commands to install all necessary packages on the raspberry pi:

```
curl https://raw.githubusercontent.com/adafruit/Raspberry-Pi-Installer-Scripts/master/rgb-matrix.sh >rgb-matrix.sh
sudo bash rgb-matrix.sh
```

After setup a test of the matrix can be done with the example code:

```
./samples/rotating-block-generator.py --led-rows=64 --led-cols=64 --led-slowdown-gpio=1
```

Use the slowdown command in order to stop a flickering of the display. 
