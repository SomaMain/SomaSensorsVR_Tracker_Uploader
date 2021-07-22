# SomaSensorsVR_Tracker_Uploader
Upload the tracking software to the ESP32 boards (both hub and tracker)

This software is currently only for ESP32 boards and MPU9250 IMUs.

To use this program, you will need to download the Arduino IDE : https://www.arduino.cc/en/software
Once you have it downloaded, open up a blank project.
Go to File > Preferences
Click on the textbox for "Additional Board Manager URLs:" and add the following line:
https://dl.espressif.com/dl/package_esp32_index.json,http://arduino.esp8266.com/stable/package_esp8266com_index.json
This will allow you to download the ESP32 board mangager.
Click OK.

Next, in the arduino IDE Go to
Tools > Board > Board Manager
Search "esp32" and download the esp32 by Espressif Systems version 1.0.6
Click Close.

Once that is installed, you should be able to use the Uploader!
