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
**NOTE:** LEDs Have one longer leg called the anode which is always connected to the positive supply of the circuit. The shorter leg called the cathode is connected to the negative side of the power supply. The resistors go in between the short leg and ground rail on a breadboard.

![](https://github.com/DundeeRJam/Resources/blob/master/Images/LEDs.png)
![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/LEDs.png)

Now plug the power supply in to turn the Raspberry pi on.

## Creating User Interface
Before we write our code this time we need to develop an interface to pick which LED we would like to blink.

First thing we need to do is open Scratch. To do this Go to Menu -> Programming and click on Scratch.

1. **Delete Felix (the Cat)**. To do this right click on sprite 1 and click on Delete.
2. **Create a sprite for our question**. To do this click on the paintbrush Icon next to New Sprite. Then click on the "T" for creating text, type What LED would you like to blink?
3. **Create a Red square**. To do this click on the paintbrush Icon again and click on the black rectangle. Now click on the paint tin icon and pick the clour red, then click in the rectangle to make it Red. You can also add the text "Red" to your square too.
4. **Create a Yellow square**. Do this exactly the same as the Red square except fill it with a yellow colour.

Your interface should look something like this:

![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/User_Interaction.png)

## Creating The Code
### **Configuring GPIO**
To configure scratch to talk to the GPIO pins double click on the stage icon and add the following code:

![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/User_Interaction_Code1.png)

### **What The Blocks Do**
Code Block                                                                                    | Meaning
----------------------------------------------------------------------------------------------|-----------------------------------------
![](https://github.com/DundeeRJam/Resources/blob/master/Images/Green_Flag.png) ![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/Green_Flag.png)      | When the green flag is clicked the code will run
![](https://github.com/DundeeRJam/Resources/blob/master/Images/GPIO_Server.png)![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/GPIO_Server.png) | Turning the GPIO Server on so that scratch can communicate with the GPIO Pins
![](https://github.com/DundeeRJam/Resources/blob/master/Images/18_out.png)![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/18_out.png)          | Configuring pin 18 as an output
![](https://github.com/DundeeRJam/Resources/blob/master/Images/23_out.png)![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/23_out.png)          | Configuring pin 23 as an output
![](https://github.com/DundeeRJam/Resources/blob/master/Images/24_out.png)![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/24_out.png)          | Configuring pin 24 as an output

### **Configuring The Red LED**
Double click on the Red sprite block and add this code:

![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/User_Interaction_Code2.png)

### **What The Blocks Do**
Code Block                                                  | Meaning
------------------------------------------------------------|------------------------------------------------------------------------------------------------------------
![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/Sprite_Clicked.png)| When this sprite is clicked do te code that follows
![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/Ask_Wait.png)| This allows you to ask a question and wait for a response
![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/Repeat.png) | This block makes the code inside it repeat a given number of times
![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/Answer.png) | This stores the answer to a question. When attached to the repeat block the code will run that many times
![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/18_on.png) | Giving pin 18 power and turning the red LED on
![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/Wait.png) | This makes the program pause for 1 second
![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/18_off.png) | Taking power away from pin 18 and turning the red LED off

### **Configuring The Yellow LED**
Double click on the Yellow sprite and add this code:

![](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/User_Interaction_Code3.png)

All the code for the Yellow sprite is the same as the Red Sprite apart from it is turning pin 23 on and off instead of pin 18.

**NOTE:** To edit the code of the broadcast blocks click on the little black arrow and pick *new/edit* and type the text into the dialog box and press enter.

Once you have copied the code above and checked to make sure it is right. Save the file and call it User_Interaction.

## Running The Code
You are now ready to run the code. You can do this by clicking on the green flag. You should now see your chosen LED blink on and off for as many times as you asked it.

## Challenge
Now you have got the Red and Yellow LEDs working. Add a green block and code to make this work for the green LED.
