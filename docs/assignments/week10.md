# 10. Mechanical Design

This week I worked on designing a machine with a group.

In this week, I worked with Angelina Yang, Kabir Nawaz, and Alana Duffy. We decided to make a claw machine.

Our group page can be found [here](https://fabacademy.org/2024/labs/charlotte/assignments/week10a/).

## Stepper Motors

I contributed by making our stepper motors work with an Arduino Uno and a CNC shield. Note that this was modified by Kabir to integrate with the other electronics.

Since we wanted to have the claw move on X and Y axes (and eventually make the claw move on the Z axis), we chose to use stepper motors due to their precision.

When I initially tried to program them, I did not know where to start, so I followed [this tutorial](https://www.youtube.com/watch?v=zUb8tiFCwmk). It detailed how to program the motors to move using a CNC Motor Shield on an Arduino Uno.

Luckily, our lab already had all of the components we needed to make the motors function: a CNC shield, a 12V power supply, wires to connect to the shield, and stepper motors (Creality 42-34).

The CNC shield was able to be placed directly on the pins in the Arduino Uno. I then checked the minimum voltage drop for the corresponding motor drivers, which was approximately 8.5V. I changed it to approximately 8.6 V using a flathead screwdriver and checked the voltage with a multimeter.

Unlike other groups from our lab, we did not use GRBL. You can find more detailed documentation on this on the group site.

## First Gantry

I also primarily designed the first gantry we used, including the outside pieces and the two pieces that would hold the middle t-slot. However, due to complications with making the machine square and the reliability of 3D printed parts, this design was scrapped.

Since the two sides of the gantry were too long to fit on the printing bed, I made the decision to join multiple pieces together via screws. In hindsight, this was probably a bad decision since the screws not being fully fastened could allow for some error with the machine.

Also, I did not include guides for the t-slots, so they were able to rotate somewhat easily and therefore made the machine not square. We eventually tried to resort to using super glue to affix them, which somewhat worked, but it was still unreliable with the stress that the system would endure.

You can find images and more documentation on the faults and attempts made for this gantry on the group page.

## Final Gantry

I also helped to find the second gantry design, which was used by our colleagues who made the Ouija Board. Note that this design can be found [here](https://www.diymachines.co.uk/kinetic-sand-art-coffee-table-self-drawing), although there were modifications made since our project has a z-axis and thus a different design for the middle piece.

I very much helped with assembly of all components for both gantries, such as screwing in components, creating and expanding shelves to hold the gantry, and creating some of the 3D printed parts. I also worked on finding and obtaining the pulleys and other items that would be used with the gantry.

I primarily cut the linear rails that were used for the final gantry's movement and the one that was used for stability for the Z-axis. This was a hard task since there are not any machines that can cut metal in our lab at the moment. I used a diamond bit on a dremel to cut the rail, and I used a grinding stone to chamfer the edges to allow for easier insertion of sliding pieces and to make the rail as flat as possible.

Once again, for all of these topics, you can find more detailed documentation and images on the [group site](https://fabacademy.org/2024/labs/charlotte/assignments/week10a/).

## Reflection

This week (which took a fair bit longer than a week to complete) made me realize how hard it is to design a working machine. Working on the individual components, I realized how many problems can be encountered with the various components involved and especially how crucial it is for a machine to be almost exactly square for it to even function. I was very satisfied with the final product since it took so long for those problems to be resolved, and it came out very well. Everything seemed to be stable, and every component of the project worked consistently. Although I likely do not plan on creating another machine of a similar scale in the future, I believe that I have learned the most out of this week. It enhanced my troubleshooting skills, time management skills, and perseverance for future projects.

## Credits

Thanks to all of my group members for continuing to work on the project despite its many failures. Also, thanks to Garrett for his consistent help and advice throughout the development of the project. All other credits are mentioned where they are used to respectively.