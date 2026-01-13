---
title: "Keithley 580 Micro-Ohmmeter"
excerpt: "Short description of portfolio item number 1<br/><img src='/images/k580.jpg' width='432' height='324'>"
collection: personalprojects
---

![](/images/k580.jpg)

This is the meter that started it all. I found it in the UW-Madison SWAP with three other vintage meters and a sticky note claiming they were defective. I was not particularly interested in the others (they have worse specs than my handheld meter) but I found the Keithley 580 intriguing.

It only measures resistance, and only to 4.5 digits, but it does so with fascinating limitations and clarity of purpose. The limitations I don't find bothersome: max 200 kOhm, and 4-wire measurements only. This is a precision low resistance instrument, after all. But the other features are what I like about it:
- the test current is explicitly stated for every range
- it has a dry-circuit mode (more on that later)
- it has a relative/offset function
- you can easily choose the drive polarity and single shot measurements

### A quick aside about the repair
The buttons were worn out. They are made from rubber with some sort of conductive film applied on the back, and they make contact with bare traces on the display PCB. I could not source new conductive paint, so I simply backed the buttons with thin copper shielding tape. I expect this will eventually wear out the PCB traces, but the buttons are not pressed very often.

### Back to the reasons I like this meter
The relative/offset function is very useful - no more math in my head about which trace or grounding path is shorter. Known test current limits are great for sensitive applications with a current limit, though I have none at the moment. The single shot and default pulsed measurements both take care of auto-zeroing the meter *and* keep the workpiece from heating up too much. And because the drive current is bipolar (with the option for unipolar), it can either prevent charge buildup on capacitive elements *or* determine if a resistor is not truly bipolar.

Lastly, the dry circuit mode. The internal current source has a high open-circuit voltage, which might for example eat through oxide layers on a corroded relay contact. Dry circuit mode limits the output to 20mV, allowing reliable checks for bad contacts in an otherwise low-resistance path. This is a fantastic feature, and I even used it when repairing my KLH-51 stereo receiver (which does not have an article here).
