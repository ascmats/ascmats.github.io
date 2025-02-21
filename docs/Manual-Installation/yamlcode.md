---
layout: default
title: YAML Code Installation
parent: Manual Installation
nav_order: 2
---

# Instructions for installing the YAML code onto the TrampleTek mat

- At this point you have the is mat registered with Home Assistant(!) and it may prompt you that a new device was discovered. If you add the device now it won’t do anything, as it doesn’t have any ability to trigger any of your devices, that’s what the YAML code does. 

-	You can close your open ESPHome Web browser tab for now and get back to the ESPHome Open Web UI. (Main Home Assistant page -> settings-> add-on -> ESPHome -> Open Web UI). You may need to wait or refresh this screen a few times until your device shows up as “Online”

<img src="../../images/ESPHome_mat_online.png" width="600"> 

-	Click on “EDIT” to add your Wi-Fi settings and the firmware to run the mat!

<img src="../../images/ESPHome_mat_edit.png" width="600"> 

-	This will open up the YAML code for your mat, and you should see something like this (I’m not worried about showing sensitive details here because I’ll be remaking this device with different values in the future):

<img src="../../images/ESPHome_mat_yaml.png" width="600"> 

## Go to the [TrampleTek Blue YAML](https://github.com/ASCKing9/TrampleTek-Blue-code/blob/main/TrampleTek_ESPHome.yaml) and follow the steps to add the necessary front matter to your YAML file.
 
- You need to make sure the mat has your your Wi-Fi credentials. You can either put your details directly into this file (you must have double quotations around the SSID and the password) or use the secrets.yaml file (optional steps below).

<img src="../../images/ESPHome_mat_yaml_wifi_secrets.png" width="600"> 

- (Optional, using secrets.yaml) Get to the Open Web UI view and click on “Secrets” in the top right corner. 

<img src="../../images/ESPHome_secrets.png" width="600"> 

-	(Optional, using secrets.yaml) If this file is empty, follow the structure of the information in the image and put in your SSID and password inside the double quotations just like the made up Wi-Fi details below. Click Save.

<img src="../../images/ESPHome_secrets_yaml.png" width="600"> 

-	Once you have the TrampleTek Blue YAML code copied in, save and upload:

<img src="../../images/ESPHome_mat_yaml_save_upload.png" width="600"> 
 
-	You will be prompted with the install list, we will use “Plug into the computer” again. Follow the same steps we used previously to install the new YAML code onto the mat (the [your mat’s name].bin will have the same name).

<img src="../../images/ESPHome_mat_yaml_plug_computer.png" width="600"> 

- The following steps are a repeat of the previous section, I will just put the images here as a reminder. If you need the full guide, go back to the [Loading ESPHome on the TrampleTek mat](https://ascmats.github.io/docs/Manual-Installation/mat_install.html) on the side navigation bar.

<img src="../../images/download_project_wating.png" width="600"> 

<img src="../../images/download_project_done.png" width="600"> 

<img src="../../images/modern_format.png" width="600">  

<img src="../../images/keep_bin_file.png" width="600"> 

<img src="../../images/open_ESPHome_web.png" width="600">  

<img src="../../images/ESPHome_web_connect.png" width="600"> 

<img src="../../images/ESPHome_web_connect_usb.png" width="600"> 

<img src="../../images/ESPHome_web_connect_install.png" width="600"> 

<img src="../../images/ESPHome_web_connect_bin_browse.png" width="600"> 

<img src="../../images/ESPHome_web_connect_bin_install.png" width="600">

If this step fails go to [Boot Mode Instructions](https://ascmats.github.io/bootmode.html).

<img src="../../images/ESPHome_web_connect_installing.png" width="600"> 

<img src="../../images/ESPHome_web_connect_install_success.png" width="600">
 
-	 After you finish installing, you can close out of ESPHome Web tab and navigate back to the ESPHome Open Web UI and click on “LOGS”. (Main Home Assistant page -> settings-> add-on -> ESPHome -> Open Web UI).

<img src="../../images/ESPHome_mat_yaml_logs.png" width="600"> 
 
-	 If everything was successful, you should see your Wi-Fi details in the log, along with a stream of data coming out of the mat. The mat is successfully connected and sending data to Home Assistant!

<img src="../../images/ESPHome_mat_yaml_logs_wifi.png" width="600"> 
 
-	NOTE: If you ever need to save and install any changes to the YAML code, you should be able to use the “Wirelessly” install option moving forward. With the “output_power: 8.5dB” line in your YAML the wireless connection should be stable enough to use this option.)

## Next Steps
Let's move on to [configuring the mat into the Home Assistant UI](https://ascmats.github.io/docs/Manual-Installation/HAintegration.html).

Please join the [ASC Discord server](https://discord.gg/cB9P6NmYJg) if you have questions or comments about this page.
