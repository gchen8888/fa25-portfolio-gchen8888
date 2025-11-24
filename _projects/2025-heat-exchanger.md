---
layout: project
title: Analysis of Heat Exchanger
description: Heat Exchanger Analysis on Counterflow vs Parallel Flow
technologies: [MATLAB, python]
image: /assets/images/IMG_1828.jpeg
---

## Heat Exchanger Analysis

This project analyzes the performance of a small water-to-water heat exchanger operated in **counterflow** vs **parallel flow** setup. Experimental data was collected using two pumps, four water reservoirs, an immersion heater, ice, thermocouples, and dye for flow tracing.

## Photos 

![Heat exchanger setup]({{/assets/images/IMG_1826.jpeg|relative_url}})
![Flow Schematic](/assets/images/IMG_1830.jpeg)


## Description of the Heat Exchanger

A heat exchanger transfers thermal energy between two fluid streams passing through one another without mixing.  

In my experiment, there are: 
- **Hot stream:** Water heated by an immersion heater  
- **Cold stream:** Water cooled by ice   
- **Two pumps** circulate the fluids  
- The heat exchanger has **four labeled ports** 1, 2, 3, 4

This experiment focuses on comparing: 
- **Counterflow:** fluids move in opposite directions  
- **Parallel flow:** fluids move in the same direction

Real-world examples of heat exchanger include:
- Radiator in a car
- Coils at the back of a refrigerator

### System Diagram 
I treat this heat exchanger as a **control volume** system. Assume it's at steady state, adiabatic (no heat loss to surroundings), and no work other than flow work of the two streams (hot, cold). Assume changes in kinetic and potential energy are negligible.

As shwon here: 
![Control volume system for the two flows](/assets/images/IMG_1094.jpeg) 

- Energy is transferred only between the two streams, not to the environment.
- No work interactions occur.

### Mass balance 
With assumption of steady state: 
![Mass balance equation](/assets/images/IMG_1095.jpeg)

### Energy balance 
With assumption of steady state: 
- Adiabatic: Q = 0
- Only flow work: W = 0
- Negligible KE and PE changes

Cosnider both flows: 
![Energy balance equation (both flows)](/assets/images/IMG_1096.jpeg) 

Cosnider one flow as a system: 
![Energy balance equation (one flow)](/assets/images/IMG_1097.jpeg) 

### Entropy Balance 
With assumptions
- Steady state 
- Adiabatic: Q = 0
- No mixing
- Must be >= 0
![Entropy balance equation](/assets/images/IMG_1098.jpeg) 




## Experimental Data

#### Counterflow Test 1
**Inflow**
- Hot: 34.9°C  
- Cold: 3.9°C  

**Outflow**
- Hot bin: 17.7°C  
- Cold bin: 21.5°C  


#### Counterflow Test 2
**Inflow**
- Hot: 34.6°C  
- Cold: 7.6°C  

**Outflow**
- Hot bin: 19.6°C  
- Cold bin: 22.8°C  

---

#### Parallel Flow Test 1
**Inflow**
- Cold: 5.4°C  
- Hot: 35.0°C  

**Outflow**
- Cold bin: 17.8°C  
- Hot bin: 21.3°C  

#### Parallel Flow Test 2
**Inflow**
- Cold: 7.3°C  
- Hot: 34.8°C  

**Outflow**
- Cold bin: 18.5°C  
- Hot bin: 21.9°C  


## Analysis

### Reason for a larger temperature differences in counterflow setup
In counterflow, the coldest cold water (at the outlet) meets the hottest hot water (from hot inlet).  
This maintains a **high temperature difference** along the entire heat exchanger, which leads to a high heat transfer rate. 
Meanwhile, parallel flow quickly loses temperature difference, as both flows go in the same direction, with smaller temperature differences along the way, so heat transfer becomes inefficient halfway through the exchanger.


## Real-World Considerations
- The heat exchanger in lab was **not perfectly adiabatic**.  
- Some heat is lost to the room. 
- The system may not reach true steady state. 
- Pumps introduce kinetic energy changes, although it might be small relative to thermal effects. 

In real devices, insulation is needed to eliminate these effects.

## Conclusion
Counterflow operation produced **larger temperature changes** and **more effective heat transfer** than parallel flow. This matches thermodynamic expectations and is helpful to keep in mind for real-world engineering design principles.

