# Apple II Profile controller board replica assembly instructions

Instructions to assemble the recreation of the Apple II Profile controller card.

## Background

Several years ago, Travis Phalen gave me an Apple Profile drive. Since I only have 
Apple II machines and not an Apple /// or a Lisa, I needed to find a controller
card. Sadly they are stupidly expensive and not readily available.

I was able to get my hands on a very rough controller card in October 2024 that I
didn't trust for a working drive, but it was suitable to recreate the controller
card using the original era chips.

## Obsolete components

Due to the age of this design, some components are no longer produced.

The following components are known to be obsolete as of June 2025:

| Reference | Chip   | Notes                                        |
|-----------|--------|----------------------------------------------|
| UA5       | CA3096 | Getting hard to find, long out of production. Recommended to be  replaced via transistors. |
| UB7       | 74LS13 | Readily available via online sources, but new stock no longer produced. |
| UC6       | 2716   | D2716 ROM. Generally available, but requires older voltage standards to erase and reprogram. |

### CA3096

The CA3096 is a series of transistors on a common substrate. In this application,
it is mostly used as a series of diodes, and the common substrate is connected to
ground.

This chip was commonly used in audio equipment, and that community has come up with
an equivalent series of transistors to replace the chip.

| Reference  | Transistor      | Form factor |
|------------|-----------------|-------------|
| Q1, Q2, Q3 | BC847C (2N3094) | SOT-23      |
| Q4, Q5     | BC857C (2N3906) | SOT-23      |

Surface mount pads are provided for the transistors. 

When assembling, only use the Q1-5 pads or the CA3096, **not both**.

## Bill of materials

Mouser links are provided where available - Mouser is a sponsor of the DFW Retro Computing group, and they are based in the DFW Metroplex. As of this writing, parts are approximately $33 before tax and shipping.

ICs are labeled using modern standards. The original card has a grid of A-C, 1-8 and my numbering system generally follows that except for the resistor packs. (This grid is common for Apple pre-1986).

