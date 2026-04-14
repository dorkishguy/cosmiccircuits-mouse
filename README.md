# ESP8266 Wi-Fi Button Mouse

A custom computer mouse built during [Name of Hackathon] using an ESP8266 (NodeMCU) and 7 tactile buttons. This project bypasses the lack of native USB HID support on the ESP8266 by streaming movement data over UDP to a Python receiver script.

## 🛠 Features
- **4-Way D-Pad:** Dedicated buttons for Up, Down, Left, and Right movement.
- **Full Click Support:** Left, Right, and Middle click functionality.
- **Wi-Fi Connectivity:** Fully wireless operation within the local network.
- **Python Backend:** Uses `pyautogui` for smooth cursor manipulation.

## 🔌 Hardware Setup
The project uses a **Common Ground** wiring strategy. One side of every button is tied to a shared Ground (GND) rail.

| Button Function | ESP8266 Pin |
| :--- | :--- |
| Move Up | D1 (GPIO5) |
| Move Down | D2 (GPIO4) |
| Move Left | D3 (GPIO0) |
| Move Right | D4 (GPIO2) |
| Left Click | D5 (GPIO14) |
| Right Click | D6 (GPIO12) |
| Middle Click | D7 (GPIO13) |

## 💻 Software Requirements
1. **Arduino IDE**: To flash the ESP8266.
2. **Python 3.x**: To run the receiver script.
3. **PyAutoGUI**: `pip install pyautogui`

## 🏃‍♂️ How to Run
1. Update the `ssid`, `password`, and `pcIP` in the Arduino code.
2. Upload the code to your ESP8266.
3. Run the Python receiver: `python receiver.py`
4. Start moving your mouse!
