
# LED ARGB control by FPGA

This project is a control ARGB leds such as WS2812b. I gonna leave the documentation how this works.


## Hardware

- myRIO 1900
- ARGB of 100 leds
- Resistor 250 ohm
- Power supply KPS305D

## Software

- Labview 2021 32 bits
- Labview FPGA
- Labview RT
## How the ARGB led works


This led has 6 pins.

Voltage 12V in/out
Data in/out
Ground in/out

![How is this led](https://cdn.sparkfun.com/assets/2/3/0/d/3/51f04880ce395f714a000000.png)

"12V" - The input voltage will can vary based on the IC version's specifications:
WS2812 -- This should be a regulated supply voltage between 5V and about 7V. More than that could harm the LED, less than 5V will either reduce brightness, or it just won't turn on.
WS2812B -- This should be a regulated supply voltage 12V.
GND -- The common, ground, 0V reference supply voltage.
DI -- Data from a microcontroller (or another WS2812/WS2812B pixel) comes into this pin.
DO -- Data is shifted out of this pin, to be connected to the input of another pixel or left floating if it is the last link in the chain.

![Signal](https://cdn.sparkfun.com/assets/b/a/2/9/c/51f04d33ce395f687c000001.png)

Timing diagram for a single bit of value 0 or 1.

The data is sent in a sequence containing 24 of those bits -- 8 bits for each color -- followed by a low "reset" pulse of at least 50µs.

Data bit order
A sequence of 24 timed-bits sets the color for each channel. 8-bits per channel. Green first, then red, then blue.

![data](https://cdn.sparkfun.com/assets/8/4/8/6/7/51f04dd6ce395f3843000000.png)





![App Screenshot](https://dummyimage.com/468x300?text=App+Screenshot+Here)


## Authors

- [@javierlopez](https://github.com/Javixl1/myRIOledstrip/tree/main)

