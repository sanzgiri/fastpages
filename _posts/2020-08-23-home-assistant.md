---
title: "Home Automation with a Raspberry Pi"
description: "Setting up Home Assistant on a Raspberry Pi 4"
layout: post
toc: false
comments: true
hide: false
search_exclude: false
categories: [automation, iot]
---

I had come across [Home Assistant](https://www.home-assistant.io/) a while back, and 
finally set it up this weekend. It was pretty quick and easy.

I ordered the [Canakit Raspberrry Pi 4 8 GB Extreme Kit](https://www.amazon.com/gp/product/B08B6F1FV5)
from Amazon. The full list of supported hardware can be found in the [Home Assistant Installation](https://www.home-assistant.io/hassio/installation/) 
instructions.

There are a couple of things to be done differently for a Pi 4:

* I used the latest build [Development 5, Release 1](https://github.com/home-assistant/operating-system/releases/tag/5.1), 
specifically the 64-bit version (hassos_rpi4-64-5.1.img.gz)

* As described in the instructions, I set up the WiFi using a blank USB stick (FAT 32 format,
 volume label CONFIG) with a file /network/my-network with the contents shown [here](https://github.com/home-assistant/operating-system/blob/dev/Documentation/network.md):
  the example under "Wireless LAN WPA/PSK". Only lines to change here are the ssid and psk settings for ure wireless LAN.
  
* That was it. After rebooting you can access your Home Assistant at http://homeassistant.local:8123
 
 
  