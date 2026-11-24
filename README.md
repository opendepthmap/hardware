# OpenDepthMap Hardware & Firmware

Open-source hardware designs, bills of materials, and embedded firmware for the OpenDepthMap ecosystem:

- **Phase 2:** DIY Autonomous Surface Survey Buoy for nearshore and inland bathymetric logging.
- **Phase 3:** Tethered Spool Puck and Diver Hand/Wrist Situational Awareness Receiver.

**Status:** Early design phase. Mechanical CAD files, schematics, BOMs, and firmware targets will be published here as Phase 2 and Phase 3 milestones progress.

## Repository Structure

```text
hardware/
├── cad/                                # Enclosures, mounts, sealing geometry, and STL files
└── firmware/
    ├── phase2-buoy-esp32s3/            # Surface survey buoy firmware
    ├── phase3-spool-esp32c3/           # Tethered spool puck buffer & RS-485 firmware
    └── phase3-hand-receiver-pi/        # Diver wrist receiver software & safe-mode watchdog
```

## Licensing

- **Hardware Designs (CAD, STL, Schematics, BOMs, Assembly Guides):** CERN Open Hardware Licence Version 2 - Permissive (`CERN-OHL-P-2.0`).
- **Embedded Firmware:** MIT License (`MIT`).

## Safety & Non-Navigational Disclaimer

Supplemental situational awareness and bathymetric reference tool only. Never replaces a primary dive computer, analog backup compass, physical reel guideline, or official NOAA/IHO nautical charts.
