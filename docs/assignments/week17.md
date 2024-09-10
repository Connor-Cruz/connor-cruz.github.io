# 17. Project Development

This is an account of progress during the final week of Fab Academy.

## Completed Tasks

Before this week, I was able to have the screen functioning and displaying images on the SD card. I also had files for all of my cuts, including the CNC file for the board outline and the cut for the Guam acrylic and its slot. I had also already cut out the outer box for the board, but I had not yet cut out Guam. I had started designing labels for locations, which I planned to vinyl cut. (Note that I documented this on the week of May 29th). 

I also tried testing the TLE493D hall effect sensors, which worked alone but not with an I2C multiplexer. Along with the screen functioning, I also had the information and images that would be displayed on the screen.

## Remaining Tasks

I still had to actually cut the outline of Guam in both the acrylic and the top wood piece. I was still unsure of whether to cut it with the ShopBot CNC machine or the laser cutter, since it would be difficult for the ShopBot to cut the sharp parts of the outline in the wood, and the laser cutter would nto be able to cut a specific depth with its deep engrave. The acrylic for cutting out Guam had not arrived yet as well. I also needed to finish programming the sensors and assembling everything.

## What Has/Hasn't Worked

I had to go through two different screens. I was able to get one for the Arduino Mega 2560 to work with it, but I couldn't use it with other chips, so I wanted to get a screen that could possibly work with smaller chips. Eventually, I found a screen that was able to work with the Xiao RP2040, which you can find in my Final Project documentation. So far, having multiple TLE493D hall effect sensors has not worked, so I plan to test out new sensors. Everything else is going well.

## Questions Remaining

How can I get the current hall effect sensors to work, and if I can't, then what new ones can I have ship on time and get to work?

Should I laser cut or CNC the cutout for Guam?

If I end up not using the I2C hall effects, will I have enough pins on the Xiao to support all of the sensors?

## Plans for Remaining Time

Here are the remaining tasks and the approximate time they should take up. Note that they are in roughly chronological order.

General:

- Test new sensors: 2-3 hours
- Design sensor board: 30 minutes
- Assemble sensor boards x 8: 1 hour
- Cut Guam outline in wooden board: 2 hours
- Cut spare top of box in case of failure: 30 minutes
- Cut Guam acrylic with cardboard: 30 minutes
- Cut Guam acrylic on scrap acrylic: 30 minutes
- Cut Guam acrylic in Green: 10 minutes
- Design main board for microcontroller(s): 1 hour
- Mill main board: 45 minutes
- Test main board: 1 hour
- Laser cut project name on board: 30 minutes
- Program sequence of pictures for each sensor: 3 hours
- Connect a power source to main board: 1 hour

Assembly

- Glue sides and bottom of box: 45 minutes
- Affix acrylic Guam to board: 15 minutes
- Affix display to board: 15 minutes
- Affix sensor boards to acrylic: 15 minutes
- Affix main board to top of box: 10 minutes
- Affix power source to top of box: 20 minutes
- Cut stickers for board: 1.5 hours
- Affix stickers: 1 hour

## What Have I Learned?

I have definitely learned a lot more about different protocols. Dr. Adam Harris helped me understand I2C in more depth, as well as teaching me how to use a logic analyzer to see where communications might go wrong and to generally analyze communication between devices. Programming the screen has also taught me the SPI protocol. I have also learned that things might not go according to plan and that many problems might arise, so I need to give myself extra time in future projects to account for this.

**Note: You can see my detailed documentation on my Final Project page.**