## Understanding Reverse Polarity Circuits

This blog post will go over the details and different ways of implementing a reverse polarity circuits. 

## Why are reverse polarity protection circuits required?

Reverse polarity protection is necessary in order to ensure that no damage occurs to the protected components in a given circuit when the polarity of the supply voltage reverses.

## Standards for reverse polarity protection

> [ISO 16750-2:2023](https://www.iso.org/standard/76119.html) provides detailed requirements for reverse battery protection in terms of voltage levels and timings to ensure that the electronic equipment can withstand reverse battery voltage without getting damaged or malfunctioning. 
>
> The standard specifies that the electronic equipment should be able to withstand a reverse voltage of up to ***60V for a period of 100ms***. This means that the equipment should not be damaged or malfunction when a reverse voltage is applied to it for a period of 100ms. 
>
>It's worth noting that the standard requires testing of the equipment under reverse voltage conditions at both room temperature and elevated temperature to ensure that the equipment can withstand reverse voltage under different temperature conditions.
>
>Additionally, the standard recommends that the duration of reverse voltage testing should be increased to 1s for electronic equipment that is critical to the safety of the vehicle or its occupants. This means that electronic equipment that is critical to the vehicle's safety or the safety of its occupants should be able to withstand reverse voltage for a longer period of time without getting damaged or malfunctioning.
>
>Therefore, the standard provides detailed requirements for reverse battery protection in terms of voltage levels and timings to ensure that the electronic equipment can withstand harsh environmental conditions and unexpected events such as reverse battery connection, especially for critical systems.

*Source: GPT3.5*

## Designing a reverse polarity protection circuit

Before we dive into designing the actual reverse polarity protection circuit, it is important to have an overview on the application that the circuit will be designed for to be able to select the corresponding components. Below is a list of parameters of the components, which will be used to design the reverse polarity protection circuit, to bear in mind. 

- Voltage and current ratings
- Power loss and efficiency
- Switching speed
- Temperature range
- Size
- Cost
- Compatibility with other components
- Reliability and durability



## Different types of implementation of reverse polarity protection

Several different components could be used for implementing a reverse polarity protection circuit. These components include, but are not limited to Schottky diode, P-channel MOSFETs, N-channel MOSFETs, Transient-voltage-suppression (TVS) diodes, automotive-grade reverse polarity protection ICs and fuses.

The table below gives you an overview of the different types of components that can be used to implement reverse polarity circuit with reference to the parameters listed above.

---
| Features	| Schottky Diodes	| P-Channel MOSFETs	| N-Channel MOSFETs	| TVS Diodes	| Automotive-grade Reverse Polarity Protection ICs	| Fuses|
| ---------- |  ------------ | ------------ | ---------- |  ------------ | ------------ | ---------- | 
| Voltage rating	                    | Low to moderate	| High	| High	| High	| High	| High | High |
| Current handling capability	        | Moderate	| High	| High	| Moderate to High	| Moderate to High	| High |
| Power loss	                        | Low	| Low	| Low	| Moderate	| Moderate to high	| Low |
| Efficiency	                        | High	| High	| High	| Moderate	| Moderate to high	| High |
| Switching speed	                    | High	| High	| High	| Fast	| Fast	| Slow |
| Temperature range	                    | Limited	| Wide    | Wide	| Wide	| Wide	| Wide |
|Size	                                | Small	| Small	| Small	| Small	| Small	| Small |
| Cost	                                | Low	| Moderate to high	| Moderate to high	| Moderate	| High	| Low |
| Reliability and durability	        | High	| High	| High	| High	| High	| High |
|Compatibility with other components	| Compatible with most components. Can be placed in series with the load to prevent reverse voltage from reaching the circuit	| Requires additional components such as a fate driver and a voltage shifted to ensure proper function	| Requires additional components such as a gate driver and a voltage shifted to ensure proper function	    | Compatible with most components	| Compatible with most components	| Compatible with most components |
---


### Reverse polarity protection circuit - Visual representation

- [ ] Add schematics for all the components
