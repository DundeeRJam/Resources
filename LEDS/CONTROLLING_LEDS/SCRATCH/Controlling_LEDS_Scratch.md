<link rel="stylesheet" type="text/css" href="C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/mystyle.css">

# Controlling LED's with Scratch

## Introduction
Within this worksheet you are going to learn how to connect and control LED's with a Raspberry Pi through scratch code.

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
Before you create the circuit make sure the raspberry pi is turned off. To create the circuit follow the diagram below:
**NOTE** LED's Have one longer leg called the annode which is always connected to the positive supply of the circuit and The shorter leg called the cathode which is connected to the negative side of the power supply. The resistors go in between the short leg and ground rail on a breadboard.

![LED Diagram](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/LED_Diagram.png)

Now plug the power supply in to turn the Raspberry pi on.

## Code
Your Raspberry Pi should now be booted up. Go to menu -> programming and click on Scratch. Now drag and drop the folowing blocks to crate your code:

![LED_on code](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/LED_on.png)

## What The Blocks Do
Code Block                                                                              | Meaning
-----------|-------------------------------------------------------------------------------------------------------------------------------
![Green Flag](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/Green_Flag.png) | When the green flag is clicked the code will run
![GPIO Server on](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/GPIO_Server.png) | Turning the GPIO Server on so that scratch can communicate with the GPIO Pins
![pin 18 out](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/18_Out.png) | Configuring pin 18 as an output
![pin 23 out](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/23_out.png) | Configuring pin 23 as an output
![pin 24 out](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/24_out.png) | Configuring pin 24 as an output
![pin 18 on](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/18_on.png) | Giving pin 18 power and turning the red LED on
![pin 23 on](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/23_on.png) | Giving pin 23 power and turning the yellow LED on
![pin 24 on](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/24_on.png) | Giving pin 24 power and turning the green LED on

**NOTE** To edit the code of the broadcast blocks click on the little black arrow and pick *new/edit* abnd type the text into the dialog box and press enter.

Once you have copied the code above and checked to make sure it is right. Save the file and call it LED_on

## Running The Code
You are now ready to run the code. You can do this by clicking on the green flag. You should now see your LED's light up.

## Challenge
You have managed to turn the LED's on. Now try and turn them off. Save your code in a seperate file.