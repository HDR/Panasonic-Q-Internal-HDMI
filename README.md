
# Panasonic Q Internal HDMI

[![GitHub](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

Please consider supporting me on [ko-fi](https://ko-fi.com/martinrefseth), i generally don't make money on projects like this.

A drop-in plug & play GCPlug based HDMI mod for the Panasonic Q

# Ordering the PCB

## **With Assembly**

### PCBWay
1. Navigate to the [PCBWay Shared Projects page](https://www.pcbway.com/project/shareproject/Panasonic_Q_Drop_in_Internal_HDMI_Mod_c8eb0727.html)
2. Select `PCB+Assembly`
3. Click `Add to cart`
4. Set assembly quantity to 1 (otherwise, the assembly cost rises from 29 USD to 88 USD)
5. Select any solder mask, silkscreen, and surface finish
6. Click `Submit`

## **Without Assembly**

#### PCBWay
1. Navigate to the [PCBWay Shared Projects page](https://www.pcbway.com/project/shareproject/Panasonic_Q_Drop_in_Internal_HDMI_Mod_c8eb0727.html)
2. Select `Only PCB`
3. Select any color, silkscreen, and finish
4. Click `Submit`

#### JLCPCB
1. Navigate to [JLCPCB's order page](https://cart.jlcpcb.com/quote)
2. Click `Add gerber file` and upload `Panasonic Q Internal HDMI.zip`
3. Select 1.6mm Thickness and any color, silkscreen and finish you want

# Ordering the printed pieces
#### PCBWay
1. Navigate to the [PCBWay Shared Projects page](https://www.pcbway.com/project/shareproject/Panasonic_Q_Drop_in_Internal_HDMI_Mod_c8eb0727.html)
2. Scroll down to `CAD-Custom parts and enclosures`
3. Click the shopping cart button
4. Select `Resin`and pick your desired material
5. Change Product Desc to `DIY Entertainment >> Gaming Enclosure (HSCode:950490)`
6. Click `Submit Request`
7. Repeat for the other piece

#### JLCPCB
1. Navigate to [JLCPCB's 3D print order page](https://jlc3dp.com/3d-printing-quote)
2. Click `Add 3D Files` and select `Panasonic Q HDMI Bracket.stl` & `Panasonic Q HDMI Cover.stl`
3. Select `SLA(Resin)` and pick your desired material
4. Set 'Product description' to `Enclosure, Block, Plate, Cylinder Category -> Plastic Enclosure - HS Code 392690`
5. Click `SAVE TO CART`

# Programming
### Tools & Software Needed
- A programmer like the CH341A/B
- The CH341A Programmer Software
-  [gcvideo-3.1-gcplug.zip](https://github.com/ikorb/gcvideo/releases/tag/GCVideo-DVI_release_3.1) from ikorb's gcvideo github page
### Flashing GCVideo
1. Bridge the jumper marked JP1
2. Connect the programmer to the HDMI board according to the pinout written on the programmer and the board
3. Open CH341A Programmer
4. Press the open button and select `gcvideo-dvi-gcplug-3.1-spirom-complete.bin`
5. Select Type: `25 SPI FLASH`, Manu: `GIGADEVICE` & Name: `GD25D40`
6. Press program
7. Press verify to make sure the firmware was written correctly
8. Remove the bridge on JP1

# Parts Overview
## Hardware Parts
```
1x Panasonic Q HDMI Bracket
1x Panasonic Q HDMI Cover
2x M2x6 Screws
1x M3x8 Screw
2x M2x3x3.2mm Threaded insert
1x M3x6x4.5mm threaded insert
```

## Board Parts
| Designator                    | Qty | Part Number           | Package                              | Description                            | LCSC Part# |
|-------------------------------|-----|-----------------------|--------------------------------------|----------------------------------------|-----------|
| C1                            | 1   | GRM155R61E225KE11D    | 0402                                 | 2.2uF Capacitor                        | C385032   |
| C2                            | 1   | CGA0402X5R475M250GT   | 0402                                 | 4.7uF Capacitor                        | C6119795  |
| C3                            | 1   | CL10A106MA8NRNC       | 0603                                 | 10uF Capacitor                         | C96446    |
| C4, C5, C6, C7, C12, C13, C14 | 7   | GRM155R71H104KE14D    | 0402                                 | 100nF Capacitor                        | C77020    |
| C8, C9, C10, C11              | 4   | GRM155R61E105KA12D    | 0402                                 | 1uF Capacitor                          | C77009    |
| D1                            | 1   | IRM-3638T             | SIP-3-2.54mm                         | 38kHz Infrared Receiver                | C16216    |
| J1                            | 1   | 2086581001            | SMD                                  | MOLEX 2086581001 HDMI Connector        | C916313   |
| J2                            | 1   | 1.0-22P CTSJ-H2.5 119 | SMD,P=1mm,Surface Mount，Right Angle | 22 Pin Top Contact 1mm Pitch Connector | C5373501  |
| J3                            | 1   |                       |                                      | 1x6 2.54mm Pin Header                  |           |
| R1                            | 1   | 0402WGJ0331TCE        | 0402                                 | 330Ω Resistor                          | C12246    |
| R2                            | 1   | RC0402FR-07220RL      | 0402                                 | 220Ω Resistor                          | C112291   |
| R3, R4                        | 2   | 0402WGJ0472TCE        | 0402                                 | 4.7kΩ Resistor                         | C25940    |
| R5                            | 1   | 0402WGF1800TCE        | 0402                                 | 180Ω Resistor                          | C38941    |
| R6, R7                        | 2   | RC0402FR-0710KL       | 0402                                 | 10kΩ Resistor                          | C98220    |
| SW1                           | 1   | B3U-1000P             | SMD,2.5x3mm                          | Remote Programming Button              | C231329   |
| U1                            | 1   | XC3S200A-4VQG100C     | TQFP-100(14x14)                      | XILINX FPGA                            | C1521645  |
| U2                            | 1   | ZD25D40CNJGR          | USON-8-EP(1.5x1.5)                   | SPI NOR Flash                          | C3646778  |
| U3                            | 1   | SSPX3819M5-L-5-0      | SOT-23-5                             | 5V Regulator                           | C20617302 |
| U4                            | 1   | RT9013-12GB           | SOT-23-5                             | 1.2V Regulator                         | C58464    |

[**Interactive BOM**](https://martinrefseth.com/ibom/QInternalHDMI.html)

You can also upload `LCSC_BOM.xls` to [LCSC](https://www.lcsc.com/inquiry)

## Notes
- Make sure you hold the button on the board to bring up the remote programming menu BEFORE assembling your Panasonic Q (Save the settings in the menu after programming the remote)
- Cut the pin headers with a flush cutter before re-assembly, otherwise your disk assembly won't fit
- The cost with assembly from PCBWay should be around 78 USD
- HDMI output is for GC mode only
- Enhanced DVI needs to be turned on in the GCVideo settings for audio output


## Credits

ikorb - [gcvideo](https://github.com/ikorb/gcvideo)

citrus3000psi - [gcplug](https://www.reddit.com/r/Gamecube/comments/7gduxq/build_your_own_gcplug/)


![image](https://github.com/user-attachments/assets/b35e1229-5001-494f-b594-a2854504505b)

![image](https://github.com/user-attachments/assets/1d111fb5-5a61-4286-8797-cf4821135f15)

https://github.com/user-attachments/assets/7356d1f4-85a7-4fde-a83c-853f3280a0fc

