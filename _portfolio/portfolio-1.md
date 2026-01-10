---
title: "10 MHz full bridge inverter"
excerpt: "Two 100 V GaN half bridges designed for off-board resonant loads.<br/><img src='/images/mvfb_side.png'>"
collection: portfolio
---

![](/images/mvfb_side.png)

This board was designed to support both of my research projects by operating at either 6.78 or 10 MHz with a series resonant load. I started with four key criteria:
- minimize switching loop inductance
- minimize gate drive power, dead time, and switching times
- minimize logic-chain propagation delay
- design for low-voltage, high-current operation

Loop inductance is mostly a result of semiconductor packaging and pcb layout and I knew from the start I would be using GaN HEMTs, so I kept layout in mind as I selected the rest of the components. Resonant gate drives are gaining popularity in high frequency converter research but they don't readily support the rapid on/off/on/off control necessary for the antenna amplifier, so I opted for a fast standard drive topology. This in mind, I selected the IGB110S10S1 from Infineon, a 100 V GaN device with only 3.4 nC gate charge and top-side cooling.

Another antenna project limitation is the need for galvanic isolation between the control and power circuits. This raises the minimum logic delay and results in three dead time options:
- isolated half-bridge driver
  - driver with integrated dead time
  - logic-side dead time circuit
- dual isolated drivers with a logic-side dead time circuit
- digital isolator with a non-isolated half bridge driver
  - driver with integrated dead time
  - separate dead time circuit (either side of the isolator)
 
The fastest isolated driver options come from Infineon, MPS, or Skyworks with 35-50 ns typical propagation delay. Those with integrated dead time did not go below 10 ns, and with only single driver outputs they offered no advantage over the dual-output single isolated drivers. Separating the isolation and gate drive allows much faster components for both, the best for my use case being the LMG1210 driver and MAX12930 isolator, for a combined 15-25 ns delay depending on operation mode. 

And finally, a top-down view of the final product.
![](/images/mvfb_top.png)
