cmake_minimum_required(VERSION 3.13)
project(pico_w_keypad_led C CXX)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# NOTE: This repository keeps the original Arduino-style firmware logic in src/main.cpp.
# Build with an Arduino-compatible RP2040 core (e.g., Earle Philhower) in Arduino IDE or PlatformIO.
# Pico SDK CMake integration is intentionally not implemented to avoid altering runtime behavior.
