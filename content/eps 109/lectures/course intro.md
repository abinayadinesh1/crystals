
learn data processing and learn to code
ppl who went to antarctica, got the oldest ice possible and generated a record of how much CO2 was dissolved (amt in rock correlates to amt in atmosphere)

	what is the exact measurement between amount of co2 in rock vs amt in the atmosphere?

snow falls, gets compacted, turns into ice, lot more layers build on top to preserve CO2 signature.

temperature is also preserved in ice. as the snow falls, it traps isotopes of hydrogen. depending on how many deuterium, can back track how old it was.

whenever CO2 went up, temperature goes up. 

correlation does not imply causality, but we have an explanation. if theres no explanation, good chance its a coincidence.

good to challenge things, dont accept data thats given to you blindly. good to accept things many people have proven before you. 
![[Screenshot 2023-09-07 at 10.57.26 AM.png]]
2 tidal bridges - moon and sun and wall that sloshes back and forth and does that 2x a day. tidal record was measured in two different locations. noise is not an accident, can do a fourier transfer to filter it out. 


2 tidal records. ask what frequencies are in the signal: daily periodic variation. if u plot the period and you get a big peak at 12 hours, it has something to do with the sun or the earth's rotation. another peak at 26 hours. moon does not have a periodicity of 24 hours, it has it of 26 hours. because it is orbiting the earth, its at a different place every time. 

write code and SIMULATE things on your laptop. 

**fractals in nature made by diffusion limited aggregation**
whenever you have a random process, you are allowed to call it monte carlo. 
how we made this simulation is to randomly pick out of 4 directions which step to take. if you hit something, it breaks. ![[Screenshot 2023-09-07 at 11.01.48 AM.png]]
monte carlo is a casino? use random numbers to generate something useful. if u apply the right kinds of rules, you get patterns emerging. if everything is deterministic, why are random numbers so useful?

fractal - self regulating and because it is so regular. has a fractional dimension (1.71)
familiar with 1, 2, 3 dimensions. 
lung and brain have to have a huge surface area squeezed into small volume. the fractal dimension of our lungs is 2.91. super close to 3, but cant be 3 or else we cant breathe. 


fractal dimension is actually just a measurement of complexity. how fast does it change over a finite area. _fractal dimension_ coined by mandelbrot who made mandelbrot set. 

one computer lab with the famous mandelbrot set to make a fraction. 
zn+1 = zn^2 + c
we just need to find a solution to this. 

mandelbrot couldnt find a analytic solution to this, so he through it at a computer. 
whole class of problems that fall under fractals you generate with a computer. 

## heat
later, we explain the temperature distribution of a wall. at a specific position at a specific time, what is the temperature? how does this change over time? good for answering a question like: if i start heating up a cabin, how long will it take to get a even distribution of heat? 

partial differential equations!!!!
very hard to solve them in math bc theyll go to diff functions. on a computer, 
1. divide your domain into different partials and solve for each. 
computer solution is not exact, but an extremeley close approximation. ![[Screenshot 2023-09-07 at 11.14.29 AM.png]]

the heat equation and diffusion equations are the same: except in one, heat is diffusing and in the other, particles are diffusing. 
![[Screenshot 2023-09-07 at 11.15.26 AM.png]]

landscape evolution models. landscapes evolve over time. take the data and write equation that change landscapes for millions of years. water erodes a bit different because it tends to form channels. heat spreads differently because it diffuses across a gradient. 



someone wrote a python interface where my laptop can connect to a server w all the known earthquakes for 50 years. 



### partial differential equations
fracking regulated to prevent earthquakes. earth 

### solar system dynamics
solve newton's equation: F = ma
no propulsion, keplers laws will tell you how long it takes to complete one orbit
P^2 proportional to radius of the orbit cubed. 

can study dynamical systems: if you perturb initial condition and wait 1000 durations, the trajectory will be completely different. chaotic. 


towards the end of the course, cherry picking interesting topics!
image processing - 

### molecular dynamics
generate a crystal and then rip it apart, lots of defects were generated



replicating/understanding what the gods of python have done for us before






labs: just try your best
homework: must finish
some people go to agu![[Screenshot 2023-09-07 at 12.01.45 PM.png]]