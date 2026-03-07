---
title: "HP54602B Repair"
excerpt: "My first oscilloscope <br/><img src='/images/hp54602b.jpg' width='576' height='324'>"
collection: personalprojects
---

The HP 54602B is a 150 MHz 2+2 channel DSO from the mid 1990s. This is one of a pair found in the junk bin, both with intermittent issues. While the other unit's problems seem localized to the front pannel controls, this mine proves more troublesome:
- Channel 1 sometimes works, but there was no logic to when so we can rule out range-switching problems
- Channels 2 and 3 are wholly inoperable.
- Channel 4 seems fine, but with only two vertical ranges it isn't terribly useful.

Of course the next thing to do is take it apart! Below you can see two pictures of the damage on channel 2. It appears the previous owner destroyed the input resistors on channels 1, 2, and 3 (either with high voltage or bad soldering). They had bypassed the input protections on channel 1 and 2 with a bodge wire (not pictured, since the microscope camera would not focus on it). Instead of wiring the input to the left of R379 it was wired to the right, making the spark gap trace useless. Only the channel 1 bypass had series resistance, and evidently the omission led to further damage on channel 2. The burnt component near the bottom is probably an MMBD1503 (or equivalent) dual switching diode, but without schematics for this model of the 54600 series it is hard to be sure. 

![](/images/hp54602b_resistor.jpg)
![](/images/hp54602b_diodes.jpg)

I have ordered new diodes and input resistors, but as with all projects I'm sure another component order will happen at some point.
