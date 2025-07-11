# Bambu Lab P1S - Enhanced G-code Start & End Scripts
## Verified on P1S with AMS

---

## Overview

These G-code scripts serve as better replacements for the default start and end routines found in Bambu Studio. The scripts aim to:

1. Optimize print setup and shutdown sequences.
2. Maintain nozzle and bed cleanliness throughout print cycles.
3. Improve the speed and reliability of AMS filament handling.
4. Ensure mesh bed integrity through verification and fallback leveling.

---

## Download

| Routine        | Description                         | Link                                                                 |
|----------------|-------------------------------------|----------------------------------------------------------------------|
| Start G-code   | Streamlined startup sequence        | [Copy the Script](https://github.com/Justagwas/P1S-GCODE/blob/main/start%20G-code) |
| End G-code     | Controlled shutdown and cooldown    | [Copy the Script](https://github.com/Justagwas/P1S-GCODE/blob/main/end%20G-code)   |

> [!TIP]
> Before replacing the default G-code scripts in Bambu Studio, **create a backup** of your existing start and end sequences.  
> You can do this by copying them into a plain text file or saving a preset within the Studio interface.

---

## Script Summary

### Start G-code

1. **System reset and initial fan setup** using `M710`, `M17`, and related configuration commands (`M220`, `M221`).
2. **Concurrent heating and motion prep**, reducing pre-print latency.
3. **Clean homing** via `G28`, ensuring predictable origin alignment.
4. **AMS initialization and filament verification** using `M620.*`, `M621.*`.
5. **Purging and wiping** at full extrusion temperature to prevent initial layer defects.
6. **Bed mesh validation** using `G29.1`. If significant deviation is detected, the system triggers a full mesh leveling routine.

### End G-code

1. **Spiral Z-axis retraction** to remove the nozzle cleanly from the print without dragging.
2. **Post-print purge and wipe**, preventing residue buildup during cool-down.
3. **Fan ramp-down sequence**, mitigating the risk of heat creep into the cold zone.
4. **Chamber ventilation sequence** lasting approximately three minutes.
5. **Motor current reduction and toolhead parking** to protect electronics and position safely for the next print.

---

## Key Advantages

- **Reduced time-to-print** through efficient thermal and mechanical initialization.
- **Improved part and print quality** due to reduced oozing and controlled nozzle behavior.
- **Enhanced reliability of AMS loading/unloading**, minimizing jams and retries.
- **Autonomous mesh verification**, avoiding unnecessary re-leveling and false starts.

---

## Integration & Testing Procedure

1. Open **Bambu Studio** or other, navigate to **Machine G-code**.
2. Replace the **Start** and **End G-code** sections with the contents of the corresponding script files.
3. Save the configuration and run a calibration or small test print.
4. Observe the AMS behavior, wipe pattern, bed leveling response, and end-of-print motions.
5. Adjust only if necessary, particularly Z-offset values or purge volumes for specialty materials.

---

## Technical Considerations

> [!WARNING]
> Do **not** increase the Z-offset beyond the default value without careful testing. Excessive positive offsets may prevent proper adhesion; excessive negative values may damage the bed surface or nozzle.

> [!WARNING]
> Commands such as `M17` (motor enable) and `M220`/`M221` (multipliers) directly affect motion behavior. Incorrect usage may result in stepper instability or clogs.

- These scripts are tailored to the **P1S with AMS**, though they should operate without issue on the **P1S** and **X1C** without AMS, provided AMS-specific calls are automatically uncalled.

---

## Contributing

Contributions are welcome. If you have refinements, compatibility notes, or verified performance changes:

1. Fork the repository.
2. Modify the relevant script(s).
3. Submit a pull request with clear documentation of the changes.
4. Open an issue if you encounter reproducible problems or firmware-specific quirks.