[Link to Mouser project](https://www.mouser.com/Tools/Project/Share?AccessID=d3199e41f6) (DIP sockets not included)

| Reference | Value | Qty | Notes |
|-----------|-------|-----|-------|
| C1, C2, C3, C4, C6, C8, C9, C10, C11, C12, C13, C14, C15, C17, C18, C19, C20, C21 | [0.1UF](https://www.mouser.com/ProductDetail/80-C420C104M5U5HA) | 18 | Any generic 0.1uf ceramic capacitor will do. |
| C5 | [0.01uf (10nf)](https://www.mouser.com/ProductDetail/80-C410C103Z5U-TR) | 1 |  |
| C7 | [47uf, 16v](https://www.mouser.com/ProductDetail/667-ECA-1CM470) | 1 | 5 mm, 2 mm pins. Use radial cap and fold over as axial caps are more expensive. |
| C16 | [10uf, 16v](https://www.mouser.com/ProductDetail/667-EEA-GA1C100B) | 1 | 4 mm, 1.5 mm pins. Use radial cap and fold over as axial caps are more expensive. |
| P1 | [2x13 2.54mm header](https://www.mouser.com/ProductDetail/649-10056845-126LF) | 1 | 2x13 2.54 MM pin header. Recommended to solder a right angle header. Used to connect pigtail cable to the Profile card. |
| Q1,Q2,Q3 | [BC847C](https://www.mouser.com/ProductDetail/637-BC847C) | 3 | SOT-23. Optional, only if not using CA3096 in UA5. NPN transistor. Possibly can use 2N3904 but not yet tested.|
| Q4,Q5 | [BC857C](https://www.mouser.com/ProductDetail/637-BC857C) | 2 | SOT-23. Optional, only if not using CA3096 in UA5. PNP transistor. Possibly can use 2N3906 but not yet tested. |
| R1,R2,R7 | [10K](https://www.mouser.com/ProductDetail/660-CFS1-4CVTR103J) | 3 | | 
| R3 | [3.3K](https://www.mouser.com/ProductDetail/660-CFS1-4CT52R332J) | 1 | | 
| R4,R6,R9 | [1K](https://www.mouser.com/ProductDetail/660-CFS1-4C102J) | 3 | | 
| R5 | [1M](https://www.mouser.com/ProductDetail/660-CFS1-4C105J) | 1 | | 
| RP1,RP2 | [4116R-1-101LF](https://www.mouser.com/ProductDetail/652-4116R-1LF-100) | 2 | 100 ohm resistor pack, inline. Original parts MDP1603-101G, replaced by [MDP1603100RGE04](https://www.mouser.com/ProductDetail/Vishay-Dale/MDP1603100RGE04) | 
| RP3 | [4608X-102-222LF](https://www.mouser.com/ProductDetail/652-4608X-AP2-222LF) | 1 | 2.2K resistor pack, inline |
| RP4 | [4114R-1-471LF](https://www.mouser.com/ProductDetail/652-4114R-1LF-470) | 1 | 470 ohm resistor pack. Original part 641-3-R470. | 
| UA2 | [74LS374](https://www.mouser.com/ProductDetail/595-SN74LS374N) | 1 | | 
| UA3 | [74LS244](https://www.mouser.com/ProductDetail/595-SN74LS244N) | 1 | |
| UA4 | [74LS125](https://www.mouser.com/ProductDetail/595-SN74LS125AN) | 1 | | 
| UA5 | CA3096 | 1 | Refer to obsolete note above, or replace with Q1-5. |
| UA6 | [74LS138](https://www.mouser.com/ProductDetail/595-SN74LS138N) | 1 | |
| UA7 | [74LS38](https://www.mouser.com/ProductDetail/595-SN74LS38N) | 1 | |
| UA8 | [74LS279](https://www.mouser.com/ProductDetail/595-SN74LS279AN) | 1 | |
| UB3 | [74LS132](https://www.mouser.com/ProductDetail/595-SN74LS132N) | 1 | |
| UB4 | [74LS368](https://www.mouser.com/ProductDetail/595-SN74LS368AN) | 1 | | 
| UB6 | [74LS259](https://www.mouser.com/ProductDetail/595-SN74LS259BN) | 1 | | 
| UB7 | 74LS13 | 1 | Refer to obsolete note above. |
| UB8 | [74LS14](https://www.mouser.com/ProductDetail/595-SN74LS14N) | 1 | |
| UC1 | [74LS280](https://www.mouser.com/ProductDetail/595-SN74LS280N) | 1 | | 
| UC2 | [74LS109AN](https://www.mouser.com/ProductDetail/595-SN74LS109AN) | 1 |  | 
| UC6 | 2716 | 1 | D2716 ROM |
| UC7 | [74LS32](https://www.mouser.com/ProductDetail/595-SN74LS32N) | 1 | |

## Assembly

1. If using, solder on surface mount transistors Q1-Q5 (omit if using a CA3096).
2. Solder on the resistors and axial capacitors (all except C).
3. Solder on DIP sockets (highly recommended as the original board has these). DIP sockets are not included in the Mouser cart above.
4. Solder on the radial capacitors and fold over.
5. Insert chips and attach ribbon cable to pin header.
6. Attach your Profile drive and start the drive. Wait 2 minutes for it to load.
7. Turn on your Apple II.
8. Enjoy your Profile drive!

## Compatibility

This is known to be compatible with the Profile 5 MB hard drive, as that is what I have. Photos online show that the 10 MB controller is the same as the 5 MB but with the 10 MB ROM chip, but I have yet to test this.

This card is not yet compatible with the [ESProfile](https://github.com/alexthecat123/ESProFile). Alex and I have swapped both our projects with the ultimate goal of getting these to work together. As the ArduinoFile is deprecated, there are no plans to work on compatibility for that project at this time. 

## Credits

Thank you to Raymond Jett of [arcadecomponents.com](https://www.arcadecomponents.com) for his assistance with troubleshooting, [Vince Briel](https://github.com/retrotink) for his guidance, and Tammy Hanson of [Apple Rescue of Denver](https://applerescueofdenver.com) for her loan of a working Profile drive to get mine functional.

## Revisions

The first version (unlabled, but now known as Rev A) had issues with missing traces. Rev B corrected those, but I had missed some traces from the D2716 data bus to UA2 and UA3.

## License

Original PCB design © 1983 Apple Computer.

Recreated PCB © 2024-25 Kevin Trinkle. The board is not yet publicly available but will be made available in limited quantities in the future. My longer term vision is to convert this to a surface mount board and update to a more accessible EPROM.

