# Laboratory Activity #7: Controlling Arduino using FastAPI

## 📝 Description
This activity demonstrates the integration of an **HTTP Web API** with hardware control. By utilizing **FastAPI**, we create a web server that listens for specific URL endpoints. When these endpoints are accessed via a browser or an API client (like Postman), the Python backend translates the web request into a serial command sent to the Arduino to manipulate the LED states.

## 🎯 Objectives
* Understand the implementation of **Serial Connections** within a web framework.
* Utilize **FastAPI** to build a RESTful interface for hardware control.
* Create a bridge between **HTTP protocols** and physical electronic circuits.

## 🛠️ Components Used
* **Microcontroller:** Arduino Uno
* **Output Devices:** 3x LEDs (Red, Green, Blue)
* **Pins Used:**
    * **Red LED:** Pin 7
    * **Green LED:** Pin 6
    * **Blue LED:** Pin 5
* **Software:** Python 3.x, FastAPI, Uvicorn (ASGI Server), and PySerial.



## 💡 Concepts Applied
* **RESTful API Routes:** Implementing path parameters to handle dynamic requests (e.g., `/led/{color}`).
* **Serial Interfacing in FastAPI:** Managing a persistent Serial connection within an asynchronous web server environment.
* **JSON Response Handling:** Returning status messages from the API to confirm hardware actions.
* **Hardware Toggling:** Logic-based state switching on the Arduino based on inbound serial characters.

## ⚙️ System Behavior & API Endpoints
The FastAPI server listens for the following routes to control the hardware:

| Endpoint | Method | Action | Serial Sent |
| :--- | :--- | :--- | :--- |
| `/led/red` | GET | Toggles Red LED | `1` |
| `/led/green` | GET | Toggles Green LED | `2` |
| `/led/blue` | GET | Toggles Blue LED | `3` |
| `/led/on` | GET | Turns **ALL** LEDs ON | `A` (or sequential 1,2,3) |
| `/led/off` | GET | Turns **ALL** LEDs OFF | `O` (or sequential 1,2,3) |



## 📂 Repository Content
* **Arduino Sketch:** `.ino` file configured to listen for numerical triggers and toggle LEDs on Pins 5, 6, and 7.
* **Python Web Server:** `.py` file containing the FastAPI application logic and PySerial integration.
* **Circuit Diagram:** Breadboard layout illustrating the LED wiring.

## 👥 Members
| Barrion, Merell Joy B. | De Asis, Johnny Jr. S. | Francisco, Gerard Obey S. | Osit, Eduardo V. | Padilla, Allexzeus Marvel C. | Roldan, Maureen T. |
