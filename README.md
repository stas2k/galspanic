# GALSPanic - X68000 SRAM Expansion

![Board design](img/board_design.png)

This repo contains Kicad sources for a Static RAM expansion board for Sharp X68000 personal computer.
Please use latest git version of kicad to open the project, or version >6.0 once it gets released.

## Design
The expansion is implemented using 2MB static RAM chips to make the design simpler.
Address decoder is implemented using a ATF22V10 GAL chip. Source code for it is available in `gal/` directory.

Board dimensions are taken from the [midiori](https://github.com/tdaede/midiori) project.

The board can support up to 10MB of memory and assumes you already have 2MB built in.

A fourth address line is routed and the board can support 1MB systems by masking half of the first memory chip. However, the GAL equations are not written for this case. Let me know if you have such a system.

## Compatibility
Following systems have been reported to work:
- Expert
- ACE
- XVI
- Pro
- 68030

## GAL Equations

You can compile `.pld` GAL equations using [GALasm](https://github.com/daveho/GALasm).

## Board production

I use JLCPCB with the following options:
* PCB Thickness: 1.6
* Surface Finish: ENIG-RoHS
* Gold Fingers: Yes
* 45°finger chamfered: Yes
