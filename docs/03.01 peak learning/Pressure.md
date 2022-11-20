date: 08.14.2022
tags: #physics/fluidmechanics #chemistry/gases
# Pressure
The pressure **in a fluid** is the normal force per unit area:
$$p = \frac{dF_\perp}{dA}$$
- $F_\perp$ is the force **normal** to the fluid

**S.I. Unit**: $N/m^2 = Pa$ aka *Pascal*

**Common Unit**: $1.01 \times 10^5 Pa = 1\ atm$ aka *atmosphere*
- Average atmospheric pressure at **sea level**

Pressure at a given depth $h$ in a fluid of *uniform density*:
$$p = p_0 + \rho gh$$
- $\rho$ is the density of the fluid
```ad-danger
Don't forget the $p_0$, especially if it's an open container!!
```

Measuring *atmospheric* pressure is done with a [[barometer]] while measuring *system* pressure is done with a [[manometer]].

There are multiple *units* for pressure:
- The standard pressure is (unit) — 1 bar exactly, denoted $P$ #flashcard 
<!--SR:!2022-11-22,3,250-->
- 1 bar — $10^5$ atm #flashcard 
<!--SR:!2022-11-20,1,230-->
- 1 atm — $\ce{101 kPa = 1.01325 * 10^5 Pa}$ #flashcard
<!--SR:!2022-11-22,3,250-->
- 760 Torr — 1 atm #flashcard 
<!--SR:!2022-11-22,3,250-->
- There's also the $psi$ but don't worry about that (pounds per square inch)

Pressure can be calculated using the [[kinetic molecular theory]] — $$P=\frac{nMv_{rms}^{2}}{3V}$$ #flashcard 


```ad-note
title: derivation
collapse: open

1. $F=\frac{p}{\Delta t}$, so first calculate **mometum**
	1. Each particle has a momentum $mv_{x}$ before it hits the “wall” of a container, and hitting → change in direction. $mv_{x}-(-mv_{x})=2mv_{x}$
	2. Find number of particles that hit the “wall” in a time interval $\Delta t$
		1. Particles in the distance $v_x \Delta t$ → $Av_{x}\Delta t$ where $A$ is the surface area of the wall
		2. Gas particles are evenly spread throughout container → number of particles in that “section” can be found by multiplying ratio of volumes by the total number of particles: $\frac{Av_{x}\Delta t}{V} \times N$
		3. Half are moving towards $\frac{NAv_{x}\Delta t}{2V}$
	3. $p=2mv_x \times \frac{NAv_{x}\Delta t}{2V}$
2. $F = \frac{mNAv_{x}^{2} }{V}$
3. $P=\frac{F}{A} \implies P=\frac{mNv_{x}^{2} }{V}$
4. Account for not all molecules moving at the same speed
	1. Use average speed of all the molecules $\langle v_{x}^{2} \rangle$
	2. This is in all 3 directions so $\langle v^2 \rangle = v_{rms}=3\langle v_{x}^{2}\rangle$
	3. $P=\frac{mNv_{rms}^{2} }{3V}$
5. Substitute $nN_A = N$ and $mN_A = M$ → $P=\frac{nMv_{rms}^{2} }{3V}$
```
