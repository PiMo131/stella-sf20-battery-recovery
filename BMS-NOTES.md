# BMS investigation notes

## Identified marking

The BMS investigated during this recovery carried the marking:

`SH3676016BP`

This identification came from direct inspection of the board.

## Measurements observed during investigation

Low-voltage circuitry around the BMS included measurements of approximately 5 V and ground. Two additional pins and a microswitch were also noted.

A static 5 V measurement does **not** establish that a pin is UART. Possible functions include:

- supply/reference voltage;
- pulled-up control/wake input;
- I2C/SMBus-style bus;
- UART or other serial interface;
- programming/debug connection.

No definitive protocol identification has yet been made.

## Suggested next measurements

With the battery safely assembled enough for the BMS to operate:

1. Establish a reliable logic ground reference.
2. Measure each unknown pin with the battery switch OFF.
3. Repeat with the switch ON.
4. Observe the lines with an oscilloscope or logic analyzer during:
   - power-on;
   - charger insertion;
   - switch operation;
   - connection to the bicycle.

Do not intentionally short an unknown signal to ground or 5 V.

## Evidence convention

Future findings should be marked:

- **OBSERVED** — directly measured or visually confirmed.
- **CONFIRMED** — function established by repeatable electrical/protocol evidence.
- **INFERRED** — plausible interpretation not yet proven.
