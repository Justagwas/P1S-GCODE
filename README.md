# Bambu Lab P1S – Enhanced Start & End G-code

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/Status-Active-brightgreen?labelColor=2d2d2d&color=4ade80">
  <source media="(prefers-color-scheme: light)" srcset="https://img.shields.io/badge/Status-Active-brightgreen">
  <img alt="Status: Active" src="https://img.shields.io/badge/Status-Active-brightgreen">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/Printer-Bambu%20Lab%20P1S-blue?labelColor=2d2d2d&color=3b82f6">
  <source media="(prefers-color-scheme: light)" srcset="https://img.shields.io/badge/Printer-Bambu%20Lab%20P1S-blue">
  <img alt="Printer" src="https://img.shields.io/badge/Printer-Bambu%20Lab%20P1S-blue">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/AMS-Supported-purple?labelColor=2d2d2d&color=a855f7">
  <source media="(prefers-color-scheme: light)" srcset="https://img.shields.io/badge/AMS-Supported-purple">
  <img alt="AMS Supported" src="https://img.shields.io/badge/AMS-Supported-purple">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/G--code%20Profiles-XL%20%7C%20L%20%7C%20S-orange?labelColor=2d2d2d&color=f97316">
  <source media="(prefers-color-scheme: light)" srcset="https://img.shields.io/badge/G--code%20Profiles-XL%20%7C%20L%20%7C%20S-orange">
  <img alt="Profiles" src="https://img.shields.io/badge/G--code%20Profiles-XL%20%7C%20L%20%7C%20S-orange">
</picture>


Carefully tuned, optimized, and documented G-code for **Bambu Lab P1S** printers, with full **AMS** support.  
Made to give you a more controlled printing workflow tailored to your priorities: **reliability**, **balance**, or **speed**.

