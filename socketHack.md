---
layout: default
title: Hacking Bluetooth Socket Instructions
nav_order: 11
---

# Instructions for hacking into the (optional) Bluetooth plug

## This is not instructions on how to connect the Bluetooth sockets into Home Assisant.

## This section assumes you're a tech wizard of some level, and that you have the ASC Bluetooth plug (which is optional when you made your purchase). If you have a Bluetooth device scanner then you can skip to the bottom to look at the possible commands.

- If you don't have a Bluetooth scanner, download "nRF Connect" by Nordic Semiconductor for your Windows, Android, or Apple device.

<img src="images/BLEhack_1_nrfApp.jpg" width="600">

- Plug in a socket (make sure it's flashing blue and not paired to anything), and use the "nRF Connect" app to scan for bluetooth devices.

- Find the Bluetooth device that starts with "TramTek" and connect to it.

<img src="images/BLEhack_2_scan.jpg" width="600">

- Tap on the "Unknown Service", and the up-arrow on the "Unknown Characteristic" that has the "NOTIFY, WRITE" properties.

<img src="images/BLEhack_3_send.jpg" width="600">

- Pick "TEXT (UTF-8)" from the drop down, and then send any one of these commands:

<img src="images/BLEhack_4_command.jpg" width="600">

## THE POSSIBLE COMMANDS YOU CAN SEND TO THE BLUETOOTH SOCKET:
All commands are UTF-8 text, ignore the 
**"1,0" - On, infinite time**
**"0,0" - Off, infinite time**
**"1,x" - On, then a timer of x milliseconds (e.g. 1,5000 for On command sent immediately, then wait 5s, then turn off)**
**"0,x" - Off, then a timer of x milliseconds (e.g. 0,5000 for Off command sent immediately, then wait 5s, then turn on)**

**The UUID Service #: 4faf01c2-1b91-45e9-8fcc-c59cc333914b**
**The UUID characteristic #: af01c21b-9145-e98f-c5cc-9cc31c913a8b**




These steps will revert the mat back to its original programming so it can be used with a TrampleTek Blue socket.

- First, click this [link to directly download](https://github.com/ASCKing9/TrampleTek-Blue-code/raw/refs/heads/main/TrampleTekBlueToothSocket.bin) the TrampleTekBlueToothSocket.bin from the Github [TrampleTek-Blue-code repo](https://github.com/ASCKing9/TrampleTek-Blue-code). It will go to whatever your default download folder is.

- Next, we will need to download the Espressif Flash Download Tools from [here](https://www.espressif.com/en/support/download/other-tools). Find the Flash Download Tools line and click on the download arrow.

<img src="images/Reflash_1_DownloadESPTool.png" width="600">

(This is what the page looked like 9/20/24)

- After it downloads, extract the compressed (zipped) folder by right-clicking on the file and picking extract (or unzip on some computers).

<img src="images/Reflash_2_UnzipESPTool.png" width="600">

- Your window may look different, but in the end extract the files to what ever folder you want.

<img src="images/Reflash_3_UnzipESPTool.png" width="600">

- Open your newly extracted folder and open the file named "flash_download_tool_3.9.7" (the number may change in future updates, but it should still be called "flash_download_tool_(numbers)").

<img src="images/Reflash_4_UnzipESPTool.png" width="600">

-	After it opens you'll need to pick the following: (1) ChipType - ESP32-C3, (2) WorkMode - Develop, and (3) LoadMode - USB.
-	Click "OK"

<img src="images/Reflash_5_PickESP32.png" width="600">   

- That will open this window, frequently I need to expand the window to see the bottom area options.

<img src="images/Reflash_6_Expand.png" width="600">  

- Click on the three dots on the top line of the long white boxes.

<img src="images/Reflash_7_dots.png" width="600">  

- This will open a file selector window, navigate to where you downloaded the [TrampleTekBlueToothSocket.bin](https://github.com/ASCKing9/TrampleTek-Blue-code/raw/refs/heads/main/TrampleTekBlueToothSocket.bin) from the first step, and click open.

<img src="images/Reflash_8_dataIn1.png" width="600">  

- Now click the check box on the left and type "0x0" into the box on the right. The box areas should turn green once you've done this.

<img src="images/Reflash_8_dataIn2.png" width="600">

- Now you need to pick your COM port, if you haven't connected your mat to your computer using the USB cable, do so now.
- If you don't know which COM port is the right one, unplug the mat and open the COM port drop down menu and take note of the COM ports. Then, click away (to close the COM port drop down menu), plug in your mat, and re-open the COM port drop down menu. Check to see if any new COM port numbers have shown up. If yes, that's the mat's COM port, select it.

<img src="images/Reflash_9_ComPort.png" width="600"> 

- Press the "Start" button.

<img src="images/Reflash_10_start.png" width="600">  

- If everything is working right you'll see this progress bar start moving after a few seconds.

<img src="images/Reflash_11_progress.png" width="600"> 

- When it's finished you've succesfully uploaded the original TrampleTek Blue code!

<img src="images/Reflash_12_done.png" width="600">

## Now unplug and re-plug in the mat and you'll see the blue light start flashing, this indicates that it's searching for a nearby TrampleTek Blue socket to pair with! Plug in your original TrampleTek Blue socket nearby and you're all ready to go.

## Go [here](https://github.com/ASCKing9/TrampleTek-Blue-code/blob/main/TrampleTekBlue_socketVerison/TrampleTek%20Instructions%20Brochure%20reduced%20color.pdf) for the original TrampleTek Blue instruction manual.

