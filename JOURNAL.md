Day 1- Friday \- \~4 hours:

- Came up with the idea of building a fully open-source flight computer for amateur rocketry.  
- Started to put together a team, and started researching parts to use  
- Came up with a rough-plan on what we want out of this and our parts selection (On Tab 1 on all the charts)

Day 2- Saturday \- \~3 Hours:

- Finalized parts selections  
- Started work on software

Day 3 \- sunday \- \~7.5

- discussed potential solutions in order to program all 3 chips with 1 usb-c connector  
- looked into alternatives, and what other people have done  
- looked into additional sensors/regulators that we will use  
- Continued to work on software- developed most of the code for the IMU’s, GPS and stuff.

Day 4 \- monday \- \~4 hours:

- Figuring out a big bug in the code and  
- final solution for programming   
- working on solution for data/power, and allowing us to flash 3 MCU’s with only one USB-C connector

Day 5 \- tuesday \- \~6.5 hours (3.5 hours huddle, 2 hours Meddy by himself afterwards, and 1 hour just Liam for software):

- Finished the switch multiplexer stuff.  
- Finished the solution for data/power, and allowing us to flash 3 MCU’s with only one USB-C connector  
- Changed a few small power rail stuff

Day 6 \- Wednesday \- \~4 hours:

- Built the full schematics for the IMU via SPI to the TMCU/

Day 7 \- Thursday \- \~4.5 hours from @Scooter Y, 4 hours from @Meddy B:

- Finally finished building the GPS module  
  - Had to figure out how to wire up the antenna, and which one to use (which ended up being the LNA one…)  
