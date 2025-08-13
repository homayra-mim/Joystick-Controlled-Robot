🤖 Wireless Joystick Controlled Robot (Arduino Nano)
This project demonstrates how to control a two-wheel robot wirelessly using a joystick transmitter and receiver setup.
The Arduino Nano on the robot receives joystick data via serial communication (e.g., RF modules, Bluetooth, or any wireless link) and controls motors, LEDs, and a buzzer based on the received commands.

📌 Features
Wireless control of robot movement (forward, backward, left, right, stop)
Two speed modes: Fast and Slow
Toggleable buzzer and LEDs
PWM motor speed control for smooth movement
Fully Arduino Nano–based

🛠 Hardware Required
Arduino Nano (Robot side)
Motor driver (L298N / L293D)
DC motors (x2) with wheels
RF Transmitter & Receiver modules (or any wireless serial link like Bluetooth HC-05, nRF24L01, etc.)
Joystick module (on transmitter side)
Buzzer
LEDs (2 pieces)
Breadboard & jumper wires
Battery pack for robot

🔌 Pin Connections (Robot Side – Arduino Nano)
Arduino Pin	Connected To	Description
D5	Motor Left (ML1)	Direction control
D4	Motor Left (ML2)	Direction control
D13	Motor Right (MR1)	Direction control
D12	Motor Right (MR2)	Direction control
D3 (PWM)	EL	Speed control left
D11 (PWM)	ER	Speed control right
D2	Buzzer	Toggle on/off
D7	LED1	Toggle on/off
D6	LED2	Toggle on/off

📡 Command Protocol
The robot receives commands from the transmitter as serial data:
a# → Toggle buzzer
b# → Toggle LED 1
c# → Toggle LED 2
x# → Set fast speed
z# → Set slow speed
~X*Y@Z# → Movement vector data (joystick values)

📄 How It Works
The transmitter reads joystick values and button presses.
Commands are sent wirelessly as serial data to the receiver Arduino.
The receiver parses incoming commands:
Controls motor direction and speed based on joystick values.
Toggles buzzer or LEDs when respective buttons are pressed.
PWM control is used for smooth acceleration/deceleration.

🚀 Getting Started
Upload the provided code to your Arduino Nano on the robot side.
Make sure your transmitter sends serial commands in the defined format.
Power the robot and transmitter.
Move the joystick and press buttons — your robot should respond instantly.
