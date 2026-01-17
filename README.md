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

_Last validated on P1S + AMS — 2026-01-14_  
_Recommended slicer: [OrcaSlicer](https://github.com/SoftFever/OrcaSlicer)_  

_Note that you may need to Enable "Advanced Mode" in your Slicer to change Start and End G-code._

### 📌 Stock (Default) Bambu Lab P1S G-code

#### - [View stock Start G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/STOCK-START%20G-code) — [RAW](https://github.com/Justagwas/P1S-GCODE/raw/refs/heads/main/G-code/STOCK-START%20G-code)
#### - [View stock End G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/STOCK-END%20G-code) — [RAW](https://github.com/Justagwas/P1S-GCODE/raw/refs/heads/main/G-code/STOCK-END%20G-code)

<details>
<summary>SOURCES — Click to expand</summary>
  
- https://github.com/bambulab/BambuStudio/tree/master/resources/profiles/BBL/machine

- https://github.com/bambulab/BambuStudio/blob/c49f7a49e8cda234185c387efca869892687105b/resources/profiles/BBL/machine/Bambu%20Lab%20P1S%200.4%20nozzle.json#L237

- https://github.com/bambulab/BambuStudio/blob/c49f7a49e8cda234185c387efca869892687105b/resources/profiles/BBL/machine/Bambu%20Lab%20P1S%200.4%20nozzle.json#L238

</details>

_Last checked — 2026-01-14_

### ⭐ Enhanced Start & End Bambu Lab P1S G-code

#### - [View Enhanced Start G-code](https://github.com/Justagwas/P1S-GCODE?tab=readme-ov-file#-start-g-code)
#### - [View Enhanced End G-code](https://github.com/Justagwas/P1S-GCODE?tab=readme-ov-file#-end-g-code)

These custom G-codes use adaptive bed leveling to check and re-probe the mesh only when necessary.

#### 🎥 **[CLICK Here](#-preview)** to preview the L Profile **(VIDEO SHOWCASE)**.

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
| **Bed Mesh Strictness** [(6)](#6-bed-mesh-validation) | ★★★ High | ★★★ High | ★ Low |
| **Thermal Stabilization** [(7)](#7-thermal-stabilization) | ★★★ Strict | ★★ Light | ★ Minimal |
| **Temperature Staging** [(8)](#8-temperature-staging) | ★★★ Multi-stage | ★★ Optimized | ★ Minimal |
| **Wipe Count** [(9)](#9-wipe-count) | ★★★ 24 wipes | ★★ 16 wipes | ★ 8 wipes |
| **Purge Line** [(10)](#10-purge-line) | Yes | Yes | No |
| **Best For** | Infrequent printing | Regular daily printing | Fast, high-turnover printing |

> [!NOTE]
> Want more options? Check out **[Optional Add-ons](#-optional-add-ons-g-codes)**.

---

# 📌 END G-code

| **Feature** | 🟩 **XL-End G-code** 🟩 | 🟦 **L-End G-code** 🟦 | 🟧 **S-End G-code** 🟧 |
|-------------|-----------------------------|-----------------------------|-----------------------------|
| **Click to View File —** <br> **or View RAW Text —** | <div align="center">[XL End G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/XL-END%20G-code)<br>[RAW XL End G-code](https://github.com/Justagwas/P1S-GCODE/raw/main/G-code/XL-END%20G-code)</div> | <div align="center">[L End G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/L-END%20G-code)<br>[RAW L End G-code](https://github.com/Justagwas/P1S-GCODE/raw/main/G-code/L-END%20G-code)</div> | <div align="center">[S End G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/S-END%20G-code)<br>[RAW S End G-code](https://github.com/Justagwas/P1S-GCODE/raw/main/G-code/S-END%20G-code)</div> |
| **Runtime** | TBA | TBA | TBA |
| **Shutdown Speed** [(11)](#11-shutdown-speed) | ★ | ★★ | ★★★ |
| **Unload Reliability** [(12)](#12-unload-reliability) | ★★★ High | ★★★ High | ★★ Medium |
| **Post-Print Purge** [(13)](#13-post-print-purge) | ★★★ High | ★ Low | ★ Low |
| **Nozzle Wipe After Print** [(14)](#14-nozzle-wipe-after-print) | Extended | Moderate | Minimal |
| **Cooldown Staging** [(15)](#15-cooldown-staging) | Multi-stage | Balanced | None |
| **AMS Unload Confidence** [(16)](#16-ams-unload-confidence) | High | High | Medium |
| **Best For** | Long idle periods | Balanced routine use | Rapid printing |

---

## 🎥 Preview

The following previews show the L Profile in action and the difference in printing when:

- a **stored bed mesh is still valid**
- a **stored bed mesh is invalid and requires re-probing**

Both instances used the same L Profile (L-Start & L-End) G-code and printer state, with only the mesh condition changed.

Bed mesh validation starts at 2:16.

### ✅ Bed Mesh Valid — Fast Startup (Mesh is reused)

<details>
  <summary><strong>CLICK HERE TO EXPAND AND VIEW VIDEO</strong></summary>
  <video src="https://github.com/user-attachments/assets/a84602ea-c883-44c7-9c1b-347b69e32dc9" controls muted style="max-width: 100%; height: auto;" ></video>
</details>

### ❌ Mesh Invalid — Slow Startup (Mesh is re-probed)
<details>
  <summary><strong>CLICK HERE TO EXPAND AND VIEW VIDEO</strong></summary>
  <video src="https://github.com/user-attachments/assets/bcd201dd-4633-439a-b95c-567698b0d04d" controls muted style="max-width: 100%; height: auto;" ></video>
</details>

---

## 📘 FEATURE EXPLANATIONS

### START G-code Feature Explanations

<details>
<summary><strong>Expand START feature explanations</strong></summary>

#### (1) Startup Speed  
How quickly the printer reaches a print-ready state.  
**★ = Slowest**, **★★ = Balanced**, **★★★ = Fastest**

#### (2) Startup Reliability  
How thoroughly the printer validates AMS, temps, resets.  
**★★★ = Highest reliability**

#### (3) Initialization Depth  
Extent to which the printer resets its internal state (motors, offsets, flow control).

#### (4) AMS Verification  
How strictly filament presence and loading are checked.  
**More stars = more consistent AMS behavior**

#### (5) Purge Volume  
Amount of material extruded to clear residual filament.  
**More stars = cleaner first layers**

#### (6) Bed Mesh Validation  
How rigorously the stored bed mesh is verified and applied.

#### (7) Thermal Stabilization  
How evenly the nozzle temperature stabilizes before printing.

#### (8) Temperature Staging  
Number of controlled temperature steps before printing starts.

#### (9) Wipe Count  
Number of nozzle wipe passes for cleaning (XL ≈ 24 passes).

#### (10) Purge Line  
Whether a purge line is printed before the first layer.

</details>

### END G-code Feature Explanations

<details>
<summary><strong>Expand END feature explanations</strong></summary>

#### (11) Shutdown Speed  
How quickly the printer completes post-print shutdown routines.  
**★ = Slowest**, **★★★ = Fastest**

#### (12) Unload Reliability  
Thoroughness and safety of the AMS filament unload process.  
**★★★ = Most thorough**

#### (13) Post-Print Purge  
Amount of filament purged after the print to clear residue.

#### (14) Nozzle Wipe After Print  
Intensity of wipe actions after the job finishes.

#### (15) Cooldown Staging  
Whether cooling occurs gradually (XL) or rapidly (S).

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

## 🧩 Optional Add-ons (G-codes)

<details>
<summary><strong>CLICK Here to expand</strong></summary>


### 🟨 L-Start-LITE G-code — Reduced Startup Purge

This optional Start G-code is based on the **L (Balanced)** variant, but with **reduced startup purge/prime**.

- Saves: **~0.2g** purge compared to standard **L-START** and has a smaller purge line.
- Trade-off: higher chance of first-line/first-layer filament/color "bleed" after AMS swaps (e.g. dark → light)

#### Files
- [View L-START-LITE G-code](https://github.com/Justagwas/P1S-GCODE/blob/main/G-code/L-START-LITE%20G-code)
- [RAW L-START-LITE G-code](https://github.com/Justagwas/P1S-GCODE/raw/main/G-code/L-START-LITE%20G-code)

</details>

---

## 🔧 Device Compatibility

- **P1S + AMS** — fully supported  
- **P1S without AMS** — AMS commands are **automatically ignored**  
- **X1C (no AMS)** — NOT Tested
- **X1C + AMS** — NOT Tested

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

## ⚠️ These profiles may not be for you if:

- You prefer the **default Bambu workflow** and do not want to alter machine behavior.
- You want the **absolute fastest** startup and shutdown sequences without additional safeguards (S profile includes safeguards).

---

## 🤝 Contributing

1. Submit "Issues" for Suggestions

OR

1. Fork the repository  
2. Make improvements or variants  
3. Submit a PR  
4. Include reproduction steps if reporting bugs

---

## 📬 Contact

**email@justagwas.com**