_Last validated on P1S + AMS — 2025-12-16_  
_Recommended slicer: [OrcaSlicer](https://github.com/SoftFever/OrcaSlicer)_
_Note that you may need to Enable "Advanced Mode" in your Slicer to change Start and End G-code._

### 📌 Stock (Default) Bambu Lab P1S G-code

#### - [View stock Start G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/STOCK-START%20G-code) — [RAW](https://github.com/Justagwas/P1S-GCODE/raw/refs/heads/main/G-code/STOCK-START%20G-code)
#### - [View stock End G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/STOCK-START%20G-code) — [RAW](https://github.com/Justagwas/P1S-GCODE/raw/refs/heads/main/G-code/STOCK-END%20G-code)

_Last checked — 2025-12-15_

### ⭐ Enhanced Start & End Bambu Lab P1S G-code

#### - [View Enhanced Start G-code](https://github.com/Justagwas/P1S-GCODE?tab=readme-ov-file#-start-g-code)
#### - [View Enhanced End G-code](https://github.com/Justagwas/P1S-GCODE?tab=readme-ov-file#-end-g-code)

These custom G-codes use advanced adaptive bed leveling to intelligently validate and re-probe bed mesh only when needed.

---

## 🟩-🟦-🟧 Variant Overview

Choose the G-code variant that aligns with your workflow:

- 🟩 **XL — Reliability & Cleanliness First**  
- 🟦 **L — Balanced for Everyday Printing (Creator Used) (Recommended)**  
- 🟧 **S — Performance / Speed-Oriented**

## ⭐ Star Intensity Guide

Stars represent **feature intensity**, not quality:

- **★★★** — Highest / most thorough  
- **★★** — Balanced  
- **★** — Minimal / fastest  

Numbers (e.g., *24 wipes*) appear for measurable operations.

---

# 📌 START G-code

| **Feature** | 🟩 **XL-Start G-code** 🟩 | 🟦 **L-Start G-code** 🟦 | 🟧 **S-Start G-code** 🟧 |
|-------------|---------------------------------|------------------------------|------------------------------|
| **Click to View File —** <br> **or View RAW Text —** | <div align="center">[XL Start G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/XL-START%20G-code)<br>[RAW XL Start G-code](https://github.com/Justagwas/P1S-GCODE/raw/main/G-code/XL-START%20G-code)</div> | <div align="center">[L Start G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/L-START%20G-code)<br>[RAW L Start G-code](https://github.com/Justagwas/P1S-GCODE/raw/main/G-code/L-START%20G-code)</div> | <div align="center">[S Start G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/S-START%20G-code)<br>[RAW S Start G-code](https://github.com/Justagwas/P1S-GCODE/raw/main/G-code/S-START%20G-code)</div> |
| **Runtime**<br><sub><em>Please note that runtimes can be<br>as short as ~2 minutes (L-profile)<br>if your bed mesh is valid.</em></sub> | ~5 minutes | ~4 minutes | ~2 minutes |
| **Startup Speed** [(1)](#1-startup-speed) | ★ | ★★ | ★★★ |
| **Startup Reliability** [(2)](#2-startup-reliability) | ★★★ | ★★★ | ★ |
| **Initialization Depth** [(3)](#3-initialization-depth) | ★★★ | ★★ | ★ |
| **AMS Verification** [(4)](#4-ams-verification) | ★★★ | ★★★ | ★★ |
| **Purge Volume** [(5)](#5-purge-volume) | ★★★ High | ★★ Medium | ★ Low |
| **Bed Mesh Strictness** [(6)](#6-bed-mesh-strictness) | ★★★ High | ★★★ High | ★ Low |
| **Thermal Stabilization** [(7)](#7-thermal-stabilization) | ★★★ Strict | ★★ Light | ★ Minimal |
| **Temperature Staging** [(8)](#8-temperature-staging) | ★★★ Multi-stage | ★★ Optimized | ★ Minimal |
| **Wipe Count** [(9)](#9-wipe-count) | ★★★ 24 wipes | ★★ 16 wipes | ★ 8 wipes |
| **Purge Line** [(10)](#10-purge-line) | Yes | Small | No |
| **Best For** | Infrequent printing | Regular daily printing | Fast, high-turnover printing |

---

# 📌 END G-code

| **Feature** | 🟩 **XL-End G-code** 🟩 | 🟦 **L-End G-code** 🟦 | 🟧 **S-End G-code** 🟧 |
|-------------|-----------------------------|-----------------------------|-----------------------------|
| **Click to View File —** <br> **or View RAW Text —** | <div align="center">[XL End G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/XL-END%20G-code)<br>[RAW XL End G-code](https://github.com/Justagwas/P1S-GCODE/raw/main/G-code/XL-END%20G-code)</div> | <div align="center">[L End G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/L-END%20G-code)<br>[RAW L End G-code](https://github.com/Justagwas/P1S-GCODE/raw/main/G-code/L-END%20G-code)</div> | <div align="center">[S End G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/S-END%20G-code)<br>[RAW S End G-code](https://github.com/Justagwas/P1S-GCODE/raw/main/G-code/S-END%20G-code)</div> |
| **Runtime** | TBA | TBA | TBA |
| **Shutdown Speed** [(11)](#11-shutdown-speed) | ★ | ★★ | ★★★ |
| **Unload Reliability** [(12)](#12-unload-reliability) | ★★★ High | ★★★ High | ★★ Medium |
| **Post-Print Purge** [(13)](#13-post-print-purge) | ★★★ High | ★★ Medium | ★ Low |
| **Nozzle Wipe After Print** [(14)](#14-nozzle-wipe-after-print) | Extended | Moderate | Minimal |
| **Cooldown Staging** [(15)](#15-cooldown-staging) | Multi-stage | Balanced | None |
| **AMS Unload Confidence** [(16)](#16-ams-unload-confidence) | High | High | Medium |
| **Best For** | Long idle periods | Balanced routine use | Rapid printing |

---

## 📘 FEATURE EXPLANATIONS

### START G-code Feature Explanations

<details>
<summary><strong>Expand START feature explanations</strong></summary>
<br>

#### (1) Startup Speed  
Fastness of reaching print-ready state.  
**★ = Slowest**, **★★ = Balanced**, **★★★ = Fastest**

#### (2) Startup Reliability  
How thoroughly the printer validates readiness (AMS, temps, resets).  
**★★★ = Highest reliability**

#### (3) Initialization Depth  
How completely machine state is reset (motors, offsets, flow).

#### (4) AMS Verification  
Strictness of filament slot and load verification.  
**More stars = more predictable/reliable AMS behavior**

#### (5) Purge Volume  
Amount of extruded material used to clear residue.  
**More stars = cleaner first layers**

#### (6) Bed Mesh Strictness  
How rigorously stored mesh is validated and applied.

#### (7) Thermal Stabilization  
How evenly the nozzle temperature stabilizes before printing.

#### (8) Temperature Staging  
Number of controlled temperature transitions before printing.

#### (9) Wipe Count  
Directional wipes for nozzle cleaning (XL ≈ 24 passes).

#### (10) Purge Line  
Presence of a purge line before the first layer.

</details>

### END G-code Feature Explanations

<details>
<summary><strong>Expand END feature explanations</strong></summary>
<br>

#### (11) Shutdown Speed  
Speed of completing shutdown routines.  
**★ = Slowest**, **★★★ = Fastest**

#### (12) Unload Reliability  
Consistency and safety of AMS unloading logic.  
**★★★ = Most thorough**

#### (13) Post-Print Purge  
Amount of purging after the print to remove remaining residue.

#### (14) Nozzle Wipe After Print  
Intensity of wipe actions after the job finishes.

#### (15) Cooldown Staging  
Whether cooldown is staged (XL) or rapid (S).

#### (16) AMS Unload Confidence  
Reliability of returning filament to AMS slots.

</details>

---

# 🛠 Installation (OrcaSlicer & Bambu Studio)

### For **OrcaSlicer**
1. Select your **P1S** printer profile.  
2. Go to **Machine G-code** → **Start G-code** / **End G-code**.  
3. Paste the desired **XL / L / S** variants.  
4. Save as a **new printer preset** (recommended).  
5. Test with a small print.

### For **Bambu Studio**
1. Open **P1S** printer profile.  
2. Go to **Device** → **Machine Settings** → **Start / End G-code**.  
3. Paste the chosen variants.  
4. Save.  
5. Test with a small print.

> [!TIP]  
> Begin with **L** if you want the safest, cleanest, most balanced behavior.  

---

## ⚙ Motion-Affecting Commands

These scripts use commands such as `M17`, `M220`, and `M221` to manage motor currents and flow.  
Incorrect changes can cause:

- Lost steps  
- Rough extrusion  
- Clogging  
- Overheating  

The included scripts use **firmware-aligned conservative defaults**.  
Modify only incrementally and test carefully.

---

## 🔧 Device Compatibility

- **P1S + AMS** — fully supported  
- **P1S without AMS** — AMS commands are **automatically ignored**  
- **X1C (no AMS)** — NOT Tested
- **X1C + AMS** — NOT Tested

---

## ⚠️ Who This Is *Not* For

These profiles may not be the best fit if:

- You prefer the **default Bambu workflow** and do not want to alter machine behavior.
- You want the **absolute fastest** startup and shutdown sequences without additional safeguards (S profile includes safeguards).

---

## ♻️ How to Restore Stock G-code
Stock (default) P1S Start and End G-code are provided at the **top of this README** for convenience.

To restore defaults:

Copy them from this *README* at the [top](https://github.com/Justagwas/P1S-GCODE?tab=readme-ov-file#-stock-default-bambu-lab-p1s-g-code), OR —

1. Open **OrcaSlicer** or **Bambu Studio**.
2. Create a **new** P1S printer preset.
3. Go to **Machine G-code**.
4. Copy the stock Start / End G-code from there.
5. Paste them into your preset.
6. Save.

---

## 🤝 Contributing

- Submit "Issues" for Suggestions

or

1. Fork the repository  
2. Make improvements or variants  
3. Submit a PR  
4. Include reproduction steps if reporting bugs

---

## 📬 Contact

**contact@justagwas.com**
