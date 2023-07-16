# sb-midi
 "Sound Blaster MIDI" cable, board fits in the connector shell

![Assembled board in plug shell](/img/assembled.jpg)
Shown here installed in the connector shell from a cheap eBay MIDI cable

## Overview
This little board provides a way to build an active MIDI Out cable that plugs into the gameport of a vintage PC sound card (or [HardMPU-WT](https://github.com/PickledDog/hardmpu-wt)). It does not provide MIDI In. With this board and BOM, you will be able to make a proper buffered MIDI cable that can be used with any gameport sound card.

## Assembly
When ordering boards, select 1.2mm-thick PCB. You can use regular 1.6mm (as in my build), but it's an *extremely* tight fit - not recommended.

Sandwich the board between the two rows of solder cups on the D-sub connector, and solder all 15 cups down on both sides. With the board secured to the connector, go ahead and solder down all the SMT parts.

Solder the cable to the 3 necessary MIDI pins (2, 4, and 5) in the DIN plug. Connect the cable screen (if present) to pin 2. Solder the wires at the other end to the numbered pads on the board. Fasten the cable clamp (included with the D-sub backshell) around the cable so that there's a little slack on the wires when everything's inside the backshell. Assemble the backshell with everything inside, and you're good to go.

### But I can't solder SMT!
Wanna learn? This is a pretty good place to start - most parts are simple 2-terminal ones, and the most complex parts are the 3-terminal transistors. All passives are friendly 0805 parts, and the board's pads are enlarged for hand-soldering. Get some [tweezers](https://www.ebay.com/sch/i.html?_nkw=smt+tweezers) and follow a guide online - 2 and 3 terminal parts are easy!

### I wanna connect a joystick as well!
You'll need a DA-15 female socket and some 10-core cable to wire it in. Solder the necessary wires to the solder cups, and route the wires over the top and bottom of the board. Note that you cannot connect a joystick to a HardMPU-WT; it's MIDI-only.

## Part selection
This project is basically all jellybean parts - just use what you have on hand as applicable. R1 and R4 don't have to be *exactly* 240Ω, so long as they both add up to around ~480Ω (for example, you can use a 200Ω and a 270Ω if you want, or just two 220Ω). You'll need to get some cable - the MIDI Manufacturer's Association recommends shielded twisted pair cable (so, shield + one pair). Another option is to cut an existing MIDI cable in half (make two cables!)

## Parts list
Bill Of Materials and part references are below. The specified parts are just the ones I used, and can be substituted as needed - Mouser links provided for convenience and reference. The cable required is *not* in the BOM - you'll need to source it yourself.

| Reference | Value | Qty | Mouser link |
| --------- | ----- | --- | ----------- |
| C1, C2 | 2.2nF ceramic | 2 | [KEMET C0805C222K5RACTU](https://www.mouser.com/ProductDetail/80-C0805C222K5R) |
| J1 | D-Sub DA-15 male | 1 | [Amphenol L717SDA15P](https://www.mouser.com/ProductDetail/523-L717SDA15P) |
| | backshell | 1 | [Kobiconn 156-2015-EX](https://www.mouser.com/ProductDetail/156-2015-EX) |
| Q1, Q2 | MMBT3904 | 2 | [Diodes MMBT3904-7-F](https://www.mouser.com/ProductDetail/621-MMBT3904-F) |
| R1, R4 | 240Ω resistor | 2 | [Yageo RC0805FR-07240RL](https://www.mouser.com/ProductDetail/603-RC0805FR-07240RL) |
| R2 | 10kΩ resistor | 1 | [Yageo RC0805FR-0710KL](https://www.mouser.com/ProductDetail/603-RC0805FR-0710KL) |
| R3 | 2k2Ω resistor | 1 | [Yageo RC0805FR-072K2L](https://www.mouser.com/ProductDetail/603-RC0805FR-072K2L) |
| | 5-pin DIN plug | 1 | [CUI SD-50](https://www.mouser.com/ProductDetail/490-SD-50) |
