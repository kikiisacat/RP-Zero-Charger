---
title: "Raspberry Pi Zero 2W Carrier Board"
github: "https://github.com/kikiisacat/RP-Zero-Charger"
description: "A board that allows you to plug a battery into a RP Zero 2W instead of needing it to depend on a microUSB."
created_at: "2026-10-31"
total_time: "7h 54m"
---

# October 31, 2026: Searched for the right parts
<!-- fabricate:entry 1743 -->

I settled on the BQ25895 and the TPS61022. The BQ25895 charges the battery from the usb-c port, while also being able to manage power for the running board as well. The TPS61022 is able to boost the battery from 3.7V to 5V, so that the Pi can use the power.

Also found the spec sheets:
https://www.ti.com/lit/ds/symlink/tps61022.pdf
https://www.ti.com/lit/ds/symlink/bq25895.pdf

![](https://fabricate.hackclub-assets.com/b7f6e8281eeff1f53848aa4fd97d6e3068fbaaf0f7ca4f21a9c91f2f7455a008/image-png/image.png)
![](https://fabricate.hackclub-assets.com/622d4692e24a4ca3ea9b34242597fbd294f6808c230e0b2b2d341fdef5a16066/image-png/image.png)

**Total time spent: 30m**

# October 31, 2026 (entry 2): The Schematic
<!-- fabricate:entry 1770 -->

I finished up the schematic for the RP Zero 2W charging pcb, and placed down USB-C, BQ25895, TPS61022, and their resistors/capacitors from their spec sheets. Used the built in RP-Zero template in KiCAD.
Added a Thermistor for safety.

![](https://fabricate.hackclub-assets.com/231279d4fa76086b2524968455f8ce8bf3619a5e509fd26ef21e947545fc33d8/image-png/image.png)

**Total time spent: 2h 48m**

# November 1, 2026: Finished PCB
<!-- fabricate:entry 1802 -->

I finished wiring up the PCB. The battery input goes on the SD card side of the pi, while the USB-C charger goes near the camera area. I decided to mount all the components on the back while the pi goes on the front for easier smd assembly. 

I tried my best to make all power traces thick, but some needed vias. It also has 2 GND pours.

![](https://fabricate.hackclub-assets.com/fa80c1e098468420d0ae025f929015abae32e8467af9651e3225109d1f468bbb/image-png/image.png)

![](https://fabricate.hackclub-assets.com/fb6e8efb1d2f4a1cdc126ea89dcab27d16009537b72ac4492d0d3a7e83e947de/image-png/image.png)

**Total time spent: 4h 12m**

# November 8, 2026: Revised PCB, Schematic, and BOM
<!-- fabricate:entry 2410 -->

I got rid of all net labels in the schematic to clean it up. I also rounded the corners of the PCB so that it can fit directly behind the pi with nothing sticking out. Lastly, I added a row in the BOM for the total.

I will still be paying out of pocket or have all the parts in the BOM so a grant will not be needed.

![](https://fabricate.hackclub-assets.com/7256c1fbf45110754bb973e73fbfd7a90e45ffc93cdcc67e2260a0f8cebf7971/image-png/image.png)
![](https://fabricate.hackclub-assets.com/5b841172174e35e068f7a8aaa716ebdaa8c2e33656cb58c70944a0201406d819/image-png/image.png)
![](https://fabricate.hackclub-assets.com/2797c7bb6b45b5f7174d1b376bc41ab39b47040611ce80ba9a8d356860775f25/image-png/image.png)

**Total time spent: 24m**
