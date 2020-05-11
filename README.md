# BM2Timer

This little gem plugs into your 28-pin socket that normally takes a 27C256 chip.
This is used to put two tuning files of 32kb on a 64kb chip (XXX512 chip) and switch
between one or the other tune file.

The BM2Timer V1.1 (and newer) has 2 methods for changing between tunes:
- Blue 2Pin Jumper (method which requires no additional equipment)
- External switch (method which requires a switch *not included*)

**Blue 2Pin Jumper Method**

With this Method you simply need to move the 2Pin blue jumper from pins 1-2 to pins 2-3 to switch between the two tunes.
- When the jumper is on the pins 1-2, it's for tune #2 (use 0000 to 7FFF chip region)
- When the jumper is on the pins 2-3, it's for tune #1 (use 8000 to FFFF chip region)

**External Switch Method**

It can has a single wire lead coming off of it using the middle pin (pin #2).
- When sorting this wire to ground you will run on the tune #2.
If this wire is in open circuit (not connect to ground or any source), it will be on tune #1.

# [Clic HERE to Obtain the BM2Timer][]

**Simple Connection 'Diagram' when using External Switch:**

| Middle pin (Pin#2) | --> Wire | --> Switch (one end) |
| Switch (other end) | --> Ground | |

The switch must be a toggle switch (SPST or SPDT) if you want to switch from one tune to another without holding the button, otherwise if you want to change tune only when the button is held, use a momentary switch.

# COMPATIBLE CHIPS

- 27C512
- W27C512
- W27E512
- 27SF512 SST
- XXX512

This is the requirement if the model you use aren't listed above:
Any 28pin Chips that end by (or has) the '512' marking on them, that are '64kb X8' and that the Pin #1 represent 'A15' will works.

If it has the 512 marking (its also a 64kb X8 chip) but the pin #1 doesn't represent A15 it'll not be a compatible chip!

# ADDRESSING INFORMATIONS

The first Tune are using chip addressing 8000-FFFF
The second Tune are using chip addressing 0000-7FFF

# HOW TO BURN A CHIP FOR THE BM2Timer

With the software that goes with your eprom programmer (chip burner), you will start by selecting your chip model.
1. Erase the chip (if it is blank avoid this step)
2. Open your Tune #2 file (yes #2)
3. Burn this file from 0000 to 7FFF
4. Then open your Tune #1
5. Burn this file from 8000 to FFFF
6. Now your chip is ready to be used, it includes your two files!

# BM2Timer V1.1
![alt tag](https://github.com/bouletmarc/BM2Timer/blob/master/BM2Timer/V1.1/1566977469810_img_3888.jpg)

# Circuit Schematic Diagram 
![alt tag](https://github.com/bouletmarc/BM2Timer/blob/master/BM2Timer/V1.1/eagle_2020-05-11_04-24-36.png)


[Clic HERE to Obtain the BM2Timer]:<https://bmdevs.fwscheckout.com/product/bm2timer>
