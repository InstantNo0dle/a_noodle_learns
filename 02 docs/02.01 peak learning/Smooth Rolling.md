date: 08.23.2022
tags:  #physics/mechanics/motion
# Smooth Rolling
Rolling motion can be studied as the **combination** of translation of the center of mass and the rotation of the object around that center.

During a time interval, a point on the rolling body travels the **distance** of an arc length:
$$
s = \theta R
$$
![[Screen Shot 2022-08-23 at 4.38.25 PM.png]]

The velocity of the **center of mass** can be found using the [[Linear Velocity]] (rotational) equation
- Essentially differentiating the distance equation from above:
	- This is because points on the outer edge of a rotating body move with the same linear speed ($v_{com}$)
$$
v_{com} = \omega R
$$
^7fddfe

Combining *translational* and *rotational* motion:
- **Rotational**: Every point on the edge of the rolling body has speed $v_{com}$ 
	- A point at the top of the rolling body has *positive* velocity==, and the opposite is true for a point at the bottom.
- **Translational**: Every point on the rolling body moves in the positive direction with the same speed $v_{com}$
- So, a point at the top of the wheel will have **twice** the speed than any other point. The point at the bottom of the wheel will be **stationary**.

![[Screen Shot 2022-08-23 at 4.47.22 PM.png]]

## Down a Ramp
Smooth rolling down a ramp involves the following **forces**:
1. **Gravitational force** pointing downwards, with $F_g sin\ \theta$ parallel to the ramp and equal to $mg\ sin\ \theta$
2. **Normal force** pointing upwards, opposing $F_g\ cos\ \theta$
3. **Static frictional force** $\vec f_s$ directed up the incline of the ramp, opposing the potential sliding downwards

**Newton's second law** can be applied twice (linear and angular):
$$
\begin{align}
F_{net,x} = f_s - Mg\ sin\ \theta = Ma_{com,x}\\
\tau_{net} = Rf_s = I_{com}\alpha
\end{align}
$$
Since it's smooth rolling, the equation for [[Friction#^dcf3b1|Acceleration of center of mass]] can be applied:
- $a_{com}$ is **negative** because the body is accelerating *down* the ramp
$$\begin{align}
f_s = -I_{com}\frac{a_{com,x}}{R^2} \\
a_{com,x} = - \frac{g\ sin\ \theta}{1+I_{com}/MR^2}
\end{align}
$$

The kinematics of a <mark style="background: #FFB8EBA6;">yo-yo</mark> can be treated the same as rolling down a ramp, except at a $90\degree$ angle and is slowed by *tension* from the string. 

>[!important]
>Although gravity causes the body to come down the ramp, it's the **frictional force** (or tensional) that causes it to rotate and roll.