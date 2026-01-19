# Laboratory Activity #6: Bidirectional Control Using Arduino and Python

## 📝 Description
This project implements a complete **Bidirectional (Full-Duplex) Serial Connection**. Unlike previous labs where Python acted only as a remote, this system involves the Arduino sending "Outbound" signals (button presses) to Python, which then processes that data and sends "Inbound" commands back to the Arduino to toggle LEDs. This simulates a real-world IoT handshake protocol.

## 🎯 Objectives
* Implement a **bi-directional serial bridge** between an MCU and a high-level language.
* Manage state-change detection for push buttons to prevent "spamming" signals.
* Achieve high-performance serial communication with a response latency of less than 1 second.

## 🛠️ Components Used
* **Microcontroller:** Arduino Uno
* **Output Devices:** 3x LEDs (Red, Green, Blue)
* **Input Devices:** 3x Push Buttons
* **Pins Used:**
    * **LEDs:** Red (7), Green (6), Blue (5)
    * **Buttons:** Button 1 (12), Button 2 (11), Button 3 (10)
* **Resistors:** 3x 220Ω (LEDs) and 3x 10kΩ (Pull-down resistors for buttons)



## 💡 Concepts Applied
* **Outbound Signaling:** The Arduino monitors button states and sends a single character (`R`, `G`, or `B`) over Serial the moment a press is detected.
* **Inbound Command Logic:** The Arduino listens for numerical strings (`1`, `2`, or `3`) to toggle specific LED states.
* **Python Event Handling:** A Python script acts as the "Brain," intercepting button characters and mapping them to numerical commands sent back to the hardware.
* **Debouncing & State Logic:** Ensuring the Arduino only sends a character **once** per physical click.

## ⚙️ System Behavior
The workflow follows a circular logic path:

1.  **Physical Trigger:** A user presses Button 1 (Pin 12).
2.  **Arduino Outbound:** Arduino detects the press and sends the character `'R'` to the Serial port.
3.  **Python Processing:** Python reads `'R'`, recognizes the request, and immediately writes `'1'` back to the Serial port.
4.  **Arduino Inbound:** Arduino receives `'1'` and toggles the **Red LED** state.

| Button | Outbound (to Python) | Inbound (to Arduino) | Result |
| :--- | :--- | :--- | :--- |
| Button 1 | `R` | `1` | Toggle Red LED |
| Button 2 | `G` | `2` | Toggle Green LED |
| Button 3 | `B` | `3` | Toggle Blue LED |

## 📂 Repository Content
* **Arduino Sketch:** `.ino` file containing the button-sensing logic and the `serial.read()` toggle switch.
* **Python Script:** `.py` file utilizing `pyserial` to create the automated loopback and user feedback.
* **Circuit Diagram:** A breadboard layout showing the 3-LED, 3-Button configuration.

## 👥 Members
| Barrion, Merell Joy B. | De Asis, Johnny Jr. S. | Francisco, Gerard Obey S. | Osit, Eduardo V. | Padilla, Allexzeus Marvel C. | Roldan, Maureen T. |
