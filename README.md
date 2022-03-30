# esp8266-homekit-button
This is a native HomeKit button with D1 mini ESP8266.

## Hardware
The following hardware is required:
```
- D1 mini (ESP8266)
- Resistor 10kOhm
- Button
```

Connection:
D1 mini -> Button (Pin A, Pin B)
```
3V3 -> 10kOhm -> Button Pin A
D1 -> Button Pin A
GND -> Button Pin B
```
![alt text](https://github.com/datjan/esp8266-homekit-button/blob/main/Schema.png?raw=true)

## Development
This sketch is for following development environment
```
Arduino
```

Following libraries are required
```
https://github.com/datjan/Arduino-HomeKit-ESP8266 (fork from Mixiaoxiao/Arduino-HomeKit-ESP8266:master)
```

## Setup
Setup my_accessory.c:
```
.password = "555-11-123"  // Homekit Code
```

Setup wifi_info.h
```
const char *ssid = "xxx"; // SETUP Wlan ssid
const char *password = "xxx"; // SETUP Wlan password
```

## Upload to device
Following files needs to be uploaded to the ESP8266 (D1 mini)
```
esp8266-homekit-button.ino
ESPButton.h
my_accessory.c
wifi_info.h
```

## Add device to Homekit
The device can be added to homekit like every other homekit device.
The button reacts to single, double and long click.
