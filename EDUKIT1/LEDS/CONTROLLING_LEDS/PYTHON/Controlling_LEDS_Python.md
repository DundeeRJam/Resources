<link rel="stylesheet" type="text/css" href="C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/mystyle.css">

# Controlling LED's with Python

## Introduction
Within this worksheet you are going to learn how to connect and control LEDs with a Raspberry Pi through python code.

## Equipment We Will Be Using
To complete this worksheet you will require:
* A Raspberry Pi with all cables
* A Electronic Breadboard
* 1 x Red LED
* 1 x Yellow LED
* 1 x Green LED
* 3 x 330 ohms Resistors
* 4 x Male to Female jumper wires

## Creating The Circuit
Before you create the circuit make sure the Raspberry Pi is turned off.
To create the circuit follow the diagram below:
**NOTE** LEDs Have one longer leg called the anode which is always connected to the positive supply of the circuit. The shorter leg called the cathode is connected to the negative side of the power supply. The resistors go in between the short leg and ground rail on a breadboard.

![LED Diagram](https://github.com/DundeeRJam/Resources/blob/master/Images/LED_Diagram.png)

Now plug the power supply in to turn the Raspberry pi on.

## Code
Your Raspberry Pi should now be booted up. Go to Menu -> Programming and click on the IDLE3 Python editor. To create a new file, go to File -> New File. Now type the following code:

**NOTE** Anything typed after a '#' is a comment in Python. Programmers use this to tell people reading the code (including themselves!) what is going on.
```python
from gpiozero import LED

red = LED(18) # this is saying the red LED is connected to pin 18 on the raspberry pi
yellow = LED(23) # this is saying the yellow LED is connected to pin 23 on the raspberry pi
green = LED(24) # this is saying the green LED is connected to pin 24 on the raspberry pi

red.on() # this is turning the red LED on
yellow.on() # this is turning the yellow LED on
green.on() # this is turning the green LED on
```

Once you have typed all of the code above, and checked to make sure it is right, save the file and call it LED_on.py

## Running The Code
You are now ready to run the code. You can do this by clicking on Run -> Run Module or by pressing F5 on your keyboard. You should now see your LEDs light up.

## Challenge
You have managed to turn the LEDs on. Now try and turn them off. Save your code in a seperate file.
