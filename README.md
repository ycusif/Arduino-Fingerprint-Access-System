# Arduino Fingerprint Access System

## Overview
Embedded biometric authentication system using Arduino UNO and the R307 fingerprint sensor.  
Implements two subsystems: access verification and fingerprint enrollment.

## Hardware
- Arduino UNO  
- R307 fingerprint sensor  
- I2C LCD 16x2  
- Green LED on pin 4  
- Red LED on pin 5  
- Buzzer on pin 6  

## Wiring
- R307 TX → D2  
- R307 RX → D3  
- VCC → 5V  
- GND → GND  
- LCD SDA → A4  
- LCD SCL → A5  

## Code Files
### `access_mode.ino`
Processes fingerprint images, converts them to templates, performs fast search, and provides feedback through LCD, LEDs, and buzzer.

### `enroll_mode.ino`
Guides enrollment through serial monitor. Captures two images of the same finger, generates a template, and stores it under an ID in sensor flash.

## Usage
Upload `enroll_mode.ino` to register IDs.  
Upload `access_mode.ino` to run the access system.

## Notes
Sensor uses 57600 baud.  
LCD address defaults to 0x27.  
System requires stable 5V power.