![image](https://github.com/user-attachments/assets/9d6a8c27-5796-4d34-b9ef-efdd3564712b)
- Finished wiring up the radio tuned at 915 MHZ to bypass HAM restrictions including all the SPI magic and the antennas for it  
  ![image](https://github.com/user-attachments/assets/5b0ac2e6-5c25-4ecc-b60c-5264a9529a90)
- Built the schematic for the H-Bridge which is responsible for controlling the servos for the reaction wheel  

- Fixed some net flag issues where I forgot to wire it to the MCU…

Day 9- Saturday- \~8 hours from @Scooter Y, @Meddy B, and @Stars:

- Added Bluetooth to the Schematic for making changes to the codebase and flashing it to the MCU’s wirelessly (especially useful on the launch pad for last minute changes). A big   
  Trouble was trying to figure out how to get it to 2.3GHZ. I had to calc π-type to figure out what to use to get it to the right frequency.  


![image](https://github.com/user-attachments/assets/0d8a23b0-110c-44b4-8bf5-857953e60745)

- 

Day 10 \- sunday the 18th \~15 hours from @meddy and @scooter y (We worked from like 1am to 4am\!)

- Today was a big day for us. We started off with doing some schematic work and adding a lot of the needed footprints like for BL. After that, we did the layout for pcb and wired up sensors and putting it on the pcb, although U didnt finish wiring everything to the power rails and mcu. I (@scooter) started the routing too for the bl chip, along with the cs, sck for rf chip as that takes time since it is a very sensitive ic. ill finish after i sleep. i need to fix the jtag/swd connectors as well.

![image](https://github.com/user-attachments/assets/74b5d807-fdfc-4bd8-b910-4bb6fe9c04ac)
![image](https://github.com/user-attachments/assets/e679b953-6bbf-4cf7-b6e9-b748a3afe3a3)
![image](https://github.com/user-attachments/assets/8060491c-2138-4424-821c-f570ddb1482c)

Day 11 \- Thursday \- May 22nd \- 4 hours

- started redoing layout

Day 12 \- Friday \- May 23rd \- 13 hours

- Started wiring, got stuck and realized the layout was bad so I scrapped it and did it again so I started a new layout. We didn’t have enough space on the PCB to properly route all the sensitive components. Also, idk what we were on, but we also had WAY too many screw terminals, we should only have like 5, not 12\.

Day 13 \- saturday \- May 24th \- 2 hours

- I realized the layout was bad so I did it one more time. Started it- not finished it ;)

Day 14 \- sunday \- May 25th \- 5 hours

- redid layout, starting wiring some more, and this time, it finally seems to be a lot nicer

![image](https://github.com/user-attachments/assets/a090447e-5e8f-4a34-ada4-d034c61e69e3)
![image](https://github.com/user-attachments/assets/18ae5ccf-7f4b-4f82-b95f-9fd85ae01886)

Through every revision it looks very similar because we have an idea of what we want with the end result, but the process of laying out every single part and the specific wiring seems to change so its not really the same every time. For example for this revision, we have the screw terminals on the top to allow more space on the sides for ant’s and stuff.

Day 15 \- May 26th \- 3 hours (@Meddy)

- Don’t really remember what I exactly wired up on this day :pf:, but I did some PCB routing, most likely regarding the MCU routing.

Day 16 \- May 27th \- 4 hours

- Did some more routing on this day- nothing crazy. I mostly re-arranged this github repo’s folders since it was a mess\!

Ive worked on it at random misc times and forgot to record  
Day 17(latest day ive acc recorded) 6/1 13 hours

- I completely redid the entire layout. Our first approach was laying everything out and then wiring, whereas with my latest version, I was focused on completing entire parts. Like completely wiring everything for a sensor, before wiring up the next part. I think this approach helped cuz now everything is actually able to fit(except the bootloader pins). The good thing is even though it was a full re-wiring, the layout was kept very similar, and it was more the way I routed it over the parts placement.  

- finished complete wiring, still need bootloader pins. worst case scenario ill will the wires directly to the mcu  

![image](https://github.com/user-attachments/assets/3878591d-961c-49dd-ad23-56484c3645b2)

Day 18 \- June 2nd \- 5 hours:

- literally just random wiring

Day 19 \- June 3rd \- 6 hours:

- Finished the layout placement ie. all the parts are now all placed now, and just the few left need to be routed, and all the MCU routing. 

Day 20 \- June 4th \- 4 hours:

- Fixes over 200 DRC errors. Now I only have 84 errors left (yay, I guess).... I also wired up the bootloader pins which will be able to be broken off once programmed for the first time. I routed this with Meddy.

Day 21 \- June 5th: maybe 3 hours?

- finally a day without wiring. fixed all drc errors. I started working on the warnings, and then I realized that I could ignore them since they were all about the silkscreens. Instead I only needed to fix the actual errors. I did that. A lot of traces didn't have space between each other since everything is so tightly packed. I cleaned up random misc traces and stuff. Everything should pretty much be good now.

Day 22 \- June 6th: 3 hours:

- So apparently even though we thought there were no DRC errors left, there somehow were :(. For some reason each device said more so we fixed those (which were actual DRC errors, I'm confused.) Nonetheless, we fixed most of the DRC errors.

Day 23 \- June 13th: 3 hours:

- Tided everything up, and finally finished all the hole DRC’s \+ trace spacing DRC’s\!

Day 24 \- 4 hours:

- I fixed the ground pour to be all 4 layers over just the top and bottom since it would be better. I also switched out the BL, and GPS antenna’s to U.FL since apparently SMA antennas for these don’t exist.. I also did some ground stitching around the GPS, BL, and RF since those need to have ground stitching and I didn’t add it yet.

Day 25 \- June 18th \- 10 minutes:

- Added the PCBWAY logo to our board since they will be sponsoring the PCB it seems like.

**Total hours worked on it so far- \~128.6 hours**  
**Links-**   
[**https://github.com/Horizon-Avionics/Horizon-Avionics-Hardware**](https://github.com/Horizon-Avionics/Horizon-Avionics-Hardware)  
[**https://github.com/Horizon-Avionics/Horizon-Avionics-Software**](https://github.com/Horizon-Avionics/Horizon-Avionics-Software)
