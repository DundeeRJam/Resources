<link rel="stylesheet" type="text/css" href="C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/mystyle.css">

# How to Setup Your Raspberry pi

## Introduction

### Project
Setting up your Raspberry pi

### Description
Within this worksheet you will get shown how to set up your raspberry pi. All the raspberry pi's we have here are pi 2's and use Micro SD cards.

## Equipment required
For this worksheet you will require:
* A Raspberry Pi 
* A Micro SD Card (8gb recommended)
* Monitor and Cable that will connect to the HDMI output of your pi (most of the monitors here are DVI)
* A Keyboard and mouse
* A raspberry pi power supply

## Setting up your Pi
Get your Raspberry Pi.
* Plug in the Micro SD card With either a copy of the Raspbian Operating system on it. (if you are doing this at home and have noobs on the SD card refer to our NOOBS install guide)
* Plug in the keyboard and mouse in to the USB ports.
* Plug in the power supply.

When your raspberry pi is all wired up it should look like the picture below.
# ADD IMAGE HERE OF WIRED UP PI

After the raspberry pi has finished booting up, you will see either the Graphical User Interface, or the Command Line Interface (the image below on the left is the graphical and one on the right is the command line).

If you find that your Raspberry Pi has booted into the Command Line Interface, you should change the settings to boot to the Graphical user interface. To do this type the following into the raspberry pi 
```bash
sudo raspi-config
```
The config tool will show.
# INSERT CONFIG TOOL MENU HERE
Use the down arrow to move the cursor down to Boot Options, and press Enter. Choose the option B4 Desktop Autologin and press Enter.
# INSERT IMAGE HERE WITH OPTION HIGHLIGHTED
use the right arrow on the keyboard to finish and exit the tool. The next time your pi reboots it will be in the Graphical User Interface.

## Updating Raspbian
Its a good idea to keep your raspberry pi up to date with latest bug fixes and improvments (this can only be done when the pi is connected to the internet). This can take up to an hour to complete, so do it when you have time.

To update your pi open a terminal window and type the following commands (pressing enter after each line)
```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
```
## Identifying the version of Raspbian
To find what version of Raspbian your raspberry pi is running type the following into the terminal
```bash
lsb_release -a
```

#### You can now successfully set up a Raspberry Pi