# LILYGO T-Display P4 — Boot and First-Contact Guide

## Scope and evidence

This is a minimum bring-up guide for the LILYGO T-Display P4. Confirmed observations come from [the first-contact notes](first_impressions.md); anything not demonstrated there is marked **unverified**.

| Item | Status | Bench evidence |
|---|---|---|
| USB connector marked `P4U` | Confirmed | Connecting USB activated the battery-charging indicator. |
| Side-mounted slide switch | Confirmed | The board did not start until the switch was placed in its on position. |
| Multiple USB connectors | Confirmed | More than one connector is present; their complete functions were not mapped. |
| Programming connector, USB bridge, required driver, bootloader sequence | Unverified | No successful host enumeration or firmware upload was recorded. |
| LCD controller, pin definitions, initialization order, backlight control | Unverified | The project index lists these as outstanding validation. |

## USB port roles

- **`P4U`:** confirmed USB power input with an observed battery-charging indication. Its use for serial communication, debugging, or firmware upload is **unverified**.
- **Other USB connector(s):** physically present, but their power, data, USB-host, USB-device, and programming roles are **unverified**. Do not assign a function from connector shape or position alone.
- Record the exact board revision, connector markings, host-detected USB device, and exposed serial port before labeling a connector as the programming interface.

## Side-switch behavior

The physical side-mounted slide switch must be in its **on** position for normal startup.

A charging indicator can illuminate while the board itself has not started. Charging activity therefore does not prove that the processor, display, or application firmware is running.

## First boot and power behavior

1. Use a known-good USB data cable and connect the connector labeled `P4U` to a suitable USB power source.
2. Check for the observed battery-charging indicator.
3. Move the side slide switch to its on position.
4. Watch the display for the existing factory or previously installed application.
5. If the charging indicator is active but the display remains blank, verify switch position and cable first; then check host enumeration and whether the installed firmware initializes the LCD and enables the backlight.
6. Record USB-powered startup, battery-only startup, charging indication, and behavior after removing USB as separate observations.

Confirmed power behavior is limited to **charging indication on `P4U`** and **startup requiring the slide switch**. Battery capacity, charging current, charge termination, runtime, automatic power-path switching, and battery-only operation remain **unverified**.

## Flashing method

A successful flashing procedure has **not** been established in the first-contact notes.

1. Identify the exact board model and revision and obtain the matching LILYGO board documentation or example project.
2. Put the side switch in its on position and connect a known-good USB data cable.
3. Check which connector actually enumerates on the host; record the USB vendor/product identification and any serial device.
4. Use the board-revision-specific upload method supported by the selected firmware environment.
5. If automatic entry into the downloader fails, consult the board-specific documentation for its actual boot/reset procedure; no button combination is confirmed here.
6. Capture the successful connector, host device, toolchain, upload command, firmware revision, and required switch/button sequence before treating the process as repeatable.

The correct programming connector, native USB versus USB-to-UART path, bootloader-entry sequence, and upload command are **unverified**.

## Driver notes

No USB interface chip, host driver package, or operating-system requirement has been identified.

- First check whether the host detects the board or creates a serial device using its existing drivers.
- If it does not, verify the cable supports data and test the other connector before assuming a driver fault.
- Install a driver only after identifying the actual enumerated USB device or bridge chip.
- Record the host operating system, detected USB identification, serial-port name, and any driver actually required.

## Known-good display test: existing application smoke test

Use an untouched board with a working factory demonstration, or another already-working P4, as the reference. This test does not depend on unverified LCD pin assignments or a new firmware upload.

1. Connect USB to `P4U`.
2. Confirm the charging indicator and place the side switch in its on position.
3. Allow the existing firmware to start.
4. Check that the screen backlight turns on and that the existing application or factory animation is visible.
5. Compare a suspect board against the known-working board with the same power source, cable, connector, and switch position.

**Pass:** visible, illuminated application content or a running factory animation.

**Fail:** charging indication without visible display output, no backlight, a blank lit screen, or no response after the switch is on.

A passing result verifies the existing firmware can drive that board's display; it does **not** establish the LCD controller, initialization order, backlight pin, touch behavior, or compatibility with a new firmware framework.

## Remaining bench questions

- Which connector supports firmware upload, serial logging, and debugging?
- What USB device or bridge appears on the host, and does it need a driver?
- What boot/reset sequence and upload command work for this exact board revision?
- Which display controller, pin definitions, initialization sequence, and backlight control are correct?
- Does the board boot and remain stable on battery alone, and what are its charging current and runtime?
