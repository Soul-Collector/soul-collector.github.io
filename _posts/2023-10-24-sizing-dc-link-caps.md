#  Sizing DC link capacitors

This blog post will go over the details of how to size the DC-link capacitor 

## Why do we need DC link capacitors?

DC-link capacitors are of essence in most power electronics systems. They serve several functions:

- Energy storage: DC link capacitors serve as energy storage components, which are able of supplying energy smooth out the voltage ripple in DC bus. This ensures that the voltage level is maintained at a constant level, which in turn, ensures smooth operation of the intended application. 

- Filtering: DC link capacitors behave as filters and remove high-frequency noise and spikes in the voltage. This ensures that the noise from the supply does not interfere with the operation of the application. 

- Voltage regulation: DC link capacitors aid in reducing the voltage fluctuation. Hence, ensure a stable operating voltage. 

- Surge protection: Surges or voltage spikes may occur during operation and could damage components in a system. DC-link capacitors can act as surge protection, with their ability to absorb any surges or voltage spikes that may occur in the system.

## How to decide between electrolytic or ceramic capacitors?

The decision between electrolytic and ceramic capacitor depends on the application requirements of the system. 

<!-- | Feature | Electrolytic capacitors | Ceramic capacitors |
| -------- | -------- | -------- |
| Capacitance values | Have higher capacitances values | Lower capacitance values |
| Energy storage | Support high energy storage due to high capacitance values | Low energy storage, suitable in high-frequency filtering applications |
| Voltage rating | Higher voltage ratings | Lower voltage ratings |
| Size | Larger size | Compact size |
| AC/DC circuits | Electrolytic capacitors are polarized, i.e., they have positive and negative terminals. Hence, they are unsuitable in AC circuits | Ceramic capacitors are non-polarized. Hence, can be used in both AC and DC circuits |
| Temperature stability | Lower temperature stability | Higher temperature stability | -->

<table>
    <thead>
        <tr>
            <th>Feature</th>
            <th>Electrolytic capacitors</th>
            <th>Ceramic capacitors</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>Capacitance values</th>
            <td>Have higher capacitances values</td>
            <td>Lower capacitance values</td>
        </tr>
        <tr>
            <th>Energy storage</th>
            <td>Support high energy storage due to high capacitance values</td>
            <td>Low energy storage, suitable in high-frequency filtering applications</td>
        </tr>
        <tr>
            <th>Voltage rating</th>
            <td>Higher voltage ratings</td>
            <td>Lower voltage ratings</td>
        </tr>
        <tr>
            <th>Size</th>
            <td>Larger size</td>
            <td>Compact size</td>
        </tr>
        <tr>
            <th>AC/DC circuits</th>
            <td>Electrolytic capacitors are polarized, i.e., they have positive and negative terminals. Hence, they are unsuitable in AC circuits</td>
            <td>Ceramic capacitors are non-polarized. Hence, can be used in both AC and DC circuits</td>
        </tr>
        <tr>
            <th>Temperature stability</th>
            <td>Lower temperature stability</td>
            <td>Higher temperature stability</td>
        </tr>
    </tbody>
</table>


## How to size DC link capacitors?

The selection and sizing of the capacitor depends on several factors. Below are some guidelines to follow when sizing DC link capacitors:

1. Determine the maximum voltage and current requirements of the system
2. Determine the acceptable voltage ripple
3. Calculate the DC link capacitor value using teh following equation: 
<br/> 
    C = (I x t) / Vripple = I / (f x Vripple)

    where, 
    <br/> C is the capacitance in Farads,
    <br/> I is the maximum current draw of the motor in amps,
    <br/> t is the period of the voltage ripple (usually taken as the inverse of the switching frequency of the motor controller), 
    <br/> and Vripple is the desired voltage ripple on the DC link

### Is there an example?

Certainly all the things in the world are much simpler to understand with the help of an example. 

So let's take an example for sizing of DC link capacitors fot a motor control application. Let's assume the following before we proceed:
 - The maximum current drawn by the motor is around 10 A
 - DC link voltage is 12 V
 - The acceptable voltage ripple is 10% of the DC link voltage, i.e., 1.2 V
 - The switching frequency of the motor control is 20 kHz

 Hence, 
 <br/> C = 10 A / (20 kHz x 1.2 V) = 416 microfarad




