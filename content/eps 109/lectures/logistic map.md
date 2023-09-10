fig tree plot: how the logistic map 
line that splits, splits again, then becomes more and more chaotic

logistic map: f(x) = rx(1-x)
map input x to output
more pet owners than vegetarians

x = number of foxes
r = number of rabbits
mapping tells you how many foxes there will be next year given the amount this year

heat bath = constant supply of something
compare the amount of foxes to a heat bath of rabbits (thats why our r is allowed to be constant regardless of the values for foxes)

what is the fixed point for the map? aka when you get the same value for what you put in. 

 f(x) = rx(1-x)
 rx(1-x) = x
**rx^2 -rx + x = 0**
when x = 0 and x = 1 - (1/r)
how many pet rabbits do i have, how many pet rabbits do i have next year. 

graphical solution: draw a line representing y = x. where this intersects is where rx(1-x) = x

stability of a fixed point: 
not on the fixed point, but a little off. does epsilon get bigger or smaller? 

**A fixed point is said to be stable if a small perturbation of the solution from the fixed point decays in time**; it is said to be unstable if a small perturbation grows in time. We can determine stability by a linear analysis

taylor series expansion: [infinite sum](https://en.wikipedia.org/wiki/Series_(mathematics) "Series (mathematics)") of terms that are expressed in terms of the function's [derivatives](https://en.wikipedia.org/wiki/Derivative "Derivative") at a single point.

function, we know we are here at some value x. what is the function value at x + delta (x). slope of the function is rise/run 
delta(y) / delta(x). 

if the derivative is less than 1, its unstable. if its greater than one its stable

for the 2 fixed points, are they stable or unstable. ![[Screenshot 2023-09-09 at 4.47.46 PM.png]]

x = 0
x = 1-(1/r)

f'(x) = r(1-x) + -rx = r(1-2x)
x = 0, r. stable for 0 to 1 (need f' to be less than 1)
x = 1 - (1/r), -r - r - 1 = 2-r, stable for anything bigger than 1
no stble fixed point for r > 3
f'(x) = r, f''(x) = 2-r
if r < 1, all foxes die. 
if r > 1, fox population increases. 
if r > 3, 

![[Screenshot 2023-09-09 at 4.53.35 PM.png]]period doubling event - **a slight change in a system's parameters causes a new periodic trajectory to emerge from an existing periodic trajectory**—the new one having double the period of the original
it takes twice as long to get to the same place. 

dynamical system: where future state is dependent on current state
![[Screenshot 2023-09-09 at 5.01.24 PM.png]]
function g tells us what happens in exactly x amount of time. it doesnt care about the future time point. 
function g has at least two stable fixed points (where it intersects with y = x). if its not a stable fixed point, its an unstable fixed point. slope of the new function is greater than 1 (unstable.)

a sequence of period doubling events leads to chaos? ? !??!?!