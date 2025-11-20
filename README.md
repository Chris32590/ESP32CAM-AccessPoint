# ESP32CAM-AccessPoint
This project sets up an ESP32-CAM as a Wi-Fi access point that streams live video to a browser. I followed a tutorial to upload the code, connect to the ESP32’s network, and view the camera feed. It helped me learn about embedded networking and troubleshooting microcontrollers.
- Wrote a sketch that uses WiFi.softAP to create a local Wi-Fi network
- Set up a web server that responds with a custom message
- Connected to the ESP32’s network from my phone
- Opened 192.168.4.1 and saw the message: “Hello Christopher Perez from ESP32 Access Point!”

**Problem:** ESP32 Wi-Fi didn’t show up on my phone  
**Fix:** Switched from WiFi.begin to WiFi.softAP, confirmed power supply was 5V, and reset the board
