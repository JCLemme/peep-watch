# hardware description

All this is preliminary since I haven't built it yet lol.

---

## what it is

The big board is a huge prototype for the eventual smartwatch. It uses most (if not all) the same parts as the final watch, implements the same circuit the final watch will use (hopefully), and is a close enough hardware match to the final product that we can start porting rebbleos to it. In addition, it presents a bunch of test points and jumpers and whatnot so that we can prototype changes that will need to be made on the next prototype.

Jumpers are included on all the power rails to every chip. This is probably gonna go down as Lemme's Folly but it's my hope that it'll let me cut off broken sections of the board so that I don't have to build new ones every time I break something. They might also be useful for power optimization - just pop the jumper out and replace with an ammeter for accurate current measurements from any subcomponent.

## i don't get it

Working on some real documentation now. Until then I left little notes in the schematic.

---

## the goods

### Nordic Semiconductor nRF5340 - dual core Cortex M33 system-on-chip with Bluetooth LE and NFC

Full part number: NRF5340-QKAA-AB0-R7 ($9.90 at Digikey)
Package: aQFN94
Datasheet: [here](../common/datasheets/nRF5340_OPS_v0.5.1.pdf)

This part is still in development, but it seems far enough along to be useful. 

### Cypress Semiconductor S25FL512S - 512Mbit [Q]SPI Flash

Full part number: S25FL512SDSBHV210 ($9.12 at Digikey)
Package: 24-TBGA
Datasheet: [here](../common/datasheets/002-00488_S25FS512S_512_Mb_1.8_V_Serial_Peripheral_Interface_with_Multi-I_O_Non-Volatile_Flash.pdf)

### Bosch Sensortec BMX160 - 9 axis IMU with accelerometer, gyroscope, magnetometer

Full part number: BMX160 ($9.50 at Digikey)
Package: 14-VFLGA
Datasheet: [here](../common/datasheets/bst-bmx160-ds0001.pdf)

### Maxim Integrated MAX20353 - PWIM with battery charger, monitor, fuel gauge, haptic controller

Full part number: MAX20353AEWN+ ($9.37 at Digikey)
Package: 56-WFBGA
Datasheet: [here](../common/datasheets/MAX20353.pdf)

### Silicon Labs Si1151 - ambient light sensor

Full part number: SI1151-AB00-GM ($1.39 at Digikey)
Package: 10-WFQFN
Datasheet: [here](../common/datasheets/si115x-datasheet.pdf)

### Japan Display Inc. LPM013M126C - 176x176 transflective memory LCD with backlight

Full part number: LPM013M126C ($34.07 at Arrow)
Package: ribbon connector, 0.5mm pitch, 10 pins
Datasheet: [here](../common/datasheets/5lpm013m126c_specification_ver03.pdf)

### TDK InvenSense ICS-40619 - MEMS microphone

Full part number: ICS-40619 ($1.54 at Digikey)
Package: custom, 3.5x2.65x1.10mm 
Datasheet: [here](../common/datasheets/ICS-40619-Datasheet.pdf)

### Jinlong Machinery and Electronics, Inc. VLV041235L - linear resonant actuator

Full part number: VLV041235L ($3.61 at Digikey)
Package: custom, ribbon with two solder pads
Datasheet: [here](../common/datasheets/VLV041235L.pdf)
