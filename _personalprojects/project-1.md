---
title: "HP 3245A repair"
excerpt: "Precision source with an ugly power supply <br/><img src='/images/hp3245a.jpg' width='753' height='302'>"
collection: personalprojects
---

I found this HP3245A universal source in semi-functional condition. It has the dual-source option installed rather than the more popular 'high-voltage' amplifier card. The unit turned on and passed all of its main computer self-checks, but could not establish connection with the second source board. Here the installed option proved incredibly useful. Upon disassembly, I discovered a large charred electrolytic capacitor on the second board.

![](/images/hp3245a_fault.jpg)

With some digging around on the internet, I learned that this was the main decoupling capacitor for first on-board power supply, and is a common point of failure. It is rated for over 2 amps of ripple current, a tall order for 30+ year old electrolytics. I removed the capacitor, but still there was a short on the board. I knew from my earlier research that the local supply's transistors (at left in image) sometimes fail, but mine passed all the usual diode checks. Removing the gate resistors helped my isolate the fault to an SG3525A pwm controller, which is thankfully still in production.

With the power supply repaired it functions beautifully, though a GPIB interface and calibration will have to happen sometime.
