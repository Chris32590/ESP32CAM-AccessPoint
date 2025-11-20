Cybersecurity : CSN150
Project: ESP32-CAM Access Point Web Server

Purpose
Set up the ESP32-CAM and Arduino IDE environment. Execute a sketch that turns the ESP32 into a Wi-Fi Access Point and serves a custom web page.

Equipment
ESP32-CAM

FTDI Programmer (set to 5V)

USB Micro Data Cable

Jumper Wires

Arduino IDE

Links to Documentation and Tools
Tutorial: ESP32-CAM Access Point Web Server – Random Nerd Tutorials

Driver (if needed): CH341SER USB-to-Serial Driver

AI GPTs Used: Microsoft Copilot (for troubleshooting, documentation, and formatting)

Steps I Followed
Cloned the CSN150 documentation template from GitHub

Installed the ESP32 board in Arduino IDE

Connected ESP32-CAM to FTDI programmer (set to 5V)

Uploaded sketch using WiFi.softAP() to create access point

Opened Serial Monitor to confirm IP address

Connected to ESP32 Wi-Fi network from phone

Opened browser and visited http://192.***.**

Saw message: “Hello Christopher Perez from ESP32 Access Point!”

problems and Solutions
Problem: ESP32 Wi-Fi network not showing on phone Solution:

Replaced WiFi.begin() with WiFi.softAP()

Confirmed FTDI adapter was set to 5V

Reset the board after upload

Verified sketch output in Serial Monitor

Problem: E (485) camera: Camera probe failed with error 0x105 (ESP_ERR_NOT_FOUND) Solution:

Installed correct USB-to-Serial driver: CH341SER.ZIP

Used Serial Monitor to confirm successful upload and board detection

Example Problem: Problem: Arduino code would not load on ESP32-CAM Solution: Camera drivers were incorrect. Installed CH341SER.ZIP and upload worked.

Final Report
This project successfully configured the ESP32-CAM as a standalone Wi-Fi access point that hosts a simple web server. The device broadcasts its own network, allowing any nearby device to connect and view a custom message in the browser. Key learning outcomes included configuring embedded networking, troubleshooting power and driver issues, and documenting the process using GitHub.
