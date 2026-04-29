# Pico W Keypad-to-LED Controller

Firmware for a Raspberry Pi Pico W that reads a 4x4 matrix keypad and drives 12 individual LEDs based on key presses.

## Project Structure

- `src/main.cpp` - original application logic (preserved).
- `include/` - reserved for future headers.
- `docs/wiring.md` - wiring reference and GPIO map.
- `docs/architecture.md` - module/logic walkthrough.
- `diagram.json` - Wokwi circuit definition.
- `CMakeLists.txt` - repository root build metadata.

## Features

- 4x4 keypad scanning using `Keypad` library.
- Direct LED control for keys `1..8` and `A..D`.
- Group control:
  - `9`: turn ON LEDs 1..8
  - `0`: turn OFF LEDs 1..8
  - `*`: turn ON LEDs A..D
  - `#`: turn OFF LEDs A..D
- Non-blocking polling loop with `delay(10)`.

## Hardware Components

- 1x Raspberry Pi Pico / Pico W (`wokwi-pi-pico` in diagram)
- 1x 4x4 membrane keypad
- 12x LEDs (8 blue + 4 red in diagram)
- 12x 220 ohm resistors (LED current limiting)
- 4x 1k ohm resistors (keypad row pull-up network)
- Jumper wires and common GND rail

## Pin Usage Summary

See full table in [`docs/wiring.md`](docs/wiring.md).

- Keypad rows: GP26, GP22, GP21, GP20
- Keypad cols: GP19, GP18, GP17, GP16
- LED outputs: GP11, GP10, GP9, GP8, GP7, GP6, GP5, GP4, GP3, GP2, GP28, GP27

## Running in Wokwi

1. Create/import a new RP2040 project in Wokwi.
2. Replace `diagram.json` with this repo's `diagram.json`.
3. Use `src/main.cpp` as sketch firmware source.
4. Add `Keypad` library from Wokwi/Arduino Library Manager.
5. Start simulation and press keypad buttons.

## Running on Real Hardware (Pico W)

This firmware is Arduino-style C++.

1. Install Arduino IDE + RP2040 Arduino core.
2. Select board: **Raspberry Pi Pico W**.
3. Install library: **Keypad** by Mark Stanley & Alexander Brevig.
4. Copy `src/main.cpp` into your sketch (or include as project source).
5. Wire exactly as documented in `docs/wiring.md`.
6. Upload and open serial monitor if needed.

## Wi-Fi Notes

- Current firmware does **not** use Wi-Fi functions.
- No SSID/password is required.
- If Wi-Fi is added later, keep credentials in a separate local config file and never commit secrets.

