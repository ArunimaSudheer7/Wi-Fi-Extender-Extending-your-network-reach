# Wi-Fi-Extender-Extending-your-network-reach

## Overview
This mini-project uses an ESP32 to extend the range of an existing Wi-Fi network using the open-source NAT Router firmware. The ESP32 connects to the home router as a client and then creates a new AP to re-broadcast the connection.

## Features
- Extends Wi-Fi into low-signal areas
- Low cost and customizable
- Uses ESP32 NAT Router firmware (open-source)

## Hardware Required
- ESP32 development board (e.g., ESP32 DevKit)
- Micro-USB cable
- PC (Windows recommended for flashing tools)
- Optional: 5V power adapter or power bank

## Software / Tools
- ESP Flash Download Tool (Espressif)
- ESP32 NAT Router firmware (e.g. martin-ger/esp_wifi_repeater)
- Web browser to access 192.168.4.1 for configuration

## Build / Setup Steps
1. Download the ESP Flash Download Tool and the NAT Router firmware (from the firmware GitHub).
2. Connect the ESP32 to your PC via USB.
3. Open the Flash Download Tool:
   - Select chip: ESP32
   - Load binaries:
     - `bootloader.bin` at `0x1000`
     - `firmware.bin` at `0x10000`
     - `partitions.bin` at `0x8000`
   - Set baud rate to **576000**
   - Press the ESP32 boot button, click **Start** to flash.
4. After flashing, the device will broadcast an SSID like `ESP32_NAT_Router`.
5. Connect to that SSID with a phone/PC and visit `http://192.168.4.1`.
6. Under **STA Settings**, enter your home Wi-Fi SSID and password.
7. Under **AP Settings**, choose a new SSID/password for the extender.
8. Save and restart the ESP32. Devices connecting to the extender should now have internet via NAT.

## Files in repository
- `docs/Wi-Fi extender.pptx` — Presentation with project overview and cost analysis.
- `README.md` — This file.
- `.gitignore` — Common ignores for development files.

## Contributors
- Nandana Shibu
- Anusree Pradeep
- Arunima Sudheer
- Bhadra J R
- Gopika S Dhilip
- Sandhya M

## References
- ESP32 NAT Router firmware (GitHub)
- Tutorials & videos linked in the presentation
