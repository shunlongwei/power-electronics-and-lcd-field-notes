# Industrial TFT-LCD Interface & Backlight Pre-Power Checklist

Pre-installation checks when replacing legacy industrial TFT-LCD panels in CNC controllers, HMIs, and medical instrumentation.

## 1. Signal Interface & Pinout Alignment
- Confirm interface standard (`LVDS 6-bit/8-bit`, `TTL`, or `eDP`) and channel count (`1ch` vs `2ch`).
- Verify `VCC` logic supply (`3.3V` vs `5.0V`) against the controller board—never assume drop-in pin compatibility across different revisions without checking the pin table.

## 2. Backlight Driver Compatibility
- Identify backlight architecture: **LED** (constant-current driver, check `V_LED` string voltage and `PWM` dimming polarity) vs legacy **CCFL** (high-voltage AC inverter).
- Inspect FFC/FPC and wire-to-board connectors for bent pins or latch fatigue.

## 3. Optical & Mechanical Fit
- Check active area, mounting ear positions, and panel thickness tolerance before fastening the bezel to avoid localized pressure spots.

---
**Extended Reading:** [Industrial Display & Power Semiconductor Reference](https://www.slw-ele.com/)
