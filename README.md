
# Bluetooth-Controlled Motor Speed System

## Objective
Develop a system to control an electric motor using a PWM output signal. The motor speed (0-100%) is controlled via a smartphone application with Bluetooth connectivity. The system displays the motor speed on an LCD.

## Features
- Motor speed control through a smartphone via Bluetooth.
- PWM-based motor speed regulation.
- Real-time speed display on an LCD.
- Simple user interface for motor speed adjustment.

## Problem Description
The system uses:
- **C Programming Language**: For microcontroller programming.
- **PWM (Pulse Width Modulation)**: To regulate motor speed.
- **Bluetooth Connectivity**: To allow speed adjustments from a smartphone app.
- **LCD Display**: To show the current motor speed.

Key functionalities:
- Initialize peripherals (UART, I2C, GPIO, etc.).
- Handle motor speed input via Bluetooth.
- Dynamically adjust PWM duty cycles.
- Display motor speed on the LCD.

## Pseudocode
### Initialization
1. Initialize the watchdog timer.
2. Configure Bluetooth module for UART communication.
3. Set up the LCD display and motor control pins.

### Main Loop
1. Continuously check for Bluetooth input.
2. Parse PWM values from incoming messages.
3. Update motor status and speed display based on the PWM value.

### UART Interrupt
1. Receive and process incoming Bluetooth messages.
2. Update motor speed and display upon receiving valid input.

### Functions
- **Motor Control**: Turn the motor on or off based on the PWM value.
- **Display Update**: Display the current PWM value on the LCD.
- **Delay**: Implement a millisecond-level delay for timing control.

## Wiring Diagram
Ensure connections as per the project specifications:
- Bluetooth module connected to the microcontroller via UART.
- Motor control pins configured for PWM output.
- LCD connected using I2C.

## How to Run
1. Clone the repository.
2. Flash the provided code onto the microcontroller.
3. Pair the Bluetooth module with your smartphone.
4. Use the smartphone app to send PWM values (0–100).
5. Observe motor speed adjustments and real-time updates on the LCD.

## Example Code
```c
#include <msp430.h>
#include "LiquidCrystal_I2C.h"
// Full implementation in `main.c`
```

For detailed implementation, see [`main.c`](./main.c).

## Authors
This project was completed as part of the coursework for **Advanced Embedded Systems**.

---

Feel free to suggest improvements or report issues in the repository.
