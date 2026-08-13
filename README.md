# Bluetooh-Jammer
nrfBlueNullifier
A tool which jam classic bluetooth signals using 1 nrf24L01 module at HSPI.

Requirements
ESP-32S 38-Pins
One nrf24L01 Module OR nrf24L01+PA/LNA Module
7 Female to Female Jumper Wires
Note
nrf24L01 and nrf24L01+PA/LNA modules have same pinout.




Pinout Table
NODEMCU ESP32S	nrf24L01
3.3V	VCC
GND	GND
GPIO16	CE
GPIO15	CSN
GPIO14	SCK
GPIO13	MOSI
GPIO12	MISO
NodeMCU ESP-32S nrf24L01




Setup
Download Arduino IDE from here according to your Operating System.
Install it.
Go to File → Preferences → Additional Boards Manager URLs.
Paste the following link :
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
Click on OK.
Go to Tools → Board → Board Manager.
Wait for sometimes and search esp32 by Espressif Systems.
Simply install it.
Wait for sometime and after that it is installed.
Go to Sketch → Include Library → Manage Libraries.
Wait for sometimes and search rf24 by TMRh20, Avamander.
Simply install it.
Wait for sometime and after that it is installed.
Restart the Arduino IDE by closing and open again.
Done!


Install
Download or Clone the Repository.
Open the folder and just double click on nrfBlueNullifier.ino file.
It opens in Arduino IDE.
Compile the code.
Select the correct board from the Tools → Board → ESP32 Arduino.
It is generally NodeMCU-32S.
Select the correct port number of that board.
Upload the code.
When show Connecting..... press and hold BOOT button.
When show Writing at  then release the BOOT button.
Done!
The script starts running automatically.




Install using ESP Web Flasher
Open Adafruit ESP Web Flasher from here.
Set the Baud Rate to 115200 Baud.
Connect ESP32 with a USB cable and then to the PC/Laptop.
Press and hold the BOOT button.
Click on Connect button.
Select your Device COM Port in the Pop-Up Window.
Release the BOOT button.
When connected successfully, then it show this Adafruit ESP Web Flasher
Click on Erase button.
Wait for sometimes to successfully erased.
Download 3 files from this directory.
The files are :
nrfBlueNullifier-HSPI-nrf24L01-Jammer-bootloader.bin
nrfBlueNullifier-HSPI-nrf24L01Jammer-partitions.bin
nrfBlueNullifier-HSPIJammer-nrf24L01.bin
Select nrfBlueNullifier-HSPI-nrf24L01-Jammer-bootloader.bin file with offset 0x1000.
Select nrfBlueNullifier-HSPI-nrf24L01-Jammer-partitions.bin file with offset 0x8000.
Select nrfBlueNullifier-HSPI-Jammer-nrf24L01.bin file with offset 0x10000.
Click on Program button.
Wait for sometimes to successfully programmed.
Press and release the BOOT button.
Unplug and plug the ESP32 on the PC/Laptop.
Done! nrfBlueNullifier-HSPI-nrf24L01 is ready.



What happened after script is running?
It breaks the sound.
It blocks the sound even the device playing the music.
Sometimes it disconnects the bluetoth from the device.




Modification In Code
The code effects on classic bluetooth and wifi.
If want to put most of the effect on classic bluetooth only, modify the code by replacing the code in line 14 by following :
byte hopping_channel[] = {32, 34, 46, 48, 50, 52, 26, 28, 30, 74, 76, 78};
Save the code.
Compile the code and then upload it.
What happened after modified script is running?
It blocks the sound even the device playing the music.
It slow down the speed of the wifi.
