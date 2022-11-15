up:: [[Atoms]]
tags:: #chemistry/molecular 

# Atomic orbitals

These *are* the **wavefunctions** of the electrons in an atom!

The wavefunction is described by [[Spherical polar coordinates]] in the following equation:

$$
\psi(r,\theta,\phi) = R(r) \times Y(\theta,\phi)
$$
Notice two parts of the equation that influence the wavefunction:
- $R(r)$ is the **radial wavefunction**
	- How the wavefunction varies as distance from the nucleus increases 
- $Y(\theta, \phi)$ is the **angular wavefunction**
	- How the wavefunction varies as angles change

Solving the Schrodinger equation for this wavefunction at the **ground state** of a hydrogen atom (properties carry over to [[s-orbital]]):
$$
\psi(r,\theta,\phi) = Ne^{-r/a_0}, N=(\frac{1}{\pi a_0^3})^{1/2}
$$
- $a_0$ is the **Bohr radius** and has the value 52.9 pm
	- Tells the rate that the wavefunction decreases with distance away from the nucleus
- $N$ makes it clear that given the radius, the wavefunction is *spherically symmetric* -- the same in all directions (only for ground state though)

The **square** of the wavefunction is the probability density of an electron **at a point** in the 1[[s-orbital]]:
$$
\psi^2(r) = N^2e^{-2r/a_0}
$$
- To find the **total** probability density of finding an electron independent of direction, use [[Radial distribution function]]

As the [[Principal quantum number]] increase, the number of **nodes** in the graph of the wavefunction increases too.
- Each orbital has $n-1$ total nodes
	- $n-l-1$ radial nodes
	- $l$ angular nodes