# Video Configuration & RGB2VGA Setup

> [English](vga.md) | [Русский](readme.md)

The Leningrad-2 2025 Revision features an integrated onboard **ZX_RGBI2VGA-HDMI** converter designed by AlexEkb. This converter uses a powerful Raspberry Pi **RP2040-Zero** board to upscale the vintage ZX Spectrum video signal to modern displays.

## Selecting Output: VGA vs. HDMI

The board can output video via either a standard VGA connector or an HDMI port.

### 1. HDMI Mode (Recommended)
* **Jumpers JP1, JP2, JP3:** Must be left **OPEN**.
* **Resistors R24 to R31:** You **MUST** replace the standard resistors with **270 Ohm** values to ensure proper signal voltage levels for HDMI stability.

### 2. VGA Mode
* **Jumpers JP1, JP2, JP3:** Must be **SHORTED**.
* Use standard resistor values as specified in the original schematic.

---

## Flashing the RP2040-Zero Firmware

To flash or update the video converter firmware via the onboard USB port, follow these crucial safety steps:

1. **Disconnect System Power:** Turn off the main power supply of the Leningrad-2 computer.
2. **Open Jumper J9:** Open/remove the **J9** jumper. *Crucial:* This completely isolates the RP2040-Zero power lines from the main computer board, preventing back-powering issues and potential hardware damage during flashing.
3. **Connect USB:** Connect a USB-C cable from your PC to the RP2040-Zero.
4. **Flash:** Hold the `BOOT` button on the RP2040-Zero, plug it in, and drop the `.uf2` firmware file onto the mounted drive.
5. **Restore:** Unplug the USB cable, **close/solder J9** back, and power on the computer.
