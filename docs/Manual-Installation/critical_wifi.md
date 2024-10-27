---
layout: default
title: CRITICAL FIX (Check or no workie)
parent: Manual Installation
nav_order: 4
---

# CRITICAL FIX

## Over The Air (OTA) updates and Wi-Fi connectivity will not work well unless this line is added to YAML code, please double check it is there:

<img src="../../images/critical_wifi.png" width="600">

This a known issue with the [boards](https://www.wemos.cc/en/latest/c3/c3_mini.html) we are using for the mat, more details [here](https://community.home-assistant.io/t/unable-to-connect-to-wifi-auth-expired-and-association-expired/678570/2).

## If you skip the rest of the setup because you're an expert, please don't skip this step!

In the future we may move away from these boards because of this issue, and although we are reducing the Wi-Fi power a bit with this step it doesn't seem to impact the Wi-Fi range that much and it makes the Wi-Fi connection very stable.

Moving on to [understanding the UI elements of the TrampleTek Blue (Home Assistant version).](https://ascmats.github.io/usingHAui.html)!
