# "todd" prototype watch

Ok so this is the "big board" prototype. Everything broken out, huge pcb, erring on the side of excess, etc. Hopefully this design can just be taken and crammed onto a tiny lil board when we're ready to make some wearable prototypes.

[See the schematic here](./sch_export/todd_watch.pdf)

---

## theory of design

I'm trying to not stray too far from the designs of the original run of pebbles. I'm all in for messing with the "formula" in the future but right now we need more of the same, yeah? With that in mind the feature set hits the same notes:

* 32bit ARM cpu @ 128mhz with ~512k RAM
* 64mb flash storage
* JDI memory-in-pixel transflective LCD
* Four buttons
* IMU with magnetometer, gyroscope, etc.
* Microphone

It's a good starting place anyway. I'm not too worried about part commonality (practical reasons, the pebbles are getting up there in years) and once I abandoned that mindset things got wild. With that in mind -

## the changes

In no particular order

* The cpu was switched over from an STM32 to a shiny new Nordic part, the nRF5340. Along with the obvious improvements - more memory, more flash, more faster - it's a combo cpu + bluetooth part, so we don't need a separate bluetooth chip. It also has a dedicated networking core which might be useful for power reduction going forward.
* The display is a 176x176 model, up from 168x144. It's the closest display I could find to the originals.
* The IMU has a magnetometer built in - one fewer chip.
* The PMIC includes all the battery hardware, plus a haptic controller. Also about that -
* Swapped the ERM vibration motor for a linear resonant actuator. Welcome to the future bay bee
* NFC is also built into the cpu, so tap to pay might be a potential feature. Maybe. Hopefully.

## back to theory

I'd like this design to stay relevant and sourceable for a while so I'm choosing parts by what I can trust will be available long term. As of right now all the parts chosen are in stock at digikey, normally stocked by digikey, and have at least five years of availability on the roadmap. (Save for the display - it's in stock at arrow right now but it's a weird part with no good replacement so).

The board is gonna be big to support all the extra jumpers and breakouts and whatnot but it's gonna use the same packages (ideally) as the small version. These are gonna be nasty little BGAs and QFNs which means that most people won't be able to build one but them's the breaks. When everything is working I'm down to do a little manufacturing run with my oven, get some hardware to people.

---

## so does it work

Not yet

## when will it work

June, probably

## what's done

Schematic is looking good. Working on BOM and footprints now
