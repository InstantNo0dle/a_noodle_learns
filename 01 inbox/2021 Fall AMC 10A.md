date: 2022-11-04
tags: #math

# 2021 Fall AMC 10A
Original solutions: [Art of Problem Solving](https://artofproblemsolving.com/wiki/index.php/2021_Fall_AMC_10A)

###### **Problem 15**: Isosceles triangle $ABC$ has $AB=AC=3\sqrt6$ and a circle with radius $5\sqrt2$ is tangent to line $AB$ at $B$ and to line $AC$ at $C$. What is the area of the circle that passes through vertices $A$, $B$, and $C$?
The key is drawing the diagram correctly; it’s almost impossible to solve without drawing — ALWAYS draw in geometry problems (and make the diagram large)!
1.  Draw an accurate diagram with triangle $ABC$ and another triangle on top with two sides as the radii of the tangent circle.
2. Notice that the circle that passes through vertices $A,B,C$ is the circumcircle and when connecting the circumcenter to the sides, form perpendicular bisectors.
3. Notice similar triangles and solve for the radius, the rest is trivial.

###### **Problem 16**: The graph of $f(x)=|\lfloor x\rfloor| - |\lfloor 1-x \rfloor|$ is symmetric about which of the following? (Here is the greatest integer not exceeding $x$.)
When given a function, ALWAYS try to graph it. If you’re unsure of what the graph looks like, break it down into parts that you do know how to graph. Then, piece it back together and use that to figure out how to do the rest of the problem.
1.  Graph $y_1 = |\lfloor x \rfloor|$ and $y_2=|\lfloor 1-x \rfloor|$ separately
2.  Subtract values of $y_1$ from $y_2$ (graphically) and you have your answer

###### **Problem 17**:An architect is building a structure that will place vertical pillars at the vertices of regular hexagon $ABCDEF$, which is lying horizontally on the ground. The six pillars will hold up a flat solar panel that will not be parallel to the ground. The heights of pillars at $A$, $B$, and $C$ are $12$, $9$, and $10$ meters, respectively. What is the height, in meters, of the pillar at $E$?
Once again, make a fairly accurate (at least make it *look* right) drawing of the 3D shape and keep in mind the constraints of the problem.
1.  Draw the hexagonal pillar and make the legs look proportional to their actual lengths
2.  Take into consideration the fact that the panel is flat (all points coplanar) so the height difference between points on parallel lines is the same
3. By the same logic, the difference between a vertex and the center should be the same for *diagonally opposite* verticies (that are collinear)