# ZEXALL
A Z80 Instruction Set Exerciser for CP/M-80

The ZEXDOC and ZEXALL programs by Frank D. Cringle are for testing
the Zilog Z80 CPU.  There are two versions - one tests by using
the documented flags (zexdoc.com) and the other one tests by
checking both the documented and undocumented flags (zexall.com).

The Flag bits are -

```
bit    7    6    5    4    3    2   1   0
       S    Z    x    H    x   P/V  N   C

where
       C = carry flag
       N = add/subtract flag
     P/V = parity/overflow flag
       H = half carry flag
       Z = zero flag
       S = sign flag

```

The flag bits marked x above are the undocumented flags.  There's a
summary of how the Z80 flags are affected by each instruction (including
the undocumented ones) at http://www.z80.info/z80sflag.htm

The exercisers can be run on a real Zilog Z80 8-bit CPU or to verify
operation under an emulator.  Both binaries can be run under one of
the Digital Research's CP/M-80 operating systems (CP/M 2.2, CP/M 3 etc).

These programs (and their source-code in Z80 assembler) were extracted
from the final version of the YAZE-AG (Yet Another Z80 Emulator) version
2.51.3 curated by Andreas Gerlich at

https://agl.yaze-ag.de/

They are licensed under the GNU General Public License v2.0.

## Updates

* Add modified source-code that can be assembled using Hector Peraza's
ZSM4 Z80 Macro Assembler (see https://github.com/hperaza/ZSM4 for source,
binaries and documentation).  These source files have the .mac file type.
Build these with commands like -

```
zsm4 =zexdoc/L
link zexdoc
```

