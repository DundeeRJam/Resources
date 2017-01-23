<link rel="stylesheet" type="text/css" href="C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/mystyle.css">

# How to Setup Your Raspberry Pi

## **Introduction**
**Project** - Setting up your Raspberry Pi

**Description** - Within this worksheet you will get shown how to setup your Raspberry Pi. All the Raspberry Pi's we have here are Pi 2's and use Micro SD cards.

## **Equipment Required**
For this worksheet you will require:
* A Raspberry Pi
* A Micro SD card (8gb or higher recommended)
* Monitor and cable that will connect to the HDMI output of your Pi (most of the monitors here are DVI)
* Keyboard and Mouse
* A Raspberry Pi power supply

## **Setting Up Your Pi**
Get your Raspberry Pi.
* Plug in the Micro SD card with either a copy of the Raspbian Operating System on it (if you are doing this at home and have NOOBS installed on the SD card refer to our NOOBS install guide).
* Plug in the Keyboard and Mouse into the USB ports.
* Plug in the monitor cable into the HDMI port.
* Plug the power supply in.

When your raspberry pi is all wired up it should look like the picture below.
<br>
![Pi Diagram](https://github.com/DundeeRJam/Resources/blob/First-draft/Images/pi.jpg)
<br>
After the Raspberry Pi has finished booting up, you will see either the Graphical User Interface or Command Line Interface ( the image below on the right is the Graphical inteface and the one on the right is the Command Line).
<br>
![GUI/CLI](C:/Users/kez/Documents/GitHub/DundeeRJam/Resources/Images/GUI_CLI.png)
<br>
If you find that your Raspberry Pi has booted into the Command Line Interface, it is recommended that you change to the Graphical User interface. To do this type the following command into the Raspberry Pi:
```bash
sudo raspi-config
```

The config tool will show:
# Insert image of config tool here
Use the down arrow to move the cursor down to Boot Options, and press Enter. Choose option B4 Desktop Autologin and press Enter.
# Insert image here with option highlighted
Use the right arrow on the keyboard to Finish and Exit the tool. The next time you reboot your Raspberry Pi it will boot into the Graphical User Interface.

## **Updating Raspbian**
Its always a good idea to keep your Raspberry Pi up to date with the latest bug fixes and improvements (this can only be done when your Raspberry Pi is connected to the internet). Updating your Pi can take up to an hour to complete so only do it when you have time. 

To update your Pi open a Terminal window and type the following commands (pressing Enter after every line).

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
```
## **Identifying Your Version of Raspbian**
To find what version of Raspbian that you are using type the following command into the Terminal:
```bash
lsb_release -a
```
### **You can now successfully set up a Raspberry Pi!**
