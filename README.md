# Buy a ready to use PCB on [shop.tynet.eu](https://shop.tynet.eu/rs485-bridge-diy-hoermann-mqtt-adapter-esp32-s3-dev-board) :rocket:

If you use a PCB from us, you can get started with our instructions: [Getting started with tynet.eu PCBs](https://github.com/Tysonpower/Tynet-HCPBridge/wiki)

Would you like to use our ESPHome-based firmware, which offers a few advantages? See our guide: [Getting started with ESPHome](https://github.com/Tysonpower/Tynet-HCPBridge/wiki/Upgrade-Firmware)

You can find prebuild firmware for our boards in the Firmware folder as non-ESPHome as well as ESPHome version.

<br>

# Hörmann HCPBridge for Home Assistant

This repository includes firmware that emulates the Hörmann UAP1-HCP board (Series 4 motors) as well as the older UAP1 that is used for Series 3 motors.
It uses a ESP32 with a RS485 converter and exposes garage door controls over a web page as well as Home Assistant (directly or MQTT).

<br>

### ESPHome based Firmware

Based on the official [Hörmann Cover Component](https://esphome.io/components/cover/hoermann_hcp/) it is the best Solution if you use Home Assistant as it directly uses their API.

Setup is really quick and the Firmware is really stable thanks to ESPome at it's core. Changing the Firmware or adding Sensors is also simple using the yaml config and recompiling it in ESPHome Device Builder.
There are two different versions, one for Series 4 and one for Series 3 boards - all of our boards ship with ESPHome based firmware.
If you don't use Home Assistant you can modify the yaml configuration to use MQTT as well - but you need to compile the firmware yourself to add your credentials.

<br>

## Features
- Read door status: open/closed/position, light on/off  
- Control: open, close, stop, light toggle, set position (half/vent/custom)  
- Home Assistant Auto Discovery  
- Web Interface for wifi setup & door control  
- OTA Updates
- First-use hotspot (for out-of-the-box Wi-Fi setup) 
- Connects to the strongest AP if the SSID is broadcast by several access points
- Optional external sensors (DS18x20, BME280, DHT22, HC-SR04, HC-SR501, MQ4)
- Support multiple HCP Bridges for multiple garage doors (one bridge per motor)
- Support for ESP32-S3

<br>

## Web UI (ESPHome Webserver V3)

You can use the WebUI for configuration and control of the garage door under.

***http://[deviceip]***
