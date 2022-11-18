date:: 2022-11-17
tags:: #chemistry/kevinstry 
priority:: 7
#  lecture 5: equilibrium
## Phyisical equilibria
This is concerned with phase changes.
- **Heat of fusion** is the transition between solid and liquid
- ![[Screenshot 2022-11-17 at 9.30.56 PM.png]]
- Supercooling: Liquid remains liquid below freezing point
	- NOT an equilibrium state!
- **Critical point**: liquids and gases are no longer different
	- Yields supercritical fluid that is in-between liquids and gases
- Heating profiles and cooling profiles
	- ![[Screenshot 2022-11-17 at 9.37.13 PM.png]]
		- Basically a temperature vs. heat supplied graph
			- At a phase change, the temperature doesn't change
- Transitions to and from *gases* are the most important
	- Vapor pressure: pressure exerted by vapor when it is in dynamic equilibrium with the liquid/condensed phase
		- Dynamic equilbrium is the transition at the interface between gas and liquid
	- More volatile gases = higher vapor pressure  and weaker IMF
- Clausius Clapeyron (formula)
	- Basically explains how vapor pressure and temperature are related
		- Enthalpy of vaporization
$$
	\ln \frac{P_{2}}{P_{1}}= \frac{\Delta H_{vap}}{R}\left( \frac{1}{T_{2}}-\frac{1}{T_{1}} \right)
$$

Solutions
- Molar solubility: molar concentration of a substance in a saturated solution
	- how much of a salt dissolved
- Miscible: two liquids forming a homogenous mixture when mixed together
- Usually solubility for solids increase with temperature
- Thermodynamics of formation
	- $\Delta H_{sol}$ components
		1. Break solute-solute interactions
		2. Break solvent-solvent interactions
		3. Form solute-solvent interactions
- Gaseous solubility changing with pressure and temp
	- Henry's law
		- $s=k_{h}P$
	- Gaseous solubility decreases with increasing temp

Volatile solute: a solute that contributes to the vapor pressure above the solution.

Colligative properties
- Relevant for non-volatile solutes
- These properties only depend on the number of particles (substance identity doesnt matter)
	- Decreasing vapor pressure (with added solute)
		- **Raoult's law**: $P_{solution} = \sum x_{substituent}P_{substituent}$ where $P_{substituent}$ is the vapor pressure of the pure volatile solute
	- Boiling point elevation
		- Solutions with non-volatile solutes 
		- i: [[Van't Hoff factor]]
		- $k_b$: ebullioscopic constant
		- b: molality
	- Freezing point depression
		- Same equation with boiling point elevation but with the cryoscopic constant instead
		- ![[Screenshot 2022-11-17 at 9.52.28 PM.png]]
	- Osmosis
		- Osmotic pressure $\Pi=iRTc_{solute}$ ($c$ is molarity)

Volatile solutions
- Binary mixtures: mixtures of two solvents
	- Vapor pressure follows Raoult's law
		- Plot pressure vs mole fraction
			- ![[Screenshot 2022-11-17 at 9.58.47 PM.png]]
			- Mole fractions of a vapor is just that pressure over sum of pressures
		- But Raoult's laws only apply for ideal solutions
			- Has $\Delta H_{sol} \approx 0$
			- Bond formation energy needed similar to bond breaking energy released
			- Judge ideal or not?
				- Like and like? = ideal! (benzene and toluene)
				- Strong IMF = likely not ideal
			- Deviations for non-ideal:
				- ![[Screenshot 2022-11-17 at 10.03.30 PM.png]]

Separation of mixtures
- [[Distillation]] (industrially)
	- Heat until pure fractions result
- **Azeotrope**: mixture's composition cannot be changed by simple distillation (just heat)
	- Vapor has same proportions as liquid
	- Water + ethanol
	- Separate using
		- Add sieves to suck out water/dessicant
		- Add another solvent that azeotropes with water (like a substitute)
## 
## Chemical equilibria
This is concerned with chemical changes.
- Molecules themselves are changing

**Chemical equilibrium**: a stage in a reaction when the composition of the reaction mixture will no longer change
- If reaction doesn't go to completion, call it reversible
- Concentrations of products and reactants remain constant
- Rate of forward reaction = rate of backwards reaction

Equilibrium constant $K$: ratio of products to reactants at equilibrium
- $K_c$: Take product concentration of products over product concentrations and raise each concentration to its coefficient
- $K_{p}$: pressures
- $K_p = K_{c}(RT)^{\Delta n}$

"Activity" ($\gamma$) = "effective concentration"
- Very complicated
- "Most effective way to gauge how active this sample is?"
- Same as concentration or pressure for gas/solutions

$K$ in the following formula:
$$
\Delta G_{r}\degree = -RT \ln K
$$
- Spontaneity depends on $K$

If the system is not at equilibrium, use $Q$ instead of $K$
- Same formula
$$
\Delta G_{r}=\Delta G_{r}\degree +RT\ln Q
$$
- Reaction quotient

Extent of reaction
- Reactions don't always go to completion, use $K$ and an ICE table
	- **I**nitial, **C**hange, **E**quilibrium

**Le Chatlier's Principle**: when stress is applied to a system in dynamic equilibrium, the equilibrium adjusts to minimize effect of stress
- Addition/removal of products/reactants
	- Think about how $Q$ will change with the stress
		- Which side of the ratio does the stress change? (products or reactants)
- Compression (gaseous)
	- Noncompressible container has constant volume, so there is no change
	- Compressible container
		- Pressure increase = volume decreases, shifts to side with less gas
		- Pressure decrease = volume increases, shifts to side with more gas
	- Volume is what matters
- Adding inert gas
	- Compressible container: Container expands
		- Volume increases, shifts to side with more gas
- Temperature change
	- Giving more heat, always want to consume heat
	- Decreasing heat, wants to produce heat