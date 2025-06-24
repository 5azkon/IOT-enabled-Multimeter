# 📟 IOT-enabled Multimeter

An affordable and scalable smart multimeter using the ESP32 microcontroller that measures voltage and current, takes ECU serial input via a 4x5 matrix keypad, and uploads real-time data to **Google Sheets** using Wi-Fi.

![](https://github.com/5azkon/IOT-enabled-Multimeter/blob/main/PROTOTYPE/Prototype.jpg)

## 🛠️ Features

- 📐 Measures **DC voltage** (e.g., 9V, 12V, 24V)
- 🔌 Calculates **current** using a shunt resistor
- ⌨️ **4x5 matrix keypad** to input ECU serial number
- 🔘 Push button to trigger data capture and upload
- ☁️ Sends data to **Google Sheets** via API
- 📊 View and log live electrical parameters remotely

---
## 📸 Block Diagram
![](https://github.com/5azkon/IOT-enabled-Multimeter/blob/main/DOCUMENTS/Block%20diagram.png)
---
## 🔋 Hardware Components

| Component              | Description                          |
|------------------------|--------------------------------------|
| ESP32                  | Wi-Fi-enabled microcontroller        |
| JST Connector          | For DC power input                   |
| Voltage Divider Circuit| To scale down voltage for ADC       |
| Shunt Resistor         | For current sensing                  |
| 4x5 Matrix Keypad      | Serial number input                  |
| Push Button            | Triggers measurement                 |
| Capacitors             | For circuit stability                |
| Optional Monitor       | For debugging/output (optional)      |

---

## 💻 Software Requirements

- Arduino IDE
- ESP32 Board Support Package
- Libraries:
  - `WiFi.h`
  - `HTTPClient.h`
  - `Keypad.h`
- Google Apps Script Web App (for Google Sheets API)

---

## 📦 Installation

1. Clone or download this repository.
2. Open the `.ino` file in Arduino IDE.
3. Install required libraries (`Keypad`, `WiFi`, `HTTPClient`) from Library Manager.
4. Update the following fields in the code:
   ```cpp
   const char* ssid = "YOUR_SSID";
   const char* password = "YOUR_PASSWORD";
   const char* serverName = "YOUR_GOOGLE_SCRIPT_URL";

5.Upload the code to your ESP32 board.

6.Power the circuit and connect input voltage via JST connector.

## ⚙️ How It Works
1.Technician enters the ECU serial number using the 4x5 matrix keypad.

2.Presses the push button.

3.ESP32 reads:

4.Voltage via voltage divider

5.Current via shunt resistor

6.Converts analog values into readable electrical units.

7.Sends data to Google Sheets via Wi-Fi + HTTP GET.

![Simulation]
---------
### 📽️ Project Demo
Full video here 👇

[![Watch on YouTube](https://img.youtube.com/vi/urKTJmTIu4k/hqdefault.jpg)](https://www.youtube.com/shorts/urKTJmTIu4k)

-----------
## 📌 Applications
🛠️ Used in CMRL stations for decentralized maintenance
🧪 Suitable for lab measurements
🛰️ Remote data acquisition in IoT/embedded systems
🧰 Cost-effective alternative to commercial multimeters

---------------
## Social media:- (www.linkedin.com/in/mr-5azkon)
