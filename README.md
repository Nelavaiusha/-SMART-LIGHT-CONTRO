# -SMART-LIGHT-CONTRO
**COMPANY**: CODTECH IT SOLUTIONS
**NAME**: NELAVAI USHA
**INTERN ID**: CT06DM957
**DOMAIN**: INTERNET OF THINGS
**DURATION**: 6 WEEKS
**MENTOR**: NEELA SANTHOSH
You will be able to turn ON/OFF an LED using a mobile app that communicates with an Arduino board through Bluetooth.

Smart lighting control in IoT refers to using internet-connected devices and sensors to manage and automate lighting systems, offering features like remote control, scheduling, and energy efficiency. These systems can be controlled via smartphones, voice assistants, or central hubs, often incorporating sensors and algorithms to adjust lighting based on user preferences and environmental conditions. 
Key aspects of IoT smart lighting control:
Remote control:
Users can adjust lights from anywhere with an internet connection. 
Automation:
Lights can be programmed to turn on/off, dim, or change color based on schedules, presence detection, or other triggers. 
Energy efficiency:
Smart lighting systems can reduce energy consumption by optimizing light levels based on occupancy, daylight availability, and other factors. 
Personalized user experience:
Users can customize lighting preferences for different moods or activities. 
Integration with other smart home devices:
Smart lighting can be integrated with other devices like thermostats, security systems, and voice assistants to create a comprehensive smart home ecosystem. 
Maintenance and diagnostics:
IoT-enabled lighting systems can provide real-time performance data and alerts for maintenance and troubleshooting. 
Technologies used in IoT smart lighting:
Sensors: Light sensors (ambient and daylight), motion sensors, occupancy sensors. 
Wireless communication: Wi-Fi, Bluetooth, Zigbee, Z-Wave. 
Smart bulbs/fixtures: LED bulbs with embedded chips that enable wireless communication and control. 
IoT gateways: Devices that connect the smart lighting system to the internet and manage communication between devices. 
Cloud platforms: Centralized platforms that allow for remote control, data storage, and analysis. 
Benefits of IoT smart lighting:
Increased energy savings:
By optimizing light levels and reducing unnecessary usage. 
Improved comfort and convenience:
Automated lighting adjustments based on user preferences and environmental conditions. 
Enhanced security:
Remote control and monitoring of lighting in areas that lack proper lighting, such as parking lots and low-traffic streets. 
Reduced maintenance costs:
Real-time diagnostics and alerts can help identify and address issues before they become major problems. 

🔧 Components Required:
1.	Arduino Uno (or any other compatible board)
2.	Bluetooth module (HC-05 or HC-06)
3.	LED
4.	220Ω resistor
5.	Jumper wires
6.	Breadboard
7.	Smartphone
8.	Mobile App (like Bluetooth Terminal or custom app)
⚙️ Circuit Diagram:
Arduino Pin      | Connects To
-----------------|-------------------------
D13              | LED +ve (through 220Ω resistor)
GND              | LED -ve
TX (Pin 1)       | RX of HC-05
RX (Pin 0)       | TX of HC-05
5V               | VCC of HC-05
GND              | GND of HC-05
Note: Use voltage divider for HC-05 TX to Arduino RX to avoid 5V damage (optional but recommended).
________________________________________
🧠 Arduino Code:
char data = 0;

void setup() {
  pinMode(13, OUTPUT);   // LED connected to digital pin 13
  Serial.begin(9600);    // Start serial communication at 9600 baud rate
}

void loop() {
  if (Serial.available()) {
    data = Serial.read();   // Read the incoming data

    if (data == '1') {
      digitalWrite(13, HIGH); // Turn LED ON
    } else if (data == '0') {
      digitalWrite(13, LOW);  // Turn LED OFF
    }
  }
}________________________________________
📱 Mobile App :
•	App: "Bluetooth Terminal" or "Serial Bluetooth Terminal" (Android)
•	How to Use:
o	Pair your phone with HC-05.
o	Open the app, connect to HC-05.
o	Send 1 to turn ON LED, 0 to turn it OFF.   
________________________________________
💡 Working:
1.	Power Arduino and connect HC-05.
2.	Pair your phone with HC-05 using password 1234 or 0000.
3.	Open Bluetooth Terminal.
4.	Send 1 to turn ON the LED, 0 to turn it OFF.
________________________________________
🔁 Extensions You Can Try:
•	Use voice control using Google Assistant + IFTTT
•	Add a brightness control using PWM
•	Use Wi-Fi (ESP8266 or ESP32) instead of Bluetooth for remote access

#OUTOUT
![Image](https://github.com/user-attachments/assets/59392378-2467-4746-8e20-a71b061c9501)



