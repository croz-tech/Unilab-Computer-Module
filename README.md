# Unilab Computer Module
This is a clone of the UNILAB BBC Micro computer interface. 
![Clone Unilab Computer Module](https://github.com/croz-tech/Unilab-Computer-Module/blob/main/pics/Finished%20PCB%20MK%20IIa.jpg)
Compatible with all UNILAB modules this allows control from a BBC Micro rateher than the usual 3-Chip-Plus.  This device connects to both PA and PB of the 6522 interface adapter (BBC User Port for input and BBC Printer Port for output).  Credit goes to Louis Higgins who shared detailed photographs of both sides from an original board, enabling this clone to be created.  You'll note that this board is smaller than the original.  While my 3-Chip-Plus clone kept the original board dimensions, this recieved mixed feelings.  In this case I've compressed the board to just 100x100mm to keep it to the $5 level for most board manufacturers. 
 
Example code to read/write these ports from BASIC is included on the schematic.  
## Compatibility:
This board should work fine with the BBC Micro (model B), the B+ range and the Master range, although I think the Master Compact lacks the user port so this is probably incompatible with that machine.

## Notes and Errors:
Note that is the first issue of this schematic/board there are a couple of errors (both to be corrected on a future revision):
1) U3 should be the TTL IC 7416, not 74LS06 as shown on the schematic and PCB skilscreen. 
2) The 3x notches for each of the female connectors (U1 and U4) are on the wrong layer of the PCB design so will be missing on manfuacture.  Use a small round file on the boards to add these notches (shown on the silkscreen) before assembly.

Note also that I have decided to not fit the diodes D2 and D3 from the CB1/CB2 ports to VREF on my first build.  While this might make sense to clamp the H1/H2 inputs (converting to TTL levels safe for the Beeb) I'm concerned that CB1/CB2 can be driven as outputs which might stress the 6522.  Will check on the 6522 datasheet and address this later.

## Connection:
The module connects to the Beeb's User and Printer ports using a 20-way and 26-way IDC ribbon cables respectively.  Unlike the original I've gone with IDC headers rather than IDC solder terminators on the PCB since these are becoming more difficult to get hold of and it means the cables can be entirely removed from the board for easier storage.    I've made the cable around 0.5m length and these are 1:1 cables (pin numbering identical at either end).  The unit takes its power from the Beeb's User Port and can also power UNILAB peripheral boards.  The board is fitted with a 500mA polyfuse to protect the Beeb from any short circuits (the original boards used a 1/4 inch glass fuse).
