# Contributing to P1S-GCODE

Thank you for helping improve P1S-GCODE.

These profiles control physical printer behavior. A useful contribution must be understandable in the G-code itself and supported by careful testing on the hardware and configuration it claims to support.

## Before proposing a change

1. Read the README, Wiki, Compatibility, Safety, and Limitations pages.
2. Search existing issues and pull requests for the same behavior.
3. Compare the proposed change with both the current profile and the stock P1S sequence.
4. Keep the stock reference files unchanged unless their documented upstream source has changed.

## Reporting unexpected behavior

Use the issue form and include:

- Printer model and relevant hardware modifications.
- Firmware version.
- Slicer and slicer version.
- AMS or external-spool configuration.
- Start and end profile names.
- Build plate and filament type when relevant.
- Exact steps and observed printer behavior.
- Whether the same sliced model behaves normally with the stock profile.

Do not attach G-code that contains private paths, identifiers, network information, or unrelated model data.

## Profile proposals

Explain the practical problem first, followed by the intended printer behavior. Identify every affected command and describe its expected effect, compatibility considerations, and recovery path.

A profile proposal should not present preference as a universal improvement. Preparation time, material use, safeguards, and cleanup behavior are tradeoffs.

## Testing

Test changes incrementally on a supported P1S configuration. Record:

- The original and revised behavior.
- Printer, firmware, slicer, and AMS state.
- Whether the sequence was observed directly from start to finish.
- At least one recovery or cancellation path when relevant.
- Any effect on movement, temperature, extrusion, probing, unloading, or cooldown.

Do not ask another person to run an unreviewed motion, heating, or extrusion change that you have not tested yourself.

## Pull requests

1. Fork the repository and create a focused branch.
2. Preserve the established naming and comment style.
3. Update documentation and comparison text with the code.
4. Include a concise explanation of what changed and why.
5. Provide the testing record and any remaining limitations.

By submitting a contribution, you agree that it may be distributed under the repository's Apache License 2.0.
