# Line Follower Robot (LFR) Project

## Overview
The Line Follower Robot (LFR) is an autonomous robot designed to follow a line using a combination of sensors, motors, and a PID (Proportional-Integral-Derivative) control algorithm. Built with an ESP32 microcontroller, the robot integrates key components such as motor drivers, an OLED display, and sensor arrays for precise navigation.

## Features
- **PID Control**: Ensures smooth and accurate line following by dynamically adjusting motor speed based on sensor input.
- **Sensor Calibration**: Allows adaptation to different line colors and backgrounds for reliable performance.
- **User Interface**: OLED display with interactive menus for sensor calibration, PID tuning, and motor control.
- **Motor Control**: Utilizes a TB6612FNG motor driver to control two DC motors with encoders for precise movement.
- **Line Detection**: A 13-sensor array detects line position, capable of handling both black-on-white and white-on-black backgrounds.
- **Lap Timer**: Measures the time taken to complete a course for performance evaluation.

## Hardware Components
- **Microcontroller**: ESP32
- **Motor Driver**: TB6612FNG
- **Sensors**: 13-line sensor array
- **Display**: 128x64 OLED
- **Motors**: Two DC motors with encoders
- **Buttons**: 4 (Select, Exit, Up, Down) for user interaction
- **Buzzer**: For audio feedback

## Software Components
- **Development Platform**: Arduino IDE with ESP32 board package installed
- **Libraries Used**:
  - `Adafruit_GFX` & `Adafruit_SSD1306`: OLED display control
  - `Preferences`: Non-volatile storage for calibration & PID values
  - `SparkFun_TB6612`: Motor control

## Project Structure
- **drive.ino**: Implements PID control and motor adjustments based on sensor input.
- **lft-mm.ino**: Initializes hardware components and executes the main event loop.
- **sensor.h**: Handles sensor calibration and position calculations.
- **phoenixUI.h**: Manages the OLED display user interface.

## Setup Instructions
### Hardware Setup
1. Connect the sensors, motors, motor driver, OLED display, and buttons to the ESP32 as per the pin definitions in the code.
2. Ensure the motor driver is correctly wired to the ESP32 and motors.
3. Connect the OLED display to the ESP32’s I2C pins.

### Software Setup
1. Install the required libraries (`Adafruit_GFX`, `Adafruit_SSD1306`, `Preferences`, `SparkFun_TB6612`) in Arduino IDE.
2. Upload the code to the ESP32.
3. Use the OLED display interface to navigate menus and configure settings.

### Calibration
1. Place the robot on the track.
2. Follow the on-screen instructions to calibrate the sensors.
3. The robot automatically adjusts sensor thresholds for optimal detection.

### Running the Robot
1. Start the robot via the OLED display menu.
2. The robot will adjust speed and direction based on sensor readings.
3. Monitor performance and adjust PID values as needed.

## Usage
- **Main Menu**: Options to calibrate sensors, set PID values, inspect sensor readings, and control motors.
- **PID Tuning**: Adjust values via the user interface for optimal performance.
- **Motor Testing**: Individual motor control and diagnostics via the OLED display.

## Contributing
Contributions are welcome! If you have suggestions, bug reports, or feature requests, feel free to open an issue or submit a pull request.

## License
This project is open-source and available under the MIT License. You are free to use, modify, and distribute the code following the license terms.

## Acknowledgments
- **Zisan (CSE 22-3)**: Developed the PhoenixUI and contributed to the overall project.
- **SparkFun**: TB6612FNG motor driver library.
- **Adafruit**: GFX and SSD1306 libraries for OLED display.

## Contact
For questions or further information, please contact the project maintainer.

---
This README provides a clear, well-structured overview of the Line Follower Robot project. Its modular design makes it an excellent starting point for robotics and embedded systems enthusiasts.
