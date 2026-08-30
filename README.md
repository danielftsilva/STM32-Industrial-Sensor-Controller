# STM32-RF-USB-Gateway

## Overview

The **STM32-RF-USB-Gateway** is an embedded hardware platform designed to provide a USB interface between a computer and a **2.4 GHz nRF24L01P wireless transceiver**.

The objective of the project is to develop a compact USB-connected wireless gateway based on the **STM32L432KBU6**, allowing the microcontroller to interface with a host computer through USB while controlling the nRF24L01P through SPI.

The design incorporates dedicated power regulation, USB ESD protection, a 16 MHz crystal oscillator, an RF impedance-matching network, a 50 Ω controlled-impedance antenna path, an external SMA connector, and an SWD programming/debugging interface.

## Main Components

- **STMicroelectronics STM32L432KBU6** — main microcontroller with USB Full-Speed and SPI interfaces
- **Nordic Semiconductor nRF24L01P** — 2.4 GHz wireless transceiver
- **Torex XC6206P332MR-G** — 3.3 V LDO regulator
- **STMicroelectronics USBLC6-2SC6** — USB ESD protection
- **Samtec SMA-J-P-H-ST-EM3** — 50 Ω SMA antenna connector
- **FTSH-105-01-F-D** — SWD programming/debugging connector
- **16 MHz crystal** — nRF24L01P reference clock

## Project Status

**Work in Progress**

- Project started: **2022**
- Objective: Exploration of the **STM32L432KBU6** and its capabilities
- Schematic: **Existing gateway architecture finalized**
- PCB layout: **In progress**
- Firmware: **Started, but not completed**
- Prototype: **Not yet completed**

The current repository documents the developed USB-to-2.4 GHz RF gateway hardware. The PCB layout is being expanded before finalization to incorporate additional functionality.

The next revision is planned to include:

- **OLED display** for local system and RF status
- **User reset button**
- **I²C environmental sensor** for temperature, humidity, pressure, etc.
- **Additional test points** for hardware debugging and validation

These additions are the reason the current PCB layout remains unfinished. The existing gateway schematic is finalized, while the new features still need to be incorporated into the schematic and PCB before the hardware can be considered complete.

---
