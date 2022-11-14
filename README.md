#Yet Another Lego Saturn V Launch Effect

I am showing how I created a Lego Saturn V Launch effect. I know that it has been done a thousand times and I’m not the first but this is my take on it!

[Lego](https://www.lego.com/en-gb/product/lego-nasa-apollo-saturn-v-92176) is going to retire this model soon so I knew I had to get one before I was at the mercy of the second-hand market. 

Many people use the [IKEA DETOLF](https://www.ikea.com/gb/en/p/detolf-glass-door-cabinet-white-80269122/) glass door cabinet to display the model once they have created the launch effect, using the whole height of the cabinet to really show off the effect, but I wanted to keep the top shelf for a couple of other Lego models so I needed to create and use a short stand.

![The before picture](https://github.com/sergeibuilds/LegoSaturnVLaunch/blob/main/pictures/1_before_picture.jpg)

I design and printed a stand that consisted of an inner core that would have the LED’s wrapped around it, an outer, translucent wall that the cotton wool would stick to and a top and bottom lid to hold it all together.
I printed the base and inner tube in black PLA, the outer wall and top lid were printed in translucent PLA. The outer wall was printed in vase mode with no top or bottom so it printed as a tube.
I also used a Pimoroni Plasma 2040 to control and drive a 1 metre length of WS2812 addressable flexible strip of LED’s, I used a 60 pixels per metre strip.

![The parts](https://github.com/sergeibuilds/LegoSaturnVLaunch/blob/main/pictures/8_the_parts.jpg)

Assembly was simply a case of glueing the inner core to the base

![The base](https://github.com/sergeibuilds/LegoSaturnVLaunch/blob/main/pictures/2_initial_assembly.jpg)

Wrapping the LED strip around the core

![Adding LEDs](https://github.com/sergeibuilds/LegoSaturnVLaunch/blob/main/pictures/3_adding_leds.jpg)

Putting on the outer wall and top lid and gluing them to the other parts. I cut a small notch in the outer wall for the wires to pass through and then powering them on to ensure they work.

![Final assbembly and test](https://github.com/sergeibuilds/LegoSaturnVLaunch/blob/main/pictures/4b_final_assembly.gif)

I used some spray glue on the outer wall and then put the stand in the bottom of the cabinet, stood the model on it and added a load of pillow stuffing to simulate the exhaust plume.

![Final picture](https://github.com/sergeibuilds/LegoSaturnVLaunch/blob/main/pictures/5_after_picture_off.jpg)

Then I turned off the lights and admired the effect!

![Final effect](https://github.com/sergeibuilds/LegoSaturnVLaunch/blob/main/pictures/7_final_effect.gif)

The Pimoroni Plasma 2040 is a great little dev board that is designed specifically for addressable LED’s so using this made coding very simple, I simply used their random-blinkies example from their [GitHub](https://github.com/pimoroni/pimoroni-pico/tree/main/micropython/examples/plasma2040) page and changed just 4 settings; Number of LED’s to 60 to match my strip, the Hue Start and Hue End values to get a range of red/yellows that I was happy with and the Speed to make them a bit faster.

I used Micropython on my Plasma 2040 instead of Circuitpython as I found the random-blinkes example almost perfect for my use case.

