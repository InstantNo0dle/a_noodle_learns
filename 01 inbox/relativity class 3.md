date:: 2022-11-19
tags:: #physics/relativity #columbiashp 
priority:: 4
# relativity class 3
## velocity addition
- 3 observers (reference frames) $O_1, O_2, O_3$ in **relative motion** with respect to each other
	- All inertial frames
	- $O_1$ has velocity $v_{12}$ with respect to $O_2$ and same for the rest
	- Clocks are synchronized
		- But [[time dilation]] and [[length contraction]] make it so that there are differences
	- Unprimed coordinates to $O_1$, primed to $O_2$ and double primed to $O_3$
- Problem: Given *two* **relative velocities**, what is the third ($v_{13}$)?
	- Conceptual: Observer on the ground, there's a river and a swimmer
		- River has velocity towards some direction
			- Swimmer is moving with respect to the water, with a velocity that is also with respect to the **water**
			- To the observer on the ground, the swimmer is moving "faster"
				- Add velocities
			- This is velocity addition in gallilean relativity (derived from [[gallilean boosts]])
	- Goal is to find formula for velocity addition in [[postulates of special relativity|special relativity]]
		- Use same conceptual thought simulation and [[lorentz boosts#^d2bf67|lorentz boosts]] instead of gallilean boosts
			- Two events that both label the swimmer (all equations address the **swimmer** because they are demonstrating velocity addition)
				- A: swimmer exists at some time $t_A$
				- B: swimmer exists at some time $t_A>t_B$ 
			- Can apply same formulas to go from primed to nonprimed (inverse of lorentz boosts) by making velocities negative (do the same to go from double primed to nonprimed)
			- ![[Screenshot 2022-11-19 at 10.26.46 AM.png|400]]
			- Velocity is $\frac{\Delta x}{\Delta t}$, so use the equations to solve
				- The swimmer isn't moving with respect to themself, so $\Delta x'' = 0$
			- Equation is:
				- $$\frac{\Delta x}{\Delta t}=\frac{v_{1,2}+v_{2,3}}{1+\frac{v_{1,2}v_{2,3}}{c^2}}=v_{1,3}$$
				- $\frac{v_{1,2}v_{2,3}}{c^2}$ is very small in everyday situations (because velocities are much smaller than $c$ usually), so we actually see gallilean velocity addition!
					- Maxima is $c$ when equation is graphed → nothing can travel faster than the speed of light
				- Can confirm that speed of light is constant in all reference frames by letting $v_{1,3} = c$. It will be found that $v_{1,2}=v_{2,3}=c$
## spacetime diagrams
- Focus on 1+1 dimensions (space and time)
	- To make dimensions consistent, multiply time by $c$ → $ct$
- Event is a point in the diagram
- **Wordline**: *curve* in spacetime
	- Parameterized set of events
	- Describes an object’s motion in spacetime
	- Light rays always have a worldline with a slope of 1
		- $$