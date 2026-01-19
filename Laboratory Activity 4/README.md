# Laboratory Activity #4: Arduino Serial Connection

## 📝 Description
This activity focuses on establishing a two-way communication bridge between the Arduino and a computer using the **Serial Monitor**. Building upon the sensor logic from previous labs, this implementation introduces "sticky" alerts—where an alarm state persists even after environmental conditions normalize—until a specific text command is received via the Serial interface.

## 🎯 Objectives
* Understand and implement **Arduino Serial Connection** protocols.
* Utilize and familiarize with basic Serial functions (e.g., `Serial.begin()`, `Serial.available()`, and `Serial.readString()`).
* Create a hardware circuit that responds to real-time user input from a terminal.

## 🛠️ Components Used
* **Microcontroller:** Arduino Uno
* **Input Sensor:** Photoresistor (LDR) connected to Pin A2
* **Output Device:** LED connected to Digital Pin 8
* **Communication:** USB Serial Cable
* **Resistors:** 10kΩ (for LDR voltage divider) and 220Ω (for LED)



## 💡 Concepts Applied
* **Serial Communication:** Utilizing `Serial` functions to send sensor data to the PC and receive control strings back.
* **String Parsing:** Handling incoming data and converting it to lowercase to ensure **case-insensitivity**.
* **State Management:** Using a boolean flag to keep the LED blinking even after the physical trigger (light level) has changed.
* **Conditional Thresholds:** Constant monitoring of analog inputs against a fixed limit.

## ⚙️ System Behavior
The system operates as a light-triggered alarm with a manual override:
1. **Detection:** The photoresistor monitors ambient brightness.
2. **Threshold Trigger:** If the brightness level exceeds **220**, the LED on **Pin 8** begins to blink rapidly (100ms delay).
3. **Persistence:** Once triggered, the LED will **continue to blink** indefinitely, even if the light level drops back below 220.
4. **Serial Override:** The user can stop the alarm by typing the word **"stop"** (case-insensitive, e.g., "STOP", "Stop", "stOP") into the Serial Monitor.
5. **Reset:** Upon receiving the command, the LED stops blinking until the threshold is breached again.

## 📂 Repository Content
* **Sketch File:** `.ino` file containing the Serial logic and case-insensitive string handling.
* **Diagram:** Breadboard diagram showing the Photoresistor on A2 and the LED on Pin 8.

## 👥 Members
| De Asis, Johnny Jr. S. | Osit, Eduardo V. | Padilla, Allexzeus Marvel C. |
