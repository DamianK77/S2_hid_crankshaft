# ESP32 S2 hid for crankshaft

## Function

This is a simple ESP32 S2 project made in ESP-IDF. Its purpose is to register as a keyboard and send keycodes based on pin states. This program is universal but is meant to work with crankshaft NG and android auto. In crankshaft settings you can enable keyboard control for android auto functions, such as pausing the music.

## How to use
Written in ESP-IDF 5.0. Requires tinyusb component. You should set the TinyUSB HID interfaces count parameter in menuconfig to 1. Otherwise upload as normal, after resetting the microcontroller should appear as a keyboard/mouse interface. Normally open switches should be connected between pins and ground (pins are pulled up internally). No extra electronics required.

## Usage with CrankshaftNG
 
ESP32 S2 will "press keys" required by Crankshaft NG to for example switch or pause music. You can customise which pin corresponds to which action by changing the main.c file. 
