Security Alert System using STM32
Project Description

This project demonstrates a simple security alert system built using the STM32 Nucleo development board, an ultrasonic sensor, a buzzer, and an LED. The system is designed to detect the presence of an object or intruder within a predefined distance range and provide an alert indication using both visual and audio outputs. The ultrasonic sensor continuously measures the distance of nearby objects, and when an object is detected within the threshold distance, the STM32 microcontroller activates the buzzer and LED to indicate a possible intrusion. This project demonstrates the implementation of a basic embedded security monitoring system using real-time sensing and output control.

Objectives

The main objectives of this project are to interface an ultrasonic sensor with the STM32 microcontroller for object detection, implement distance-based intrusion detection logic, control a buzzer and LED as alert mechanisms, and demonstrate real-time embedded system monitoring and response.

Hardware Used

The hardware components used in this project include the STM32 Nucleo Development Board, an HC-SR04 Ultrasonic Sensor, a buzzer, an LED, jumper wires, a breadboard, and a power supply. The STM32 board acts as the central controller, the ultrasonic sensor performs intrusion detection, and the buzzer and LED provide alert indications.

Pin Configuration

The ultrasonic sensor’s TRIG pin is connected to PA1 configured as a GPIO output, and the ECHO pin is connected to PA2 configured as a GPIO input. The buzzer is connected to PB5 configured as a digital output pin, and the LED is connected to PB3 configured as a digital output pin. Proper ground and power connections are provided to all components.

System Functionality

The system operates by continuously measuring the distance between the ultrasonic sensor and nearby objects. The STM32 sends a trigger pulse to the ultrasonic sensor, which emits ultrasonic waves and waits for the reflected echo signal. The time taken for the echo to return is measured using an internal timer, and the distance is calculated using the ultrasonic distance formula. When an object or person enters the predefined detection range, the STM32 interprets it as an intrusion event and activates the buzzer and LED. The buzzer produces an audible alert while the LED provides a visual indication. When the object moves away from the detection range, the alert devices are turned OFF automatically.

Output Behavior

The output of the system is observed through the buzzer and LED. When an object is detected within the threshold distance, the LED glows and the buzzer sounds continuously, indicating a security alert. Once the object leaves the monitored region, both the LED and buzzer turn OFF automatically.

Software Details

The project is implemented in the C programming language using STM32CubeIDE. STM32 HAL libraries are used for configuring and controlling GPIO pins and timers. The ultrasonic sensor interfacing is implemented using precise timing functions, while the LED and buzzer are controlled through digital output signals.

How to Run

To run the project, open the project in STM32CubeIDE and configure the GPIO pins and timers according to the specified pin configuration. Connect the ultrasonic sensor, LED, and buzzer to the STM32 board as required. Build and flash the code onto the STM32 Nucleo board using a USB connection. Once powered, the system continuously monitors the surroundings, and whenever an object enters the threshold distance, the buzzer and LED are activated automatically to indicate a security alert.
