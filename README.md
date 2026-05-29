# EVBox G2 ESPHome Controller

ESPHome-based replacement/emulation controller for an EVBox G2 charge point using an M5Stack AtomS3 Lite and ATOMIC RS485 Base.

## Features

- EVBox G2 CP/modem emulation
- Remote start via command 31
- Delayed G2 start via 6A state 07 → command 6B
- Remote stop via command 32
- Home Assistant controls
- Charging modes:
  - Off
  - Manual
  - Auto
  - Solar Surplus
- Solar surplus feedback control using grid power
- Session tracking:
  - session id
  - start time
  - end time
  - duration
  - energy
  - estimated solar surplus share

## Hardware

- M5Stack AtomS3 Lite
- ATOMIC RS485 Base
- EVBox G2 charge point

This project provides RS485 CP/modem emulation for selected EVBox G2-like charge points, with remote start/stop, dynamic current limiting, solar-surplus charging and charging-session tracking.

> Experimental project. Not affiliated with or endorsed by EVBox.

## Warning

This project interacts with EV charging hardware and RS485 control signals. Use at your own risk. Incorrect wiring or configuration may damage equipment or create unsafe charging behavior.

## Safety warning

This project is experimental. It is not an officially supported EVBox integration.  
Do not use this unless you understand EV charging safety, electrical installation limits, circuit protection, phase configuration, and local regulations.

The current limit sent by this controller must never exceed what your installation, cable, breaker, EVSE and vehicle can safely support.

This project interacts with EV charging hardware and RS485 control signals.

Use at your own risk. Incorrect wiring, configuration or current limits may damage equipment or create unsafe charging behavior. Never configure current limits above what your installation, breaker, cable, EVSE and vehicle can safely support.

## Acknowledgements

This project builds on the work and published research of others in the EVBox and smart-charging community.

Special thanks to:

- **Maarten Tromp** for his extensive EVBox protocol documentation and reverse-engineering work on the internal EVBox Max communication protocol. His documentation was an important reference for understanding the RS-485 protocol, frame structure, addressing and command behavior.
- **Harm Otten** for his work and write-up on smart charging at home, including practical concepts around using EV charging in a home energy-management context.

Their work helped make this project possible.

References:

- Maarten Tromp — EVBox protocol documentation: https://www.geekabit.nl/projects/managed-ev-charger-to-stand-alone/protocol/
- Harm Otten — Smart charging at home, and more: https://olino.org/blog/us/articles/2019/07/17/smart-charging-at-home-and-more/
