# Bambu Lab P1S Modified G-code Scripts

**Download:**

* [Modified Start G-code]()
* [Modified End G-code]()

*These scripts have been tested on a Bambu Lab P1S equipped with AMS and perform as intended.*

---

## Purpose

These modified G-code scripts are intended to replace the standard scripts provided in Bambu Studio. 

They are designed to improve safety, cleanliness, and consistency during the start and end of every print. 

They are also faster and more optimised.

---

## Summary of Modifications

### Start G-code

* The initialization sequence has been simplified to remove legacy commands.
* Startup time has been reduced.
* Homing is performed in a clean and predictable manner using `G28`.
* AMS material loading includes short pauses to improve reliability.
* The nozzle is purged at a higher temperature and wiped in a controlled pattern to reduce clogs and contamination, preventing oozing.
* A stored bed mesh is loaded and verified automatically. If the measured points deviate beyond limits, a full bed re-leveling is performed.

---

### End G-code

* The nozzle lifts in a spiral pattern to clear the print safely without leaving residue.
* Additional purge and wipe steps are performed to minimize stringing and oozing.
* The cooling process uses a controlled fan ramp-down to prevent heat from creeping into the extruder.
* Chamber ventilation sequences, lasting ~3minutes total.
* Motors are reset to safe current levels and the toolhead is parked.

---

## Benefits

* Filament remains controlled and does not fling or ooze.
* The nozzle and bed remain cleaner.
* Automatic mesh validation makes print startups way faster.
* AMS operation becomes more reliable and consistent.
