Day 1- Friday - ~4 hours:

- Came up with the idea of building a fully open-source flight computer for amatuer rocketry.  
- Started to put together a team, and started researching parts to use  
- Came up with a rough-plan on what we want out of this and our parts selection (On Tab 1 on all the charts)

Day 2- Saturday - ~3 Hours:

- Finalized parts selections  
- Started work on software

Day 3 - sunday - ~7.5

- discussed potential solutions in order to program all 3 chips with 1 usb-c connector  
- looked into alternatives, and what other people have done  
- looked into additional sensors/regulators that we will use  
- Continued to work on software- developed most of the code for the IMU’s, GPS and stuff.

Day 4 - monday - ~4 hours:

- Figuring out a big bug in the code and  
- final solution for programming   
- working on solution for data/power, and allowing us to flash 3 MCU’s with only one USB-C connector

Day 5 - tuesday - ~6.5 hours (3.5 hours huddle, 2 hours Meddy by himself afterwards, and 1 hour just Liam for software):

- Finished the switch multiplexer stuff.  
- Finished the solution for data/power, and allowing us to flash 3 MCU’s with only one USB-C connector  
- Changed a few small power rail stuff

Day 6 - Wednesday - ~4 hours:

- Built the full schematics for the IMU via SPI to the TMCU/

Day 7 - Thursday - ~4.5 hours from @Scooter Y, 4 hours from @Meddy B:

- Finally finished building the GPS module  
  - Had to figure out how to wire up the antenna, and which one to use (which ended up being the LNA one…)  
- Finished wiring up the radio tuned at 915 MHZ to bypass HAM restrictions including all the SPI magic and the antennas for it  
- Built the schematic for the H-Bridge which is responsible for controlling the servos for the reaction wheel  

- Fixed some net flag issues where I forgot to wire it to the MCU…

Day 9- Saturday- ~8 hdwours from @Scooter Y, @Meddy B, and @Stars:

- Added Bluetooth to the Schematic for making changes to the codebase and flashing it to the MCU’s wirelessly (especially useful on the launch pad for last minute changes). A big   
  Trouble was trying to figure out how to get it to 2.3GHZ. I had to calc π-type to figure out what to use to get it to the right frequency.  



- 

Day 10 - sunday the 18th ~5 hours from @meddy(i worked from 11pm-4am)

- finished layout for pcb and wiring up sensors and putting it on the pcb, although i didnt finish wiring everything to the power rails and mcu. ill finish after i sleep. i need to fix the jtag/swd connectors as well

Day 11 - Thursday 4 hours

- started redoing layout

Day 12 - friday 13 hours

- Started wiring, got stuck and realized the layout was bad so I scrapped it and did it again so I started a new layout

Day 13 - saturday 2 hours

- I realized the layout was bad so I did it one more time

Day 14 - sunday 5 hours

- redid layout, starting wiring and it seems a lot nicer

Day 20 - 06/1  1 hour stars  
Day 21 - 06/2 2 hours stars

- Changed some I2C comms

Day 23 - 06/4 1 hour stars

- Made MMCU send the packet to NMCU

Through every revision it looks very similar because we have an idea of what we want with the end result, but the process of laying out every single part and the specific wiring seems to change so its not really the same every time

Ive worked on it at random misc times and forgot to record  
Day 16(latest day ive acc recorded) 6/1 13 hours

- I completely redid the entire layout. Our first approach was laying everything out and then wiring, whereas with my latest version, I was focused on completing entire parts. Like completely wiring everything for a sensor, before wiring up the next part. I think this approach helped cuz now everything is actually able to fit(except the bootloader pins)  

- finished complete wiring, still need bootloader pins. worst case scenario ill will the wires directly to the mcu  



Day 17 13 hours - 7 hours from Meddy and 6 hours from @Scooter Y:

Today I worked a lot on the routing of the PCB since there were a LOT of issues (450+!)! Today I got it down to only about 80 DRC errors (most of them being garbage, so thats amazing I guess). I also finished routing a lot of the GPS, and all the bootloader pins on 2 sides, and a whole lot of re-routing some vias (definitly a little more than a lot ;)).

Some of the re-routing was done specifially to the TMCU (the MCU on the right side), since most of the RX/TX connections come through this MCU. It was a via-mess, and now it's just bareable.

![image](https://github.com/user-attachments/assets/f70af8d4-baa2-4753-b9be-16f1019343c4)

Day 06/15 - 1 hour yourlocaldndnerd

- filters... :sob: at least we have some rough filters now, all that's left is testing.


**Total hours worked on it so far- \~ hours**  
**Links-**   
[**https://github.com/Horizon-Avionics/Horizon-Avionics-Hardware**](https://github.com/Horizon-Avionics/Horizon-Avionics-Hardware)  
[**https://github.com/Horizon-Avionics/Horizon-Avionics-Software**](https://github.com/Horizon-Avionics/Horizon-Avionics-Software)



goon goon goon
