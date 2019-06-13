# Xbox Open Source Video Project
![Finished XOSVP Image](/images/enclosure.jpg)
XOSVP is an open-source alternative to the Microsoft HD AV Pack. The XOSVP strives to produce the absolute best analog video quality out of your original Xbox.

## Features
- Highest possible quality analog Y/Pb/Pr component video out
    - Impedance matched board traces and cabling from original Xbox
    - High quality video filter + amplifier, [THS7316](https://www.ti.com/lit/ds/symlink/ths7316.pdf)
        - Low pass filter removes high-frequency noise and aberrations from the source signal without harming video frequencies
        - Reconstructs + Amplifies original signal to ensure matching with the Y/Pb/Pr Standards
        - Reduces DAC Imaging effects on the video receiver
- Optical Audio/SPDIF
    - Best possible audio quality from the original Xbox
    - Support Stereo -> 5.1 Surround Sound
    - Cheap, high-quality optical DAC's easy to source on Amazon/Ebay for those without stereo systems

## More Details
[Check out my in-depth blog post on the XOSVP detailing its construction, evolution, and comparison images.](https://blog.dtho.mp/2018/12/15/xosvp-intro/)

## Designs
- [**Schematics**](/xosvp.pdf)
- [**PCB**](/pcb.png)
- [**BOM**](/bom.csv)
- [**Enclosure**](/enclosure.obj)

All designs are produced with KiCAD 5. This includes all schematic sources, designed footprints, and PCB layout.

## Enclosure
![XOSVP Enclosure](/images/enclosure2.jpg)
Also within this repo is a 3D printable enclosure for the XOSVP. It is designed for friction fit so please ensure your 3D printer is calibrated properly before printing. All files were exported with Millimeter scale.

The enclosure was designed with Tinkercad, and you can view this design [HERE](https://www.tinkercad.com/things/6Rlx4JstT6S-xosvp-enclosure-v3).

## License
I want high-quality analog video from the original Xbox to be available to everyone, which is why I open sourced this project. Everything within this repo is covered by [CERN Open Hardware License v1.2](/LICENSE).

## Contributing
If you have any suggested changes/improvements, please feel free to create an issue or a PR. They will be happily accepted!

# Build Instructions

## Kit
The Following image contains all the parts in the BOM/XOSVP DIY Kit:
![Kit Contents](https://blog.dtho.mp/public/images/kit-contents.jpg)

## PCB Installation

The parts are placed on the board in the following configuration
![PCB Layout](/images/layout.png )

The 3D Printed enclosure is designed for a friction fit, so it is very important that the Y/Pb/Pr jack and VGA connector are completely flush to the PCB like in the following image:
![Flush Y/Pb/Pr connector](https://blog.dtho.mp/public/images/flush.jpg)

## AVIP to XOSVP
![XOSVP Adapter](https://blog.dtho.mp/public/images/xbox-to-vga.jpg)
To make the cable that connects the Xbox to the AVIP, you will need to splice the included AVIP connector with the included VGA cable.

Creating this cable is a rather involved process, and you want to get it right, so I created the following video tutorial to document the process I follow when making them.

[**YouTube Video Tutorial**](https://www.youtube.com/watch?v=ltjp-2m_H6U)

The following pinouts are provided for extra detail and are intended to be used alongside the video tutorial.

This splice must follow the following pinout guide

![AVIP Pinout](/images/avip-pinout.png)

Each of the colored AVIP pins must be connected so that they match the following pinout of the VGA cable. The only exception is the `AVIP JMP 1` and `AVIP JMP 2` pins. These need to be jumped together on the top + bottom of the AVIP connector.

![VGA Pinout](/images/vga-pinout.png)
