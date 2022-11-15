date: 08.24.2022
tags:  #physics/mechanics/motion 
# Precession of a Gyroscope
A rapidly spinning gyroscope, instead of continually rotating downwards due to [[Torque]], insteads **rotates** *horizontally* around a vertical axis -- <mark style="background: #FFB8EBA6;">precession</mark> .
- For a rapidly spinning one, the magnitude of [[Angular Momentum]] is fixed, so torque can only change its **direction**
	- $$
	d\vec L = \vec\tau dt
	$$
		- Derived from [[Newton's Second Law#^8869df|Newton's second law in angular form]]
	- Since $d\vec L$ is in the same direction as $\vec \tau$, which is perpendicular to the angular mommentum, $\vec L$ must rotate around the $z$ axis and thus the **shaft** also rotates
- ![[Screen Shot 2022-08-24 at 10.15.05 PM.png]]

The <mark style="background: #D2B3FFA6;">precession rate</mark> can be calculated using the above equation and the magnitude of $\tau$:
- Also using using the [[Angular Momentum#^2eeca9|angular momentum of a rigid body rotating around a fixed axis]]
$$ \begin{align}
\tau = Mgr\ sin\ 90\degree=Mgr\\
dL = \tau dt = Mgr\ dt\\
d\phi = \frac{dL}{L} = \frac{Mgr\ dt}{I\omega} \\
\therefore \Omega = \frac{Mgr}{I\omega}
\end{align}
$$