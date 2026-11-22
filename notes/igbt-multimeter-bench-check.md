# IGBT Module Offline Multimeter Bench Check

Quick static verification steps before installing an IGBT module into a motor drive or inverter stage.

## 1. Safety & ESD Preparation
- Discharge DC-link capacitors completely and isolate the module from the busbar.
- Use an ESD wrist strap or grounded mat before touching gate (`G`) and auxiliary emitter (`E_aux`) pins.

## 2. Gate-Emitter (`G-E`) Integrity
- Set multimeter to resistance (`Ω` / `MΩ`).
- Measure between Gate and Emitter: a healthy insulated gate should read open circuit (`OL` or `>10 MΩ`, unless an internal gate-emitter resistor is specified in the datasheet).
- Shorted or low-resistance `G-E` (<100 kΩ without internal bleeder) indicates gate oxide breakdown.

## 3. Collector-Emitter (`C-E`) & Freewheeling Diode Check
- Switch multimeter to Diode mode.
- Forward bias across the anti-parallel freewheeling diode (`E → C` for N-channel IGBT): typical forward voltage drop `Vf` is `0.35V – 0.65V` at room temperature.
- Reverse direction (`C → E`) with `G` shorted to `E`: must read `OL` (blocking).

## 4. Baseplate Insulation
- Verify isolation between all power terminals (`C`, `E`, `AC`) and the copper/AlSiC mounting baseplate before torquing onto the heatsink.

---
**Extended Reading:** [A Practical Guide to Testing IGBT Modules with a Multimeter](https://www.slw-ele.com/a-practical-guide-to-testing-igbt-modules-with-a-multimeter.html)
