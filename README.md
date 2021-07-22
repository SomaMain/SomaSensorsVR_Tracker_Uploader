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

Open the Uploader, plug in your hub or tracker
Scan for the comPort and select the correct one
select your location or hub
Upload

To manually run the script from a Command Prompt:

C:\Users\USER_NAME\AppData\Local\Arduino15\packages\esp32\tools\esptool_py\3.0.0/esptool.exe --chip esp32 --port COM4 --baud 921600 --before default_reset --after hard_reset write_flash -z --flash_mode dio --flash_freq 80m --flash_size detect 0xe000 C:\Users\USER_NAME\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.6/tools/partitions/boot_app0.bin 0x1000 C:\Users\USER_NAME\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.6/tools/sdk/bin/bootloader_qio_80m.bin 0x10000 C:\Users\USER_NAME\Desktop\SomaStuff\SomaSensorsVR_Tracker_Uploader-main\Uploader_For_Tracker_v0.1\Hub_Version\1.8/Hub.ino.bin 0x8000 C:\Users\<USER_NAME>\Desktop\SomaStuff\SomaSensorsVR_Tracker_Uploader-main\Uploader_For_Tracker_v0.1\Hub_Version\1.8/Hub.ino.partitions.bin

Replace <USER_NAME> with your user name

Replace COM4 with whichever com port your tracker is connected to
  
Replace <C:\Users\<USER_NAME>\Desktop\SomaStuff\SomaSensorsVR_Tracker_Uploader-main\Uploader_For_Tracker_v0.1\Hub_Version\1.8> with whatever directory you saved the uploader folder to.
