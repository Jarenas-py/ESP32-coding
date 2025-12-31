# ESP32 IoT & Automation Projects

Welcome to the **ESP32 IoT & Automation Projects**. This repository features a collection of basic to intermediate level projects designed for the ESP32 microcontroller.

The goal of this collection is to demonstrate the ESP32's capabilities in **Internet of Things (IoT)**, **Sensor Fusion**, and **Voice Automation**. It bridges the gap between simple sensor reading and full-scale cloud integration using platforms like **Blynk** and **Sinric Pro**.

## 📂 Featured Projects

### 1. 🗣️ Voice-Activated Smart Home Control
* **Tech Stack:** ESP32, Sinric Pro, Google Assistant, Amazon Alexa.
* **Description:** A smart switch system that allows users to control high-voltage appliances (simulated via LEDs/Relays) using voice commands.
* **Key Features:**
    * Integration with **Google Home** & **Alexa** ecosystems.
    * Real-time status synchronization between physical buttons and the cloud app.
    * Debounced push-button logic for manual override.

### 2. 💧 IoT Water Level & Flood Monitoring
* **Tech Stack:** Ultrasonic Sensor (HC-SR04), Blynk IoT Cloud, LCD I2C.
* **Description:** A precision tank monitoring system that visualizes water levels in real-time on a mobile dashboard and local LCD.
* **Key Features:**
    * Real-time percentage and distance calculation.
    * **Automated Alert System:** Triggers a buzzer and app notification when levels are critical (<25% or >100%).
    * Visual status indicators for "Tank LOW", "Normal", and "FULL".

### 3. 🌱 Smart Agriculture & Gas Safety System (Combined Monitor)
* **Tech Stack:** MQ-2 Gas Sensor, Soil Moisture Sensor, Relay Modules.
* **Description:** A multi-tasking environmental monitor that simultaneously tracks soil health and air safety.
* **Key Features:**
    * **Gas Safety:** Detects hazardous gas levels and triggers an audible alarm + LED warning.
    * **Smart Irrigation:** Monitors soil moisture and allows remote control of a water pump via the Blynk app.
    * **Sensor Fusion:** Combines data from three different sensors (Water, Gas, Soil) into a single unified LCD dashboard with page-switching logic.

## 🛠️ Hardware Requirements

To replicate these projects, you will need:
* **Microcontroller:** ESP32 Development Board (DOIT DEVKIT V1 or similar)
* **Sensors:** HC-SR04 (Ultrasonic), MQ-2 (Gas/Smoke), Capacitive Soil Moisture Sensor
* **Actuators:** 2-Channel 5V Relay Module, Piezo Buzzer, Water Pump (5V/12V)
* **Displays:** 16x2 or 20x4 LCD with I2C Interface
* **Components:** Push Buttons, LEDs, Resistors (220Ω, 1kΩ, 10kΩ), Breadboard, Jumper Wires

## 💻 Software & Libraries

These projects utilize the Arduino IDE and several key libraries. Ensure you have the following installed via the Library Manager:

* `BlynkSimpleEsp32` – For Blynk IoT Cloud connectivity.
* `SinricPro` & `SinricProSwitch` – For Alexa/Google Home voice integration.
* `LiquidCrystal_I2C` – For managing I2C LCD displays.
* `WiFi.h` – Standard ESP32 WiFi library.

## 🚀 Setup & Configuration

1.  **Cloud Setup:**
    * For **Voice Control**: Create an account on [Sinric Pro](https://sinric.pro/), create a "Switch" device, and copy the `APP_KEY` and `APP_SECRET` into the code.
    * For **IoT Monitoring**: Create a template in **Blynk Console**, set up Datastreams (V1, V2, etc.), and copy the `BLYNK_AUTH_TOKEN`.
2.  **WiFi Configuration:**
    * Update the `ssid` and `pass` variables in the code with your local network credentials.
3.  **Wiring:**
    * Refer to the images within each project folder for the circuit wiring.
4.  **Upload:**
    * Select "DOIT ESP32 DEVKIT V1" in Arduino IDE and upload the code.

## 👤 Author

**Joseph Arenas**
* *Student:* BET-CPET (Computer Engineering Technology)
* *Institution:* Technological University of the Philippines - Manila
