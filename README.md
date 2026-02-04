```
╔═══════════════════════════════════════════════════════════════════╗
║                                                                   ║
║   ███████╗██╗  ██╗      ██████╗  ██████╗ ██████╗ ████████╗       ║
║   ╚══███╔╝╚██╗██╔╝      ██╔══██╗██╔═══██╗██╔══██╗╚══██╔══╝       ║
║     ███╔╝  ╚███╔╝ █████╗██████╔╝██║   ██║██████╔╝   ██║          ║
║    ███╔╝   ██╔██╗ ╚════╝██╔═══╝ ██║   ██║██╔══██╗   ██║          ║
║   ███████╗██╔╝ ██╗      ██║     ╚██████╔╝██║  ██║   ██║          ║
║   ╚══════╝╚═╝  ╚═╝      ╚═╝      ╚═════╝ ╚═╝  ╚═╝   ╚═╝          ║
║                                                                   ║
║   ZX-PORTSCANNER V1.0                                            ║
║   Sinclair ZX Spectrum I/O Port Scanner & Analyzer               ║
║   github.com/bad-antics | NullSec Retro Series                   ║
╚═══════════════════════════════════════════════════════════════════╝
```

## Overview

ZX-PORTSCANNER is a BASIC utility for the Sinclair ZX Spectrum that scans and displays the state of I/O ports. Essential for hardware debugging, peripheral detection, and understanding the Spectrum's architecture.

## Features

- **Port Map Display**: Shows all documented ZX Spectrum I/O ports
- **Keyboard Matrix Scan**: Reads all 8 keyboard half-rows
- **Full Port Scan**: Scans all 256 base ports for active devices
- **Binary Display**: Shows port values in binary for bit analysis
- **Colored Output**: Uses INK colors for better readability

## ZX Spectrum I/O Map

| Port | Function |
|------|----------|
| $FE | ULA (Keyboard/Tape/Speaker/Border) |
| $FF | Floating Bus |
| $7FFD | 128K Memory Paging |
| $BFFD | AY-3-8912 Data Register |
| $FFFD | AY-3-8912 Address/Register |
| $1FFD | +3 Disk/Printer |

## Usage

1. Load the program: `LOAD ""`
2. Run: `RUN`
3. View the port map and keyboard scan
4. Press any key for full 256-port scan

## Keyboard Matrix

The Spectrum keyboard is organized as an 8×5 matrix:

| Row | Keys | Port |
|-----|------|------|
| 0 | CAPS-V | $FEFE |
| 1 | A-G | $FDFE |
| 2 | Q-T | $FBFE |
| 3 | 1-5 | $F7FE |
| 4 | 0-6 | $EFFE |
| 5 | P-Y | $DFFE |
| 6 | ENTER-H | $BFFE |
| 7 | SPACE-B | $7FFE |

## Compatibility

- ZX Spectrum 16K/48K
- ZX Spectrum 128K
- ZX Spectrum +2/+2A
- ZX Spectrum +3
- Fuse/ZXSpin/Spectaculator emulators

## Loading

### From Tape
```basic
LOAD ""
RUN
```

### From +3 Disk
```basic
LOAD "scanner.bas"
RUN
```

## Technical Notes

- Uses Spectrum BASIC IN function for port reading
- Port values of $FF typically indicate no device
- Keyboard ports return $FF when no key pressed (active low)
- 128K ports only respond on 128K models

## Part of the NullSec Retro Series

Single-script security and system tools for vintage computing platforms.

## License

MIT License - See LICENSE file
