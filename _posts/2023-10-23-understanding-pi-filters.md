#  Understanding PI filters

This blog post will go over the details of PI-filters. 

## What are PI filters?

PI filter is a low-pass filter, which is widely used in power electronics to attenuate high frequency noise from power supply, which may affect the expected functioning of a particular load circuit. The circuit consists of two capacitors connected in series with an inductor in the middle. 

# What are the key parameters to consider before designing your PI filter?

The design of the PI filter largely depends on the load and the application that it will be used in. The following parameters will determine the design of the PI filter:

- Frequency range to be filtered: Depending on the noise frequency spectrum of your system, the range of high frequency noise can be determined to be filtered out
- Capacitors: In order to build the PI filter, the value of the capacitance of the capacitors should be determined in such a way that they resonate at the frequency that is desired to be filtered out.
- Inductor: Based on the frequency range to be filtered out with the resonant frequency and the chosen capacitor value, the value of the inductor can be determined.
- Type of inductor: The type of inductor used in the PI filter can influence the effectiveness of the PI filter. Given their high permeability, ferrite core inductors are widely used to minimize losses.
- Placement: The PI filter is placed between the power supply and the load circuit to ensure that the noise from the power supply is filtered out before it reaches the load circuit. 

