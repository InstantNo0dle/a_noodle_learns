date: 2022-11-12
tags: #physics/relativity 
# lorentz boosts

These are *replacements* for [[gallilean boosts]] in special relativity, which do not match up/work with special relativity because they don't consider the speed of light to be constant.

Set up $\Delta x'$ and $\Delta t'$ as functions of $\Delta x$ and $\Delta t$ with a standard form similar to [[gallilean boosts#^ff127d|gallilean boosts]]:
$$\begin{align}
\Delta x' = A\Delta x + B \Delta t \\
\Delta t' = C\Delta x + D\Delta t
\end{align}
$$
- Linear because when you deal with very *small*, infinitessimal values, you can always linearize

Constraint the equations with the [[effects of special relativity]] and definitions:

| effect/def                  | constraint     | equation                               |
| --------------------------- | -------------- | -------------------------------------- |
| [[rear-clock-ahead effect]] | $\Delta t = 0$ | $\Delta t' = -\frac{\Delta x' v}{c^2}$ |
| [[length contraction]]      | $\Delta t = 0$ | $\Delta x = \frac{\Delta x'}{\gamma}$  |
| [[time dilation]]           | $\Delta x = 0$              |  $\Delta t = \gamma \Delta t'$ and $\Delta x = v\Delta t$                                      |
|  definition of velocity  | $\Delta x' = 0$               |   $\Delta x' = -v \Delta t'$    |


Use these constraints and equations to solve for A, B, C, and D
- Take two equations at a time and solve

In the end, you get:
$$
\begin{align}
\Delta t' = \gamma [\Delta t - \frac{v}{c^2}\Delta x] \\
\Delta x' = \gamma [\Delta x - v\Delta t] \\
\end{align}
$$

^d2bf67

- These are pretty intuitive:
	- $\Delta x'$ has $\gamma$ to compensate for [[length contraction]]
	- $\Delta t'$ : "Simultaneity of events from a distance in space"

Boosts can be thought of as rotations in time.