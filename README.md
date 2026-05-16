# bigslinger
Mainsail and Klipper Configuration files for Bigslinger in the SAU Makerspace. See README for Specs and Config

# How to Use Printer
1. Install Tailscale (http://www.tailscale.com)
2. Login w/ SAU email to Join SAU Tailnet
3. In a web browser navigate to 100.123.100.114
4. Home All Axes
5. Adjust Z-Offset
Making your gcode:
1. In Prusa Slicer, Go to file > Import > Import Config Bundle
2. Upload "Bigslinger_prusa_config_bundle.ini"
3. Use these slicer settings as a baseline and make adjustments as you see fit (do not change speed settings)
4. Under printer, click "Add Physical Printer"
5. Under Host Type Choose "Klipper (via Moonraker)"
6. Under Hostname, IP, or URL: 100.123.100.114
7. Leave all other fields blank and click ok (feel free to change the name at the top)
8. Once sliced, click the "G" in the corner to upload and print

* You can also manually upload files in the web interface (100.123.100.114:80) and select existing files under gcode

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

%%%% See Pinout for locations %%%%

# Useful Links:

Klipper Gcodes: https://www.klipper3d.org/G-Codes.html#force_move_1

#Licensing
This Project in its entirety is Licensed strictly Under GPL 3.0, The licensor reserves the right to issue other licenses separate from the standard GPL 3.0 License. See http://www.gnu.org/licenses/gpl-3.0.en.html#license-text for full details.
