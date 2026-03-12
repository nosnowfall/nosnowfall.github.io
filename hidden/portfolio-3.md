---
title: "Capacitive water heater"
excerpt: "Using wireless power transfer for direct heating <br/><img src='/images/waterimpedance.png' height='320' width='426'>"
collection: portfolio
---

This one is still very much a work in progress, but the basic idea is to use the slight conductivity of fluids with electrolytes (like salt water) to heat them via wireless power transfer. Typical fluid processing involves contact heating through a heat exchanger, of which there are many kinds. A common thread among those is that estimating the delivered power is difficult, and evenly heating the bulk of the fluid requires mechanical complexity. This work draws inspiration from heating methods commonly used in food processing, where bulk heating and sterility are important.

We use a nonconductive container for the fluid and capacitively couple from the outside to the ions in the fluid itself. Driving current through this coupling can generate bulk ohmic heating in the fluid. As in my other work, I make use of resonant converters and tunable compensation networks. Here is a sample of measured load impedance vs. frequency with a variety of coupling methods:

![](/images/waterimpedance.png)

A publication is forthcoming, but I can say that the method is verified and with the right parameters 100+ Watts of heating can be achieved.
