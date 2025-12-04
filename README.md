# PMW3389 Breakout Board

A compact breakout board for the PMW3389 optical mouse sensor, designed for easy integration into custom keyboards, trackballs, and pointing devices.

This design is a complete rebuild from the ogen open source design, with significant improvements including:
- Ferrite beads for enhanced EMI hardening
- Better filtering capacitors for improved stability and noise rejection
- Optimized component placement for reliability

![PMW3389 Breakout Board](3389_JST-SH.png)

## Features

- **Compact Design**: Small form factor optimized for integration into custom projects
- **JST-SH Connector**: Easy plug-and-play connectivity with common cable assemblies
- **Standard SPI Pinout**: Compatible with most microcontrollers and development boards
- **Complete Filtering**: Onboard capacitors for stable sensor operation
- **Pre-configured I2C Pull-ups**: Ready to use with I2C-compatible controllers
- **Clear Labeling**: All pins clearly marked for easy identification

## Specifications

- **Sensor**: PMW3389DM-T3QU
- **Resolution**: Up to 16,000 CPI/DPI
- **Tracking Speed**: Up to 400 IPS (inches per second)
- **Acceleration**: Up to 50g
- **Power Supply**: 3.3V (±10%)
- **Interface**: SPI
- **Operating Temperature**: -40°C to +85°C

## Pin Assignments

### JST-SH Connector (Left side)
1. VCC (3.3V)
2. GND
3. MOSI
4. MISO
5. SCK
6. CS

### SPI Header (Right side)
- **CS** - Chip Select
- **GND** - Ground
- **3v3** - 3.3V Power Supply
- **MISO** - Master In Slave Out
- **MOSI** - Master Out Slave In (also labeled as MOSI on some variants)
- **SCK** - Serial Clock

## Assembly Instructions

### Required Components
- PMW3389 sensor (pre-installed on breakout board)
- Optical lens (usually included with sensor)

### Steps

1. **Remove Polyimide Dust Cover**
   - The sensor comes with a thin amber/brown protective film
   - **IMPORTANT:** Position the sensor vertically (upright) during removal
   - This prevents dust from entering the sensor holes
   - Carefully peel off using tweezers or a fingernail

2. **Install Optical Lens**
   - Place the lens directly over the sensor aperture
   - Ensure it sits flat and centered
   - The lens is held by friction - no adhesive needed
   - Keep the lens clean and free of fingerprints

3. **Connect to Controller**
   - Use either the JST-SH connector or SPI header pins
   - Ensure 3.3V power supply (NOT 5V)
   - Connect SPI lines according to your microcontroller pinout

## Electrical Specifications

- **Supply Voltage**: 3.0V to 3.6V (3.3V nominal)
- **Supply Current**: ~15mA typical
- **Logic Levels**: 3.3V CMOS
- **SPI Mode**: Mode 3 (CPOL=1, CPHA=1)
- **SPI Clock**: Up to 2MHz

## Design Files

This repository includes:
- KiCad schematic and PCB design files
- Gerber files for manufacturing
- Bill of Materials (BOM)
- Assembly guide documentation
- 3D model (STEP file)

## Manufacturing

The board is designed for easy fabrication with most PCB manufacturers:
- **PCB Thickness**: 1.6mm
- **Copper Weight**: 1oz
- **Surface Finish**: ENIG or HASL
- **Minimum Trace/Space**: 6mil/6mil
- **Minimum Drill**: 0.3mm

Recommended manufacturers: JLCPCB, PCBWay, OSH Park

## Important Notes

⚠️ **Warnings:**
- The sensor requires 3.3V power - DO NOT connect to 5V
- Always remove the polyimide film with the sensor positioned vertically to prevent dust from entering the sensor holes
- Avoid touching the sensor surface or lens with bare hands
- ESD sensitive - handle with appropriate precautions

💡 **Tips:**
- Keep the lens clean for optimal tracking performance
- Mount the sensor 2.5mm above the tracking surface for best results
- Use shielded cables for JST-SH connection to minimize EMI
- Add a small amount of kapton tape around the lens if needed to prevent light leaks

## Troubleshooting

**Sensor not responding:**
- Verify 3.3V power supply
- Check SPI connections
- Ensure polyimide film has been removed
- Verify lens is properly seated

**Poor tracking performance:**
- Clean the lens with a microfiber cloth
- Check the distance from the tracking surface (should be ~2.5mm)
- Verify CPI/DPI settings in firmware
- Ensure adequate lighting (the sensor has built-in LED)

**Erratic cursor movement:**
- Check for loose connections
- Verify SPI clock frequency (max 2MHz)
- Reduce cable length or add ferrite beads
- Check for EMI from nearby components

## License

This hardware design is licensed under the CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN-OHL-S v2).

**Key Requirements:**
- Attribution is required
- Non-commercial use encouraged
- **Production requires permission** - Please contact for licensing if you wish to manufacture these boards
- Modifications must be shared under the same license

See [LICENSE](LICENSE) for full details.

## Upcoming: Precision Trackball Mount

An improved trackball mount design will soon be introduced to **Cosmos** (keyboard generator at [www.ryanis.cool/cosmos](https://www.ryanis.cool/cosmos)). 

Features:
- 2-part design for precision assembly
- Captive ceramic ball bearings that rotate freely
- Precision trackball positioning
- High-quality resin construction

Available on the website in a couple of weeks.

## Support & Contact

For assistance, questions, or licensing inquiries:
- **Email:** thebigskree@gmail.com
- **Discord:** #Alakuu
- **YouTube:** [@skreellc](https://youtube.com/@skreellc)

## Contributing

Contributions are welcome! Please feel free to submit:
- Bug reports
- Feature requests
- Pull requests for improvements
- Documentation updates

For major changes or production inquiries, please contact first.

## Credits

- Board design: WainingForests (Skree LLC)
- Original inspiration: ogen open source design
- Improvements: EMI hardening with ferrite beads, enhanced filtering capacitors
- PMW3389 sensor: PixArt Imaging

## Related Projects

- [QMK Firmware](https://qmk.fm/) - Popular mechanical keyboard firmware with pointing device support
- [Cosmos Keyboard Generator](https://ryanis.cool/cosmos) - Modern keyboard design tool
- [Custom Keyboard Builds](https://www.reddit.com/r/MechanicalKeyboards/)

## Changelog

### v1.0 (Current)
- Initial release
- JST-SH and header pin options
- Optimized component placement
- Complete filtering and pull-up networks

---

**Note**: This is an open-source hardware project with attribution and share-alike requirements. PCB files and documentation are provided under the CERN-OHL-S v2 license. Production for commercial purposes requires permission from the designer.
