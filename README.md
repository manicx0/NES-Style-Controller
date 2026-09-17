### NES-Style Modern Controller — Component List & Wiring Overview

An SoC with built-in WiFi+Bluetooth handles wireless duty, with an optional dedicated 2.4GHz nRF radio for a low-latency "wired-like" mode — a common approach in hobby gamepad builds since no single chip natively does WiFi+BT+proprietary-nRF all at once.

### Component List

**Brain**

- Main MCU/SoC with built-in WiFi + Bluetooth (e.g. an ESP32-class chip) — handles button/stick polling, display driving, and wireless output
- Optional secondary 2.4GHz radio module (nRF24L01+ style) for a dedicated low-latency "nRF mode," wired to the MCU over SPI

**Input**

- 2x analog stick modules (dual-potentiometer + click-button type, PSP/Joy-Con style)
- D-pad (4-way cross, either 4 discrete tactile switches or a single 4/8-way rocker module)
- 4x face buttons (tactile switches)
- Start/Select buttons
- 1-2x dedicated "menu/mode" buttons for navigating the mini display's settings UI (can double up with Start/Select if you want to save parts)
- Tactile switch caps / keycaps for the above

**Display**

- Small SPI or I2C TFT/OLED display (roughly 0.9"–1.5" is typical for a corner status screen)

**Power**

- LiPo battery (single-cell, capacity to taste)
- Battery charge/protection module (handles USB-C charging + over-discharge protection)
- 3.3V voltage regulator (if your battery/charger output doesn't already give clean 3.3V)
- USB-C connector (charging + optional wired/data mode)
- Power slide switch

**Support**

- Pull-down (or pull-up) resistors for each button line, unless using MCU internal pull resistors
- Small decoupling capacitors near MCU and radio modules
- Status LED(s) (battery/pairing indicator — optional)
- Protoboard or custom PCB
- 3D-printed or laser-cut rectangular shell (NES-004 proportions, no shoulder-button cutouts)


## Acknowledgments / Inspiration

Design inspired by the NES 004 controller form factor.
