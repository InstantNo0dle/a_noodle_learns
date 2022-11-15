date: 2022-11-08
tags: #compsci #math #toresearch 
# markov random field

This is an undirect graph:
- Each node = random variable
- Each edge = relationship between two nodes

The energy function is:
![[Screenshot 2022-11-08 at 9.38.21 PM.png]]
- $C_u$ = unary cost
	- Cost of assigning state $l_u$ to a node
	- $C_u(l_u) = -log P(l_u|u)$
- $S_{uv}$ = pairwise cost
	- Cost of assigning states $l_u$ and $l_v$ to neigboring nodes
- $N(u)$ = variables that are neighbors of $u$