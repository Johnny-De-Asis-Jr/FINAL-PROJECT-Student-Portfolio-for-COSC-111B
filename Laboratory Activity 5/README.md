# Laboratory Activity #5: Receiving Serial Connection using Arduino from Python

## 📝 Description
This activity demonstrates **Cross-Platform Serial Communication** by using a Python script as a controller for an Arduino-based hardware circuit. It moves beyond the standard Serial Monitor by implementing a custom Python UI that sends encoded characters to the MCU to toggle specific hardware states (LEDs).

## 🎯 Objectives
* Understand and implement a bidirectional **Serial Connection** between Python and Arduino.
* Utilize the **PySerial** library to transmit data from a high-level language to a microcontroller.
* Create a hardware circuit controlled remotely via a Python-based terminal interface.

## 🛠️ Components Used
* **Microcontroller:** Arduino Uno
* **Output Devices:** 3x LEDs (Red, Green, Blue)
* **Pins Used:**
    * **Red LED:** Pin 8
    * **Green LED:** Pin 9
    * **Blue LED:** Pin 10
* **Software:** Python 3.x with `pyserial` library installed.
* **Resistors:** 3x 220Ω Resistors and Jumper Wires.



## 💡 Concepts Applied
* **PySerial Communication:** Establishing a baud rate connection (9600) between a Python script and a COM port.
* **State Toggling:** Implementing logic to switch LED states (on-to-off or off-to-on) based on a single recurring command.
* **Case-Insensitive Parsing:** Ensuring both Python and Arduino handle user inputs (e.g., 'R' vs 'r') identically.
* **Non-terminating Loops:** Using a `while True` loop in Python to maintain the controller interface until an exit command is given.

## ⚙️ System Behavior
The system acts as a remote LED controller with the following command logic:

| Input | Action |
| :--- | :--- |
| **R / r** | Toggle **Red LED** (On/Off) |
| **G / g** | Toggle **Green LED** (On/Off) |
| **B / b** | Toggle **Blue LED** (On/Off) |
| **A / a** | Turn **ALL** LEDs ON |
| **O / o** | Turn **ALL** LEDs OFF |
| **X / x** | Terminate the Python script |

* **Error Handling:** Any other inputs sent via the Python script will return an error message in the console.
* **UI Refresh:** (Optional implementation) The Python console clears and reprints the menu after every action for a clean user experience.



## 📂 Repository Content
* **Arduino Code:** `*.ino` file (handling serial input and LED toggling).
* **Python Script:** `*.py` file (the user interface and serial sender).
* **Diagram:** Breadboard diagram illustrating the RGB LED connections.

## 👥 Members
| De Asis, Johnny Jr. S. | Osit, Eduardo V. | Padilla, Allexzeus Marvel C. |
