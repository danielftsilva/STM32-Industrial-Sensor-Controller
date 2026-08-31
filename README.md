# STM32-RF-USB-Gateway

## Overview

The **STM32-RF-USB-Gateway** is an embedded hardware platform I developed to provide a USB interface between a computer and a **2.4 GHz nRF24L01P wireless transceiver**.

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

### STM32 Peripheral Assignment

The STM32L432KBU6 was configured as the central controller of the gateway, with its peripherals and GPIOs assigned to the USB, nRF24L01P, SWD, and status interfaces.

<p align="center">
  <img src="docs/images/stm32-pinout.png" width="600">
</p>

<p align="center">
  <em>STM32L432KBU6 pin assignment used in the design</em>
</p>

## Project Status

**Work in Progress**

- Project started: **2022**
- Objective: Exploration of the **STM32L432KBU6** and its capabilities
- Schematic: **Existing gateway architecture finalized**
- PCB layout: **In progress**
- Firmware: **Started, but not completed**
- Prototype: **Not yet completed**

The current repository documents the developed USB-to-2.4 GHz RF gateway hardware. The PCB layout is being expanded before finalization to incorporate additional functionality.

## PCB Design

The PCB layout was developed from the finalized schematic, with dedicated areas for the USB interface, power regulation, STM32, nRF24L01P, RF matching network, SMA antenna interface, and SWD connector.

<p align="center">
  <img src="docs/images/pcb-layout-overview.png" width="900">
</p>

<p align="center">
  <em>Current PCB layout</em>
</p>

The RF section was designed as a dedicated 50 Ω controlled-impedance interface between the nRF24L01P matching network and the external SMA connector.

<p align="center">
  <img src="docs/images/pcb-rf-section.png" width="900">
</p>

<p align="center">
  <em>2.4 GHz RF matching network, controlled-impedance transmission line and SMA interface</em>
</p>

## Planned Expansion

The next revision is planned to include:

- **OLED display** for local system and RF status
- **User reset button**
- **I²C environmental sensor** for temperature, humidity, pressure, etc.
- **Additional test points** for hardware debugging and validation

These additions are the reason the current PCB layout remains unfinished. The existing gateway schematic is finalized, while the new features still need to be incorporated into the schematic and PCB before the hardware can be considered complete.
