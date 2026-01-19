# Finals Laboratory Exam: Arduino-to-Python API Client

## 📝 Description
This project implements a remote-trigger system where an Arduino acts as a client. A physical button press on the Arduino sends a signal via Serial to a Python program, which then calls a predefined API endpoint to control a remote LED system.

## 🎯 Objectives
* Implement **software debouncing** to ensure one button press sends exactly one signal.
* Create a **non-terminating Python application** to listen to serial ports.
* Normalize serial input to avoid case-sensitivity issues during processing.
* Establish communication with an external API using HTTP requests via Python.

## 🛠️ Components Used
* **Arduino Uno**
* **Push Button**: Serves as the primary input device
* **Python Environment**: With `pyserial` and `requests` libraries installed.

## 💡 Concepts Applied
* **Client-Server Architecture**: The Arduino sends local signals to a Python client that interacts with a remote API.
* **Serial Signal Validation**: Ensuring the group number is extracted and normalized from the input.
* **Software Debouncing**: Preventing repeated API calls from long button presses.
* **HTTP Integration**: Using Python to call endpoints in the format `/led/group/<number>/toggle`.

## ⚙️ System Behavior
1. **Trigger**: User presses the button on the Arduino.
2. **Serial Transmission**: Arduino sends the assigned group number to the Python client.
3. **Python Processing**: Python extracts the data, normalizes it, and sends a GET/POST request to the API.
4. **Feedback**: The Python terminal displays the group number, the endpoint called, and the API success/error status.

## 📂 Repository Content
* `.ino`: Arduino sketch with software debouncing and serial output.
* `.py`: Non-terminating Python script for serial listening and API calling.
* `.png`: Wiring diagram for the push button setup.

## 👥 Members
| Barrion, Merell Joy B. | De Asis, Johnny Jr. S. | Francisco, Gerard Obey S. | Osit, Eduardo V. | Padilla, Allexzeus Marvel C. | Roldan, Maureen T. |
