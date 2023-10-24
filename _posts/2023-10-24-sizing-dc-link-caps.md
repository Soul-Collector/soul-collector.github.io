#  Sizing DC link capacitors

This blog post will go over the details of how to size the DC-link capacitor 

## Why do we need DC link capacitors?

DC-link capacitors are of essence in most power electronics systems. They serve several functions:

- Energy storage: DC link capacitors serve as energy storage components, which are able of supplying energy smooth out the voltage ripple in DC bus. This ensures that the voltage level is maintained at a constant level, which in turn, ensures smooth operation of the intended application. 

- Filtering: DC link capacitors behave as filters and remove high-frequency noise and spikes in the voltage. This ensures that the noise from the supply does not interfere with the operation of the application. 

- Voltage regulation: DC link capacitors aid in reducing the voltage fluctuation. Hence, ensure a stable operating voltage. 

- Surge protection: Surges or voltage spikes may occur during operation and could damage components in a system. DC-link capacitors can act as surge protection, with their ability to absorb any surges or voltage spikes that may occur in the system.

# How to size DC link capacitors?

The selection and sizing of the capacitor depends on several factors. Below are some guidelines to follow when sizing DC link capacitors:

1. Determine the maximum voltage and current requirements of the system
2. Determine the required energy storage, based on application requirements
3. Calculate the value of capacitance required with the help of the following formula: E = 0.5 x C x V^2, where E is the energy in joules, C is the capacitance in farads, and V is the voltage across the capacitor.
4. Select a capacitor value slightly higher than the value that is calculated value to warrant the desired energy storage.
5. Ensure that the temperature rating of the capacitor is higher than the operating temperature of the application

Below is an example for sizing a DC link capacitor intended for a BLDC motor application operating at maximum of 48 V and maximum of 10 A. <br/> 
Typically, energy storage for BLDC motors is about 10 joules. Hence, the value of teh capacitance can be calculated in the following manner: <br/>
C = 2E / V^2 <br/>
C = 2 x 10 / 48^2 <br/>
C = 8.68 x 10^-6 F <br/>

Hence, the capacitance of the DC link capacitor should be at least 8.86 microfarads with an appropriate thermal rating.

## How to decide between electrolytic or ceramic capacitors?

The decision between electrolytic and ceramic capacitor depends on the application requirements of the system. 






