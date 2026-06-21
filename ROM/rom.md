\# ROM Selection and Configuration Guide



> \[English](ROM.md) | \[Русский](ROM.ru.md)



The "Leningrad-2 2025 Revision" PCB provides flexible options for installing ROM chips. You can use standard vintage EPROMs or modern alternatives depending on your goals.



\## Supported ROM Chips



1\. \*\*Standard 48K Setup:\*\*

&#x20;  \* \*\*2764 (К573РФ4/6)\*\* — Requires two separate chips. One holds the lower part of the ROM (Basic-48), and the other holds the upper part.

&#x20;  \* \*\*27128 (К573РФ8)\*\* — A single chip that holds the entire 16 KB ZX Spectrum 48K ROM.



2\. \*\*Expanded Setup (with TR-DOS / BDI):\*\*

&#x20;  \* \*\*27256\*\* — Allows you to store two different versions of TR-DOS or customized firmware.

&#x20;  \* \*\*W27E256\*\* — A modern, electrically erasable (EEPROM) drop-in replacement for the 27256. Highly recommended for easy flashing.



\---



\## Jumper Settings for ROM



\* \*\*JP4 (ROM Type Selection):\*\* 

&#x20; \* \*\*Short\*\* this jumper if you are installing \*\*two 2764\*\* chips.

&#x20; \* \*\*Leave Open\*\* if you are using a single \*\*27128\*\* or \*\*27256\*\* chip.

\* \*\*J12 (TR-DOS Firmware Selection):\*\* 

&#x20; \* Active only when using a \*\*27256\*\* ROM. It switches between the two firmware banks stored on the chip.

\* \*\*JP5–JP9 (Memory Expansion Support):\*\* 

&#x20; \* Must be soldered/shorted to ensure correct address lines routing for future memory expansions and multi-bank ROM configurations.



