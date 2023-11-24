# Ender-3-DD-Klipper

## Description

This project is a deep modernisation of Ender 3. The basic philosophy is: how to print yourself a 3D printer, having a 3D printer. All the parts were printed only on the Ender 3 with minimal purchases of any components. Because I don't see the point in buying something if I can print it without much loss of properties

## Some thoughts and notes
- Out of all the budget controllers I've seen, BTT is the coolest and most well-documented. The amount of time and nerves I spent on setting up all sorts of custom variants, clones of famous boards, mks robin, was enough to take a couple of rework and buy a few mini BTT SKRs, so don't waste too much time on some crap, do what you love and buy a quality product. (This is not an advertisement, there may be even better control boards that I have not had the chance to work with)
- Some ABL sensors do not have a touch mode and require over-engineering to interact with Klipper. It is better to avoid them, because they are usually not very accurate
- Most air ducts are designed for good bridges and high-quality layer sintering, if you don't need to print very large bridges, don't use them
- A big problem with all cooling / direct drive solutions is the weight and leverage that parts create when moving the Z and X axes
- Most slicers are designed for proprietary printers and there is no one-size-fits-all solution, but my headache disappeared after migrating from Cura / Creality / SimplyPrint  to SuperSlicer / PrusaSlicer


## Features
Here are some of the features that I've come up with through constant analysis and improvement of my printer's print quality, prioritised by their impact on print quality

### Hardware
Most hardware changes affect several indicators: print quality, stability and usability, noise (the latter is very important to me).

The ABL is a very important part of your printer, as well as its mount,  you don't want to be constantly adjusting the z-offset and reprinting your prints. The ABL can be made on standard Marlin firmware, but if you want to go further, Klipper is your only option to make life easier.

- ABL CR-Touch + Mount - (Below, a few of the tested options)
- Raspberry Pi 3A+ - [Case](https://www.thingiverse.com/thing:6277790)
- BTT SKR mini E3 v3 - [GitHub](https://github.com/bigtreetech/BIGTREETECH-SKR-mini-E3)
- PSU MeanWell LRS-350 - [Case](https://www.thingiverse.com/thing:4750639)

### Kinematics
- Custom ducts - (Below, a few of the tested options)
- Direct Drive - [SpeedDrive](https://github.com/sashalex007/speedDrive)
- Z Stabilizer - [Bearing](https://www.thingiverse.com/thing:3370355) + [Motor spacer](https://www.thingiverse.com/thing:2925230)
- Spool Adaper - [No purchased parts](https://www.thingiverse.com/thing:5159563)
- Belt Tensioner - [X+Y](https://www.thingiverse.com/thing:2986144)
- Creality Glass Bed
- Yelow spings

### Software
- Klipper + Moonraker + Mainsail [KIAUH](https://github.com/dw-0/kiauh)
- Adaptive Meshing ( Without Purging ) - [KAMP](https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging)
- Timelaps ( RPi Camera Module 3 )
