# HexEnder

This is a project to add the amazing HextrudORT to the Creality Ender 6. This is a DIY, lightweight alternative to other direct drive options currently being modified to fit the Ender 6. The purpose was to end up with a fully enclosed, fast and accurate, Nylon and PC capable printer built upon what is already a brilliant printer. 

What this is not, is a step by step guide. 

This is not the cheapest option for Direct Drive, nor am I claiming it is the best. It is what I wanted to make work, and work it does. My Ender6 now comfortably prints ABS/ABS+ in a ~50c chamber at 150mm/s with 5k acceleraion and in my opinion, better than stock quality. 


<B>THIS IS NOT A SIMPLE PROJECT AND CARE SHOULD BE TAKEN BEFORE STARTING</B>

This is current a version 1. This is the only conversion I know of, so I cannot guarentee that all possible scenarios have been taken into account. Please read through these comments and ask any questions before you start. Plus:
- You will need to know how to wire in the new components
- You will need to be comfortable changing VREFs manually
- Klipper is a must
- If you don't have a back up printer, at the very least print everything in duplicate as mistakes can happen during assembly
- You will need to complete other upgrades to make this work - linear rails / Berd Air / canopy etc.


## Build notes:

### HextrudORT Print Head
- This project has only been tested using the Dragon Hotend version. 
- Please use the latest files from the HextrudORT GitHUb and print ABS/ABS+ (their BOM spreadsheet is also very handy)
- If you use a BLTouch, I have included a new mount that moves the BLTouch to a new position to avoid the belts on the Ender 6
- I would highly suggest buying new belts, the stock ones just fit at a stretch and I really dont recommend that at all. Keep the stock ones as spares.
- Remember to adjust the VREF for the extruder down to 0.350. From what I understand from the Hevort guys, any higher and the stepper will possibly melt/deform the ABS mount.

The Ender 6 uses 9mm belts, both mounted to the front of the X 2020. This makes fitment of after market or DIY solutions hard as most are designed around 6mm belts in a front/back configuration. The goal was to reuse the stock belts 9mm belt setup including steppers, while adding a simpler method of belt tensioning. My design keeps the entire HextrudORT system stock if you wish, by adding a carriage mount underneath to connect the belts to the HextrudORT carriage. However, I found a simple modification to the HextrudORT carriage allowed me to accomodate a simple Berd Air setup and cable chain mount. This is my preferred configuration as it allowed me to fit a small custom PCB breakout board to the back of the carriage for simple changeout of parts. Hotend cooling is delivered via a 3010 fan.

### Berd Air
- Must be 24v
- Do not connect without a diode
- Can be run and controlled via part fan connection

Use any enclosure/mount you like for the pump. It's noisy, no other way to say it, fans will always be quieter. It is not the best choice for high speed printing on PLA so please be aware of that. But for ABS etc. it is perfect. I have opted for twin 'tusks' but you can be as inventive as you like.

### Cable Chain and mounts
- Must be printed in ABS/ABS+
- If you aren't rewiring in Silicon AWG, then at least use a cable sleeve to protect the wiring.

The cable chain is a modified version of the printable Panzer Chain VoronUser mod. It is loosely based on the IGNUS chain designs and so far after 100hrs of printing has yet to sag or deform. I highly recommend it over the current options available, but it will require the carriage design to match, as well as the frame mount. Both are sized to fit inside the stock Creality canopy if you use it.

### Print Bed
- The Z endstop will need a lot of adjustment before printing

The final nozzle height is significantly higher than stock. In fact it is borderline too high. You will need to adjust the Z endstop height and screw out the bed height to make it work. Or, get some taller silicon mounts. Either way, you may need to play around until you are happy. 

### X Rail
- Can be Carbon Fibre 2020
- You will need print the endstop trigger

The only way I could mount the X Endstop without modifyng the HextrudORT, was to use a small trigger peice mounted on the Y carriage. Simple and easy to fit, it doesnt affect your print volume.

### Linear rails
- Use any of the rail mods on Thingiverse
- X Rail is MGN9H x 350mm
- Y rails are MGN12H x 350mm

Any mod should work, but if you are using the Creality Canopy mount, make sure the mod doesn't extend beyond the edge of the frame by more than 10mm. If it does, then the mount won't fit.

### Creality Canopy
- The name plate is optional
- See notes on linear rail mods above

A simple mount to hold and secure the stock Creality Canopy. Its not the best canopy by a long shot, but it seems to be popular and does look the part. Only optional if you don't want to print anything but PLA/PETG or have another solution. Just note that from comments, it seems the clear side panels vary in position and might need adjusting to make the position work.

### Air Filter
- Completely optional
- My choice is either the NeverMore or Annex Rebreather

This is a personal choice. I went for the NeverMore v5 Duo VoronUser mod because it looked the best. It does make a noticable difference to the smell when printing ABS though, so I think its brilliant. I am running mine off the powersupply directly as the stock board doesn't have another PWM connection to use. 

