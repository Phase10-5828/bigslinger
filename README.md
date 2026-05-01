# bigslinger
Mainsail and Klipper Configuration files for Bigslinger in the SAU Makerspace. See README for Specs and Config

# Specs
BigTreeTech Octopus V1.1
  - Load klipper.firmware onto microSD card
Motors X & Z:
  - Nema 17
  - TMC2209
  - UART
Motor Y:
  - Nema 23
  - TNC5160T Plus
  - SPI
Raspberry Pi 4(4GB) - Mainsale OS
  - See Mainsale Branch for Config and setup
BIQU H2 V2S Extruder
24 V PSU 250-350 W

# Config
 -- Exhaust and power are considered to be the back side of the printer for orientation.
Motor0 - X-Axis
 - Motors 0-2 Use UART jumper config on Octopus
Motor1 - Extruder
Motor 2_1 Z-Axis (Left of Gantry)
Motor 2_2 Z-Axis (Right of Gantry)
  - Motors work in Tandem, controlled by one stepper driver
Motor 7 - Y-Axis
  - Separate stepper driver mounted beside Octopus
  - Jumper set to SPI config on Octopus

Fan0 - Extruder
  - PWM Controlled
Fan5 - Case Fan
  - PWM Controlled
  - Set to Always-on
Fan6/Fan7 - Case Fans
  - Always-on
  - CANNOT be configured

HE0+- - Hotend Plugs

Endstops -- Plug into PG#/GND DO NOT PLUG INTO VCC/3V3
J27 - Endstop X
J29 - Endstop Y
J31 - Endstop Z

J45 - Thermistor

See Pinout for locations
