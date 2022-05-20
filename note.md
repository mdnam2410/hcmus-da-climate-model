# Climate Modeling - Predicting Earth Temperature

## Outline
1. Background: Ordinary Differential Equation
2. Background: Climate Physics

   2.1. Absorbed Solar Radiation
   2.2. Outgoing Thermal Radiation
   2.3. Greenhouse Effect
   
## Requirements
1. Build a model for predicting temperature using Python
2. Predict temperature change in 2030
3. Compare the result with NASA's observation

## Submission
1. One notebook file. Make sure the result is reproducible.
2. A Data directory containing relevant data

# Researching
## Zero-dimensional models
_From article Climate model (Wikipedia)_

### Radiative equilibrium of the Earth:

$$\text{Incoming energy from the Sun} = \text{Outgoing energy from the Sun}$$
$$(1 - a)S\pi r^2 = 4 \pi r^2 \epsilon \sigma T^4$$

where:
- $S$: solar constant - incoming solar radiation per unit area - 1367 W/m^2
- $a$: Earth's average albedo - 0.3
- $r$: Earth's radius - 6.371e6 m
- $\sigma$: Stefan-Boltzmann constant, about $5.67\times 10^{-18}  JK^{-4}m^{-2}s^{-1}$
- $\epsilon$: effective emissivity of Earth, about 0.612

This gives the temperature of Earth:

$$T^4 = \frac{(1 - a)S}{4\epsilon\sigma}$$

$a$ and $\epsilon$ can change:
* $a$ can cause heat, heat causes ice to melt, and melting ice in turn can cause a to change
* $\epsilon$ is related to the greenhouse effect

## Albedo
Albedo is the measure of diffuse reflection of solar radiation out of total solar radiation.

$$ a = \frac{\text{diffuse reflection}}{\text{total solar radiation}} $$

The Earth's average albedo is around 0.3-0.35 but varies significantly depending on location.

## Emissivity
Emissivity of a surface is the effectiveness in emitting energy as thermal radiation.

$$ \epsilon = \frac{\text{thermal radiation from a surface}}{\text{thermal radiation of a perfect black body}} $$

Emissivity of Earth is related to greenhouse gas. See more:
* https://sites.stat.washington.edu/peter/Emissivity.html

## Changes in temperature
$$ \delta heat = I - O + \tau $$

$$ I = (1 - a)S \pi r^2 $$

$$ \frac{dT}{dt} = \delta\text{heat content} / C $$

$$ \frac{dT}{dt} = B(T_0 - T_t) $$

$$ \tau(t) = \text{forcing coefficient} \ln{c_{\text{CO2}(t)} / C02 preindustrial} $$

$$ CO2(t) = 1 + (t - 1850)^3 / 220 $$
