<link rel="stylesheet" type="text/css" href="C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/mystyle.css">

# User Interaction

## Introduction
Within this worksheet we are going to control the red, yellow or the green LEDs depending on the choice that the user makes. 

## Equipment Required
To complete this worksheet you will require:
* A Raspberry Pi with all cables
* A Electronic Breadboard
* 1 x Red LED
* 1 x Yellow LED
* 1 x Green LED
* 3 x 330 ohms Resistors
* 4 x Male to Female jumper wires
* 1 x Piece of hookup wire

## Creating The Circuit
Before you create the circuit make sure the Raspberry Pi is turned off.
To create the circuit follow the diagram below:
**NOTE** LEDs Have one longer leg called the anode which is always connected to the positive supply of the circuit. The shorter leg called the cathode is connected to the negative side of the power supply. The resistors go in between the short leg and ground rail on a breadboard.

![](https://github.com/DundeeRJam/Resources/blob/master/Images/LEDs.png)
![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/LEDs.png)

Now plug the power supply in to turn the Raspberry pi on.

## Code
If you have done the previous worksheets you will see that we are using the same circuit, but this time the LEDs are going to be controlled by user input.

Within this worksheet you will get introduced to user input and variables which will store information that will be used in later code.

Your Raspberry Pi should now be booted up. Go to Menu -> Programming and click on the IDLE3 Python editor. To create a new file, go to File -> New File. Now type the following code:

**NOTE** Anything typed after a '#' is a comment in Python. Programmers use this to tell people reading the code (including themselves!) what is going on.

```python
from gpiozero import LED
from time import sleep
import os

red = LED(18) # this is saying the red LED is connected to pin 18 on the raspberry pi
yellow = LED(23) # this is saying the yellow LED is connected to pin 23 on the raspberry pi
green = LED(24) # this is saying the green LED is connected to pin 24 on the raspberry pi

os.system('clear') # Clears the screen

print ("Which LED would you like to blink")
print ("1: Red?")
print ("2: Yellow?")

# Prints prompts to the screen and waits for input from the user
led_choice = input ("Choose your option: ")
count = input ("How many times would you like it to blink? ")

# Convert user input from string (text) to integer (number)
led_choice = int(led_choice)
count = int(count)

# Set the LEDChoice variable depending on the led_choice
if led_choice == 1:
    print ("You picked the Red LED")
    LEDChoice = red
if led_choice == 2:
    print ("You have picked the Yellow LED")
    LEDChoice = yellow

# if we have chosen a valid choice, flash the LED 
if LEDChoice>0:
    while count > 0:
    LEDChoice.on()
    sleep (1)
    LEDChoice.off()
    sleep(1)
    count = count -1
```

Once you have typed all of the code above, and checked to make sure it is right, save the file and call it user_input.py

## Running The Code
You are now ready to run the code. You can do this by clicking on Run -> Run Module or by pressing F5 on your keyboard. You should now see your red LED blink.

The screen will clear and you will be prompted for which LED you would like to turn on and off. Enter 1 or 2.
You will then be prompted for how many times you want the LEDs to flash. The LED you chose will then flash the number of times you requested.
 
