# Bambu Lab P1S - Enhanced Start & End G-code
### Verified on P1S with AMS - Last Tested on 2025/11/24

### Recommended for use with [Orca Slicer](https://github.com/SoftFever/OrcaSlicer).

*Works with ANY.

---

## Download / Copy

| G-Code Type      | Description                  | Script Link                                                                 | RAW Link                                                                 |
|--------------|------------------------------|-----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Start G-Code | Optimized startup sequence   | [View Script](https://github.com/Justagwas/P1S-GCODE/blob/main/start%20G-code) | [Raw File](https://github.com/Justagwas/P1S-GCODE/raw/refs/heads/main/start%20G-code) |
| End G-Code   | Controlled shutdown/cooldown | [View Script](https://github.com/Justagwas/P1S-GCODE/blob/main/end%20G-code)   | [Raw File](https://github.com/Justagwas/P1S-GCODE/raw/refs/heads/main/end%20G-code)   |

> [!TIP]  
> Back up your current start and end G-code before replacing them in your Slicer.

---

## Overview

These G-Code scripts replace the default Start and End routines in your Slicer. 

They are designed to:

- Make print setup and shutdown faster.
- Keep the nozzle and bed clean between prints.
- Improve AMS filament handling reliability.
- Verify mesh bed integrity and trigger leveling if needed.
- Work straight out of the box (Just copy and paste!) without extra setup.

---

## Script Summary

### Start G-code
- Resets system state, motor currents, and fan defaults.  
- Enables runout detection and resonance compensation.
- Heats bed and nozzle in parallel while preparing motion.
- Homes all axes.
- Initializes AMS, reloads, and verifies filament.
- Purges and wipes at extrusion temperature to ensure a clean nozzle.
- Cools slightly, then validates mesh bed, if selected, and enables compensation.
- Draws a purge line at print temperature before starting the job.

### End G-code
- Clears motion buffer and resets motor/acceleration settings.
- Performs a small retract and spiral lift to safely move away from the print.
- Parks at purge area, extrudes/purges, and runs a wipe routine to leave nozzle clean.
- Gradually cools nozzle to prevent ooze and stringing, then unloads filament back into AMS.
- Cools down and performs a final nozzle wipe with ABL temporarily disabled.
- Re‑enables ABL and resonance suppression, and safely stops timelapse recording if active.
- Raises Z and moves toolhead to a rear park position.
- Runs staged fan cooldown (high → medium → off) to manage chamber and hotend ventilation and temps.
- Reduces motor currents for idle state and clears action flags.

---

## Benefits

- Faster time-to-print through efficient prep.
- Cleaner first layers and reduced oozing.
- More reliable AMS loading/unloading.
- Only the necessities and safeguards!

---

## Integration & Testing

1. Open **Your Slicer** -> **Machine G-Code**.
2. Replace the **Start G-Code** and **End G-code** sections with these scripts.
3. Save and run a calibration or small test print.
4. Observe AMS behavior, wipe pattern, bed leveling, printing, and shutdown.
5. Adjust only if needed.

---

## Technical Notes

> [!WARNING]  
> Adjust Z-offset carefully. Too high = poor adhesion. Too low = risk of nozzle/bed damage.

- The default values are {-0.02} or {0.00}. Recommended range is from {-0.04} to {0.04}, although I highly advise against touching this value if not needed.

> [!WARNING]  
> Commands like `M17`, `M220`, and `M221` directly affect motion. Incorrect values may cause instability or clogs.

- Scripts are tailored for **P1S with AMS**, but also work on **P1S** and **X1C** without AMS (AMS-specific calls are skipped automatically).

---

## Contributing

Contributions are welcome:
1. Fork the repository.
2. Modify the script(s).
3. Submit a pull request with clear documentation.
4. Open an issue for reproducible problems or firmware quirks.

---

## Contact

For questions or feedback, reach out at:  
[contact@justagwas.com](mailto:contact@justagwas.com)
