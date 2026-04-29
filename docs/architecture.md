# Firmware Architecture

## Overview

The project is a single-file Arduino-style firmware that scans a keypad and updates GPIO outputs for LEDs.

## File Layout

- `src/main.cpp`
  - Pin and keypad map declarations.
  - `setup()` initializes all LED GPIO as outputs and default LOW.
  - `loop()` polls keypad and runs a `switch` dispatch for each supported key.

## Core Data Structures

- `keys[4][4]`: keypad character matrix.
- `ledPins[12]`: LED output mapping in logical order.
- `rowPins[4]` and `colPins[4]`: matrix scan pin assignment.
- `Keypad keypad`: keypad driver instance.

## Control Flow

1. Boot: configure LED pins as output and OFF.
2. Runtime loop:
   - Read key: `keypad.getKey()`.
   - If key is valid (`!= NO_KEY`), execute key handler:
     - Single-key LED ON (`1..8`, `A..D`)
     - Group ON/OFF operations (`9`, `0`, `*`, `#`)
   - Delay 10 ms.

## Design Notes

- Program behavior is intentionally preserved from the provided source.
- No abstraction layers were added to avoid changing timing/logic semantics.
- Wi-Fi peripherals of Pico W are not used by current firmware.

