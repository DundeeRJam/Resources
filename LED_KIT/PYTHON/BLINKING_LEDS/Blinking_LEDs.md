# Making LEDs Blink

## Introduction
Within this worksheet you will learn how to make LEDs blink using a Raspberry Pi and Python.

## Equipment We Will Be using
To complete this worksheet you will require:
* A Raspberry Pi with all cables
* An Electronic Breadboard
* 1 x Red LED
* 1 x Yellow LED
* 1 x Green LED
* 3 x 330 ohms Resistors
* 4 x Male to Female jumper wires
* 2 x Piece of hook-up wire

## Creating The Circuit
Before you create the circuit make sure the Raspberry Pi is turned off.
To create the circuit follow the diagram below:
**NOTE** LEDs Have one longer leg called the anode which is always connected to the positive supply of the circuit. The shorter leg called the cathode is connected to the negative side of the power supply. The resistors go in between the short leg and ground rail on a breadboard.

<img src = "Images/LEDs.png" width = "300px" height = "300px" />

Now plug the power supply in to turn the Raspberry pi on.

## Lets Get Coding!
Your Raspberry Pi should now be booted up. Go to Menu -> Programming and click on the IDLE3 Python editor. To create a new file, go to File -> New File. Now type the following code:

**NOTE** Anything typed after a '#' is a comment in Python. Programmers use this to tell people reading the code (including themselves!) what is going on.

```python
from gpiozero import LED
from time import sleep

red = LED(18) # this is saying the red LED is connected to pin 18 on the raspberry pi
yellow = LED(23) # this is saying the yellow LED is connected to pin 23 on the raspberry pi
green = LED(24) # this is saying the green LED is connected to pin 24 on the raspberry pi

# LEDs On
red.on() # this is turning the red LED on

sleep(1) # Pause for 1 Second

# LEDs Off
red.off() # this is turning the red LED off

sleep(1) # Pause for 1 Second

# LEDs On
red.on() # this is turning the red LED on

sleep(1) # Pause for 1 Second

# LEDs Off
red.off() # this is turning the red LED off
```

Once you have typed all of the code above, and checked to make sure it is right, save the file and call it Blinking_LEDs.py

## Running The Code
You are now ready to run the code. You can do this by clicking on Run -> Run Module or by pressing F5 on your keyboard. You should now see your red LED blink.

## Challenge 1
You have managed to make the red LED blink. Now try and make the yellow and green ones blink too. Save your code and run it like before.

<div class="page-break"></div>

## Making LEDs Blink Forever
```python
from gpiozero import LED
from time import sleep

red = LED(18) # this is saying the red LED is connected to pin 18 on the raspberry pi
yellow = LED(23) # this is saying the yellow LED is connected to pin 23 on the raspberry pi
green = LED(24) # this is saying the green LED is connected to pin 24 on the raspberry pi

while True:
    # LEDs On
    red.on() # this is turning the red LED on

    sleep(1) # Pause for 1 Second

    # LEDs Off
    red.off() # this is turning the red LED off

    sleep(1) # Pause for 1 Second
```

Now save your code as Blinking_LEDs_Forever.py and run the code as before.

You should now see the red LED blinking forever. To stop this press Ctrl+c.

## Challenge 2
You have made the red LED blink forever now do the same for the yellow and green LEDs. Save your code and run as before. You should now see all three LEDs blink on and off forever.
