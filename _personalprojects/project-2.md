---
title: "Keithley 2000 repair"
excerpt: "6.5 digit multimeter with a simple ADC failure <br/><img src='/images/k2000_front.jpg' width='438' height='330'>"
collection: personalprojects
---

![](/images/k2000_front.jpg)

I was excited to find this meter, since I'd been using a Keithley 2700 for research projects and loving the feature set. This one reported a pretty generic ADC failure code on startup, so I got straight to disassembly. The K2000 uses a form of multislope integrator ADC and unlike the more famous HP3458A, most of the circuit is made from discrete components. I got to measuring and eventually found the integrator was latched to the positive supply. The integrator here is a composite of two op amps, shown center in the photo below:

![](/images/k2000_inner.jpg)

It didn't seem to respond to any change of input either outside or inside the composite. Not knowing which chip was defective and in the interest of time, I simply replaced them both. Now that I'd fixed it, I went ahead and replaced all of the electrolytic supply capacitors as a precaution - I want this meter to last. I don't yet have a way to calibrate it, but most of the measurements compare favorably with newer 6.5 digit meters in the WEMPEC lab, including the 2700. I recently found a multiplexer card compatible with this unit, which puts me one step closer to using its full scanning meter capability.
