# Controlling LEDs

## Introduction
Within this worksheet you are going to learn how to connect and control LEDs with a Raspberry Pi through scratch code.

## Equipment We Will Be Using
To complete this worksheet you will require:
* A Raspberry Pi with all cables
* A Electronic Breadboard
* 1 x Red LED
* 1 x Yellow LED
* 1 x Green LED
* 3 x 330 ohms Resistors
* 4 x Male to Female jumper wires
* 2 x Pieces of hook-up wire

## Creating The Circuit
Before you create the circuit make sure the raspberry pi is turned off. To create the circuit follow the diagram below:
**NOTE** LEDs Have one longer leg called the anode which is always connected to the positive supply of the circuit. The shorter leg called the cathode which is connected to the negative side of the power supply. The resistors go in between the short leg and ground rail on a breadboard.

<img src = "Images/LEDs.png" width = "300px" height = "300px" />
<img src = "Images/Pin_numbers.png" width = "300px" height = "100px" />

Now plug the power supply in to turn the Raspberry pi on.

<div class="page-break"></div>

## Code
Your Raspberry Pi should now be booted up. Go to Menu -> Programming and click on Scratch. Now drag and drop the following blocks to crate your code:

<img src = "Images/LED_on.png" width = "300px" height = "350px" />

## What The Blocks Do
<table style = "width:100%" >
  <tr>
    <th> Code Block </th>
    <th> Meaning </th>
  </tr>
  <tr>
    <td> <img src = "Images/Green_Flag.png" width = "150px" height = "40px" /> </td>
    <td> When the green flag is clicked the code will run </td>
  </tr>
  <tr>
    <td> <img src = "Images/GPIO_Server.png" width = "150px" height = "40px" /> </td>
    <td> Turning the GPIO Server on so that scratch can communicate with the GPIO Pins </td>
  </tr>
  <tr>
    <td> <img src = "Images/18_out.png" width = "150px" height = "40px" /> </td>
    <td>  Configuring pin 18 as an output </td>
  </tr>
  <tr>
    <td> <img src = "Images/23_out.png" width = "150px" height = "40px" /> </td>
    <td> Configuring pin 23 as an output </td>
  </tr>
  <tr>
    <td> <img src = "Images/24_out.png" width = "150px" height = "40px" /> </td>
    <td> Configuring pin 24 as an output </td>
  </tr>
  <tr>
    <td> <img src = "Images/18_on.png" width = "150px" height = "40px" /> </td>
    <td> Giving pin 18 power and turning the red LED on </td>
  </tr>
  <tr>
    <td> <img src = "Images/23_on.png" width = "150px" height = "40px" /> </td>
    <td> Giving pin 23 power and turning the yellow LED on </td>
  </tr>
  <tr>
    <td> <img src = "Images/24_on.png" width = "150px" height = "40px" /> </td>
    <td> Giving pin 24 power and turning the green LED on </td>
  </tr>
</table>

**NOTE** To edit the code of the broadcast blocks click on the little black arrow and pick *new/edit* and type the text into the dialog box and press enter.

Once you have copied the code above and checked to make sure it is right. Save the file and call it LED_on

## Running The Code
You are now ready to run the code. You can do this by clicking on the green flag. You should now see your LEDs light up.

## Challenge
You have managed to turn the LEDs on. Now try and turn them off. Save your code in a separate file.
