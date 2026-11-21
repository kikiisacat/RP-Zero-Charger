# RP-Zero-Charger

# Why I made it
Many people buy Raspberry Pi Zeros because they are easier to carry around and move compared to the bigger boards, which in turn makes them easier to use in projects. However, they still depend on micro USB power. I designed a carrier board that allows you to plug in a normal battery to charge your pi, and when that battery runs out, you can plug in a USB C to charge both the pi and the battery at the same time. I decided to make this as many people use RP Zeros to make devices such as wearables, robots, and drones, which all depend on battery and would benefit from a charger that is compact and easy to use.

# Features
Battery Power for RP Zeros \
USB C Charging \
A 5V converter for more consistent power

# How it works
The board uses a BQ25895 to charge a battery and manage power for the raspberry pi. The pi is able to easily connect to the circuit board through a regular 40 pin header. All power components are placed on the back for faster and simpler assembly. It also does not need extra firmware for the basic charging features.

# How I made it
I made the schematic and PCB in KiCAD, and searched online for parts to use. I came across a BQ24074 (https://www.adafruit.com/product/4755) breakout board, and decided I would use a BQ25895, which is basically its upgraded version. Next, I chose a TPS61022 to convert batteries' 3.7V to 5V so the Pi could use it. I then placed all components on the back side and started wiring, making sure that I used bigger traces and tried to avoid Vias for power traces.

# List of Parts
1 - BQ25895 battery charger/power manager \
1 - TPS61022 5V converter \
1 - USB C connector \
1 - JST PH battery connector \
1 - 2 * 20 female header for the Raspberry Pi \
2 - 2 pin headers for the switch and thermistor \
1 - MMBT3904 transistor \
1 - 2.2 uH inductor \
1 - 1 uH inductor \
1 - switch \
1 - 10 k ohm NTC thermistor \
 \
Capacitors: \
1 - 47 nF \
1 - 4.7 uF \
1 - 1 uF \
5 - 10 uF \
3 - 22 uF \
 \
Resistors: \
2 - 5.1 k ohm \
2 - 10 k ohm \
3 - 100 k ohm \
1 - 732 k ohm \
1 - 261 ohm \
1 - 5.23 k ohm \
1 - 30.1 k ohm

# PCB Model Front (Where the Pi and its headers get mounted)
<img width="1299" height="630" alt="image" src="https://github.com/user-attachments/assets/897fe3b3-6ce8-4c9e-b805-5db08caf6b9c" />

# PCB Model Back (Where all the components are)
<img width="1115" height="893" alt="image" src="https://github.com/user-attachments/assets/39ace053-e656-4b39-9227-7eb56715b7be" />

# PCB
<img width="922" height="455" alt="image" src="https://github.com/user-attachments/assets/74989d66-3ccf-41d1-b63b-a35101c779cd" />

# Schematic and Wiring (With no labels)
<img width="835" height="1138" alt="image" src="https://github.com/user-attachments/assets/338a689d-a5b1-409d-b85b-e7f737ae3868" />
