# Unilab Computer Module
A clone of the UNILAB BBC Micro computer interface.  Compatible with all UNILAB modules this allows control from a BBC Micro rateher than the usual 3-Chip Plus.  This device connects to both PA and PB of the 6522 interface adapter (BBC User Port for input and BBC Printer Port for output).  Credit goes to Louis Higgins who shared detailed photographs of both sides from an original board, enabling this clone to be created.
 
Example code to read/write these ports from BASIC is included on the schematic.  

Note that is the first issue of this schematic/board there are a couple of errors (both to be corrected on a future revision):
1) U3 should be the TTL IC 7416, not 74LS06 as shown on the schematic and PCB skilscreen. 
2) The 3x notches for each of the female connectors (U1 and U4) are on the wrong layer of the PCB design so will be missing on manfuacture.  Use a small round file on the boards to add these notches (shown on the silkscreen) before assembly.
 
