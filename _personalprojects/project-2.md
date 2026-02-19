---
title: "Keithley 2000 repair"
excerpt: "6.5 digit multimeter with a simple ADC failure <br/><img src='/images/k2000_front.jpg' width='438' height='330'>"
collection: personalprojects
---

![](/images/k2000_front.jpg)

I was excited to find this meter, since I'd been using a Keithley 2700 for research projects and loving the feature set. This one reported a pretty generic ADC failure code on startup, so I got straight to disassembly. The K2000 uses a form of multislope integrator ADC and unlike the more famous HP3458A, most of the circuit is made from discrete components. I got to measuring and eventually found the integrator was latched to the positive supply. The integrator here is a composite of two op amps, shown center in the photo below:

![](/images/k2000_inner.jpg)

It didn't seem to respond to any change of input either outside or inside the composite. Not knowing which chip was defective and in the interest of time, I simply replaced them both. Now that I'd fixed it, I went ahead and replaced all of the electrolytic supply capacitors as a precaution - I want this meter to last. I don't yet have a way to calibrate it, but most of the measurements compare favorably with newer 6.5 digit meters in the WEMPEC lab, including the 2700. I recently found a multiplexer card compatible with this unit, which puts me one step closer to using its full scanning meter capability.

---
February 2026 update: the RS232 converter has gone haywire. This is apparently a failure for older Keithley 20xx main boards, stemming from bad level shifter implementation. The RTS line (DB-9 pin 7) is connected to an output pin (pin 7) of the ADM202 level shifter. This pin should be controlled by the host terminal or computer rather than the instrument. Attempting to drive the line high or low (depending on the K2000 software revision) makes the ADM202 fight with the level shifter on the other side of the line and eventually one of them loses. The ADM202 has a weak charge pump compared to most USB-RS232 converters and eventually loses control over its output voltage on all of the Tx lines. Thankfully mine had not been connected to an active RS232 adapter very often, and lifting pin 7 solved the issue. This does make flow control unusable, but I don't expect to need it.
