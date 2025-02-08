# Smart Navigation Stick

## Project Overview
The **Smart Navigation Stick** is a device designed to assist visually impaired individuals in navigating their surroundings. It uses an **ultrasonic sensor** to measure the distance between the user and nearby objects. If an object is too close (below a certain threshold), the device activates a **buzzer** and an **LED** to alert the user.

### Features:
- **Ultrasonic Distance Measurement**: Measures the distance using an ultrasonic sensor (HC-SR04).
- **Buzzer Alert**: Activates a buzzer when an object is detected within a certain distance.
- **LED Indicator**: Lights up when the object is too close.
- **Simple and Affordable**: Built using common Arduino components.

## Components Used:
- **Arduino Uno**
- **HC-SR04 Ultrasonic Sensor**
- **Buzzer**
- **LED**
- **Jumper Wires**
- **Breadboard**

## Wiring Diagram
- **Trig Pin** → Arduino Pin 9
- **Echo Pin** → Arduino Pin 10
- **Buzzer** → Arduino Pin 11
- **LED** → Arduino Pin 13
- **VCC, GND** for ultrasonic sensor connected to Arduino's 5V and GND.

## Code
The code uses the **HC-SR04 ultrasonic sensor** to measure the distance and triggers the **buzzer** and **LED** when the measured distance is below a certain threshold (5 cm in this case). The following logic is implemented:
- **Triggering the ultrasonic sensor**: A HIGH pulse is sent to the trigPin for 10 microseconds.
- **Reading the echoPin**: The time taken for the sound to return is measured using `pulseIn()`.
- **Distance Calculation**: The formula `distance = duration * 0.0343 / 2` is used to calculate the distance.
- **Threshold Check**: If the distance is less than or equal to 5 cm, the buzzer and LED are turned ON. Otherwise, they are OFF.

Installation
Clone this repository to your local machine:

bash
Copy
Edit
git clone https://github.com/Elakkiya-16/SmartStick.git
Open the project folder in the Arduino IDE.

Connect the Arduino Uno to your computer via USB.

Select the appropriate board and port in the Arduino IDE.

Upload the code to the Arduino Uno.

Once uploaded, the Smart Navigation Stick should be functional.
