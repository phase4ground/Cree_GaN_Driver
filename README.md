# Cree GaN Gate Driver and Power Sequencer.
A general purpose GaN gate driver board based on [Cree APPNOTE-011 Rev. B](https://github.com/kf4mot/Cree_GaN_Driver/blob/master/docs/gan_hemt_biasing_circuit_with_temperature_compensation.pdf).
Provides about 2 ms of delay after power is good before switching on the mosfet. Switch off during power fail or shut down is nearly instant.

**Incomplete. Tested with DC load for function and power sequencing only.**

**Things worth knowing**

1. If operating at 14 Volts or less then R10 should be decreased from 4.7KΩ to 1KΩ.
1. C8 value can change per installation, or is optional. A though hole electrolytic soldered to the adjacent power pads is also a convenient option for bulk capacitance.
1. Infineon SPD15P10PL G can be used as a alternate mosfet. **Untested**
1. The series resistance that is R11, R13, and RV1 is there for hackability. Allowing for GaN's with differing gate voltage requirements and to have the ability to use fixed resistors for preventing voltage shift.

   

[Schematic](https://github.com/kf4mot/Cree_GaN_Driver/blob/master/hardware/Cree_GaN_Driver.pdf)

[Licensed under CERN-OHL-S V2. Julian White, 2020](https://www.ohwr.org/project/cernohl/wikis/home)

![First!](https://github.com/kf4mot/Cree_GaN_Driver/blob/master/images/IMG_20200329_075126953.jpg "First Board")

Ch.1 is drain. Ch.2 is gate.

![First!](https://github.com/kf4mot/Cree_GaN_Driver/blob/master/images/gan-bias-pwr-up-clean.jpg "Normal Power Up")

![First!](https://github.com/kf4mot/Cree_GaN_Driver/blob/master/images/gan-bias-dirty.jpg "Power Fail at Power Up")

![What does this do?](https://github.com/kf4mot/Cree_GaN_Driver/blob/master/images/gan-bias-pwr-down.jpg "Normal Turn Off")
