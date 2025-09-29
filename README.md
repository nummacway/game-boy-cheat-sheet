# Printable Game Boy SM83 (DMG-CPU) Instruction Cheat Sheet

This is a more graphical representation of the instructions supported by the Game Boy CPU. The goal was to get all relevant information to fit on one sheet of A4 paper, and to employ graphs, figures and tables instead of lists. Graphs are used to show the Loads possible with a single instruction, whereas tables compare similar instructions.

[![Preview of the PDF](/Printable%20Game%20Boy%20Instruction%20Cheat%20Sheet.png)](https://nummacway.github.io/game-boy-cheat-sheet/Printable%20Game%20Boy%20Instruction%20Cheat%20Sheet.pdf)
[Download](https://nummacway.github.io/game-boy-cheat-sheet/Printable%20Game%20Boy%20Instruction%20Cheat%20Sheet.pdf)

The product has been created with Affinity Publisher v1.10.6 in late September 2025. The 8-Bit Loads graph is from February 2025. Because the latter's original size/DPI (it wasn't originally meant to be printed) looked nicest when put on A5 paper, the original project file (`.afpub`) uses A5 paper. It was upscaled to A4 prior to export.

## Notes
* The document is 100% vector graphics and text.
* Some instructions appear twice, because they fit into multiple categories defined by the document.
* The SM83 CPU has several instructions that are identical, usually with the exception of how they set the flags. Only `XOR A` and `SUB A` are explicitly listed as identical, but `RLA` and `ADC A` are mentioned in the text. The _8-Bit Shifts_ table also implies that five 1-byte instructions on A have comparable 2-byte instructions on any 8-Bit register (and the byte HL points to) that set one flag differently. `NOP`, `LD r8, r8`,  `AND A` and `OR A` are not listed as identical although they all do the same thing: nothing (though the latter two set flags).
* I'm intentionally using `RST n16` rather than `RST vec`, because in my opinion (which isn't shared by many) this is more in line with the widely-accepted `JR` notation, `JR n16`. Both are severely limited in what arguments they take. When I was new to assembly, the whole `RST` terminology was confusing to me. I used `RST n16` (16-bit) rather than `RST n8` (8-bit) to not imply a _fundamental_ difference between `RST` and `CALL`.

## Future
Maybe I'll eventually make another cheat sheet for Pan Docs/`hardware.inc`. Unlike the instructions which could all be listed on one sheet of paper, a hardware cheat sheet would require selecting the most relevant information, even if using two or three pages (which it likely will).
