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

# How to design PI filters without measuring the noise frequency spectrum of your system?

In order to be able to design the PI filter, the noise frequency spectrum of the system needs to be determined. This can be done by the following hints below:

1. Determine high frequency generating components: Determine any high frequency noise generating components in your circuit. This, for example, could be the clock frequency of your microcontroller, which could be estimated from the datasheet. In case of existence of multiple high frequency components, a wide range of frequencies may be needed to be filtered. 
 
2. Establish the frequency range to filter: Depending on the frequency determined in 1, the range of frequency to be filtered out can be determined. A guideline would be to design the filter to attenuate frequencies 10 times higher than the switching frequency. Hence, the resonant frequency can be determined. This is the frequency at which the PI filter would resonant and create a low-impedance path to ground for noise. 

3. Choose capacitor and inductor values: The following equation can be used to determine the capacitor and inductor values C = 1 / (4 * pi^2 * L * f^2)

4. Simulate: A good rule of thumb is to simulate your filter using a circuit simulation tool to ensure its performance. You can alter the values of the components to attain the desired performance



