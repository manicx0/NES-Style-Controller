# NES-Style Modernized Wireless Controller

A custom-built rectangular controller inspired by the NES 004 form factor, 
featuring dual analog sticks, a built-in OLED settings display, and 
dual-radio wireless connectivity (BLE/WiFi via ESP32 + 2.4GHz NRF24L01 link).

![Controller Photo](docs/images/controller-hero.jpg)

## Features

- 🎮 Dual analog joysticks (no L1/L2/R1/R2/R3/L3 — clean rectangular NES-style layout)
- 📟 1.3" OLED display for in-controller settings (volume, connection mode, battery %)
- 📡 Dual wireless: Bluetooth/WiFi (ESP32) + dedicated 2.4GHz link (NRF24L01+PA+LNA)
- 🔋 Rechargeable LiPo battery with USB-C charging (TP4056)
- 🔧 Fully open-source hardware — schematics, PCB layout, and firmware included

## Status

🚧 **Work in progress** — currently in [schematic / PCB layout / firmware] stage.

## Hardware

| Component | Part |
|---|---|
| MCU | ESP32-WROOM-32 (DevKit V1, 30-pin) |
| Wireless | NRF24L01+PA+LNA |
| Display | SSD1306 OLED, 1.3", 128x64, I2C |
| GPIO Expansion | MCP23017 (I2C) |
| Regulator | MCP1700-3302E (3.3V LDO) |
| Battery | 3.7V LiPo, JST-PH2.0 |
| Charger | TP4056, USB-C, dual output |
