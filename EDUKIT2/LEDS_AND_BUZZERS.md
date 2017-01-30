<link rel="stylesheet" type="text/css" href="C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/mystyle.css">

# Controlling LED's and A Buzzer

## Introduction
Within this worksheet you will learn how to connect and control LED's and a buzzer using a raspberry pi and Python.

## Equipment Required
* A Raspberry pi
* A Breadboard
* 1 x Red LED
* 1 x Blue LED
* 1 x Buzzer
* 1 x Male to Male jumper wie
* 4 x Male to Female Jumper Wires
* 2 x 330 ohms Resistors

## Building The Circuit
Before you create the circuit make sure the raspberry pi is turned off. To create the circuit follow the diagram below:

**NOTE** LED's Have one longer leg called the annode is always connected to the positive supply of the circuit. The shorter leg called the cathode is connected to the negative side of the power supply. The resistors go in between the short leg and ground rail on a breadboard.

![LED Buzzer Diagram](https://github.com/DundeeRJam/Resources/blob/master/Images/LED_Buzzer_Diagram.png)

You can now turn on your raspberry pi.

## Code
Now that the raspberry pi is booted up, go to menu -> programming -> IDLE3 python editor. Create a new file by going to file -> new file. Type the following code:

``` python
from gpiozero import LED, Buzzer

# configuring the LEDs and Buzzer to pins of raspberry pi
Red = LED (18)
Blue = LED (24)
Buzz = Buzzer (22)

# Turning on LED's and sound
Red.on()
Blue.on()
Buzz.on()
```

**NOTE:** Anything starting with a "#" is a comment in python, so you don't have to type them.

## Running The Code
You are now ready to run the code to do this click on -> Run -> Run module or press F5 on the keyboard.

## Challenge
You know how to turn the LEDs and buzzer on. Now edit the code to turn them off.
