date: 08.24.2022
tags:  #physics/mechanics/motion 
# Angular Momentum
The angular momentum of a particle of mass $m$ with linear momentum $\vec p$ is:
$$
\vec l = \vec r \ \times \vec p = m(\vec r \ \times\ \vec v)
$$
- The particle itself doesn't have to rotate around the point it's relative to

Its *direction* is always **perpendicular** to the plane formed by the position and linear momentum vectors (found using the right hand rule).
![[Screen Shot 2022-08-24 at 9.36.30 PM.png]]

>[!note] Important
>**Angular momentum** only has meaning *with respect to* the specified origin.

For a rigid body rotating about a fixed axis:
- The angular momentum can be found by **summing** the $z$ components of all the angular momenta of each "point" in the body.
- You can substitute the [[Linear Velocity#^ddc2d5|linear velocity of a rotating body]] equation
- Also substitute [[Moment of Inertia]] about a fixed axis equation
$$ \begin{align}
l_i = (r_i)(p_i)(sin\ 90\degree)=(r_i)(\Delta m_iv_i)\\
l_{iz} = l_isin\ \theta=(r_i sin\ \theta)(\Delta m_iv_i)=r_{\perp i}\Delta m_iv_i\\
L_z = \sum^n_{i=1}l_{iz} = \sum^n_{i=1} \Delta m_iv_ir_{\perp i} = \sum^n_{i=1}\Delta m_i(\omega r_{\perp i})r_{\perp i} \\
=\omega(\sum^n_{i=1}\Delta m_ir_{\perp i}^2)\\
\therefore L=I\omega
\end{align}
$$
![[Screen Shot 2022-08-24 at 9.59.10 PM.png]] ^2eeca9