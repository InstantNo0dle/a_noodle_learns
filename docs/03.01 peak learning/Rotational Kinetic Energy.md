date: 08.20.2022
tags: #physics/mechanics/motion #physics/mechanics/motion  
# Rotational Kinetic Energy
To get the [[Kinetic Energy]] of a rotating rigid body, add all the **individual** kinetic energies of the particles:
- Since $v_i$ isn't standardized for all particles, use a value that is (substitute [[Linear Velocity#^^ddc2d5]|linear velocity equation]])
- [[Moment of Inertia]] can be substituted inside the parentheses

$$ \begin{align}
K = \frac{1}{2}m_1v_1^2+\frac{1}{2}m_2v_2^2+\frac{1}{2}m_3v_3^2 + \cdot\cdot\cdot =\sum\frac{1}{2}m_iv_i^2 \\
=\sum\frac{1}{2}m_i(\omega r_i)^2=\frac{1}{2}(\sum m_ir_i^2)\omega^2\\
=\frac{1}{2}I\omega^2
\end{align}
$$
>[!important]
>Rotational kinetic energy depends not just on the mass of the body, but how it's **distributed** is important as well.

Kinetic energy can also be found for a [[Smooth Rolling]] rigid body, using the above equation:
- The equation can be used since rolling can be considered pure rotation about an axis through a point ($p$) on the outer edge
- [[Parallel Axis Theorem]] can be used to represent the moment of inertia in terms of **center of mass**
- [[Smooth Rolling#^7fddfe|Linear velocity for smooth rollling]] equation can be applied
$$
\begin{align}
K=\frac{1}{2}I_p\omega^2\\
=\frac{1}{2}I_{com}\omega^2 + \frac{1}{2}MR^2\omega^2 \\
=\frac{1}{2}I_{com}\omega^2 + \frac{1}{2}Mv_{com}^2
\end{align}
$$
- There are two parts to this equation; a rolling object has *two* types of kinetic energy
	1. **Rotational kinetic energy** from rotation about the object's center of mass
	2. **Translational kinetic energy** from translation of the center of mass