# Smart Street Light System

## Overview

This repository contains the code and documentation for a Smart Street Light System developed in November 2018. The project enhances traditional street lights using Internet of Things (IoT) principles with an Arduino-based system. The system incorporates various hardware components, including an Arduino board, relays, ultrasonic sensors, jumper wires, bulbs, etc.

## Hardware Dependencies

The project relies on the following hardware components:

1. Arduino Board
2. Relays
3. Ultrasonic Sensors
4. Jumper Wires (make sure to get all three kinds: M-M, F-F, M-F)
5. Bulbs (or equivalent light sources)
6. LDR

## Connection Setup

Connect the hardware components based on the following pin assignments in the provided Arduino code:

- **LEDs:**
  - `led` (Pin 3)
  - `led1` (Pin 10)
  - `led2` (Pin 5)
  - `led3` (Pin 6)
  - `led4` (Pin 9)

- **Analog Sensors:**
  - `ldr` (Analog Pin A0)
  - `ir` (Analog Pin A1)
  - `ir1` (Analog Pin A2)
  - `ir2` (Analog Pin A3)
  - `ir3` (Analog Pin A4)
  - `ir4` (Analog Pin A5)

## Running the Code

1. Install the Arduino IDE on your computer.
2. Connect the Arduino board to your computer using a USB cable.
3. Open the Arduino IDE and copy the provided code into a new sketch.
4. Verify and upload the sketch to the Arduino board.

## Operation

The Smart Street Light System operates based on the following logic:

- If the light sensor (`ldr`) detects low light conditions (<= 300), the system activates all LEDs with varying intensities based on analog sensor readings.
- Each LED is controlled by an Ultrasonic sensor. If an obstacle is detected (analog reading < 500), the corresponding LED remains on; otherwise, a delay of 1000 milliseconds is introduced.
- When light conditions improve, all LEDs are turned off.

## Additional Notes

- Adjust the threshold values in the code to fine-tune the sensitivity of the light and US sensors.
- Ensure proper power supply and connections for reliable operation.

Feel free to modify the code and documentation according to your specific requirements. For any questions or issues, please refer to the [Issues] Section
