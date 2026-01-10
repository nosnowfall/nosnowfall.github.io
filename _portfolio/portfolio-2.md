---
title: "Phase-correct hysteresis controller"
excerpt: "Amplifier envelope controller that preserves phase-shift keying <br/><img src='/images/hysteresis_blockdiagram.png'>"
collection: portfolio
---

The goal is regulation of our non-LTI amplifier output power for root-raised-cosine pulse shaping. Prior work in the project was done with unregulated square pulse shapes, which allowed high symbol rates but did not suppress undesirable out-of-band radiation. The control scheme is similar in spirit to envelope elimination and restoration (EER) as proposed by Leonard Kahn, in that we separate the phase/frequency data modulation from pulse shape in order to drive a nonlinear amplifier. The system is optimized for phase-shift keying, and the current transmit symbol determines the phase of the carrier-frequency clock sent to the gate driver. Pulse width modulation is incompatible with RF class-D amplifiers (series resonant half- or full-bridge, not the audio kind) since departures from 50% duty prevent soft switching. This controller therefore uses hysteresis, or bang-bang control.

Whereas Kahn's and most contemporary EER systems rely on feedforward or predistortion, can be optimized for a known load, e.g. 50 ohms. Ours is a closed-loop controller because it automatically accounts for deviations in load impedance arising from the electrically small antenna and single-element compensation network. The controller block diagram is below:

![](/images/hysteresis_blockdiagram.png)
