# Wiring and GPIO Mapping (Raspberry Pi Pico W)

## Assumptions

- Mapping is derived from the provided source arrays and Wokwi `connections` data.
- Board in diagram is `wokwi-pi-pico`; project target is Pico W. GPIO mapping is equivalent for used pins.

## Components List

- Pico/Pico W: 1
- 4x4 Keypad: 1
- LEDs: 12
- 220 ohm resistors: 12 (one per LED)
- 1k ohm resistors: 4 (row pull-up chain to 3V3)

## Keypad Wiring

| Keypad Pin | Pico GPIO |
|---|---|
| R1 | GP26 |
| R2 | GP22 |
| R3 | GP21 |
| R4 | GP20 |
| C1 | GP19 |
| C2 | GP18 |
| C3 | GP17 |
| C4 | GP16 |

Additional row pull-ups in diagram:
- R1/R2/R3/R4 lines are tied through 1k network to 3V3.

## LED Wiring

All LED cathodes connect to GND. Each anode is connected to one GPIO through a 220 ohm resistor.

| Logical LED | Trigger key | Pico GPIO |
|---|---:|---:|
| LED1 | 1 | GP11 |
| LED2 | 2 | GP10 |
| LED3 | 3 | GP9 |
| LED4 | 4 | GP8 |
| LED5 | 5 | GP7 |
| LED6 | 6 | GP6 |
| LED7 | 7 | GP5 |
| LED8 | 8 | GP4 |
| LED9 | A | GP3 |
| LED10 | B | GP2 |
| LED11 | C | GP28 |
| LED12 | D | GP27 |

## Behavior Reference

- Key `9` sets LED1..LED8 HIGH.
- Key `0` sets LED1..LED8 LOW.
- Key `*` sets LED9..LED12 HIGH.
- Key `#` sets LED9..LED12 LOW.

