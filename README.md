# Computational Methods Final Project
## Orbital Motion and Voyager 1 Trajectory
Meghan Cilento and Mairead Heiger


### Project Outline
The main goal of this project is to animate the trajectory of Voyager 1 as it
uses gravitational assists to travel out of our solar system. The following steps
outline the intermediate stages to getting to that final animation:

1. Calculate and animate different types of Keplerian orbits
2. Explore how different initial conditions affect slingshot trajectory
3. Calculate the trajectory of Voyager 1
4. Animate the trajectory of Voyager 1


#### **Stage 1**
In order to generate the trajectory of Voyager 1, we knew that we needed to first 
animate the orbits of Earth, Jupiter and Saturn, as well as produce a hyperbolic, or 
slingshot, orbit. We therefore began this project by plotting and animating 
different possible Keplerian orbits to explore the initial conditions which produce 
such trajectories. 

The equations of motion for a planetary orbit are given by second order 
differential equations which can be derived from the force of gravitational
attraction between two celestial bodies:

![ODEs](ODE.png)

The two second order ODEs outlined in red were solved using the 4th order Runga 
Kutta Method. This method was chosen over others because there is a minimal loss 
of energy during the timescale of Voyager 1's trajectory. It was also easy to code, 
and it is not an implicit method, so it was less computationally demanding. 

Using the solutions to these equations, we were able to set initial conditions
for position and velocity. Knowing that the tangential velocity of one object 
with respect to another determines whether the object collides, orbits, or flies 
off into space allowed us to generate the five different possible Keplerian orbits 
by adjusting the initial velocity condition. Our main focus of this project is 
on the hyperbolic orbit, which produces gravitational assists.

The python notebook, `Final Project Code.ipynb`, generates the plots and
animations for the five different orbit types:

1. Collision Orbit
2. Circular Orbit
3. Large Elliptical Orbit
4. Parabolic Orbit
5. Hyperbolic Orbit

In this notebook, we used Jupiter as an example planet. The equations for tangential
velocity condition extend to any two interacting objects, but in this case, we 
set Jupiter at its perihelion location (x0 = 7.4052e11) and gave it different initial 
tangential velocities to demonstrate how initial velocity affects final trajectory. 
As you can see in the animations (all of which are saved in `Orbit Animations`), 
changing the initial velocity drastically changes which path Jupiter takes as it 
orbits the sun.

The following equations provide the initial velocity constraints which determine
the final path an object will take when it starts moving tangentially to another
object.

![Velocity Conditions](Velocity_conditions.png)

The following known values were used in our calculations:  
**M** (sun) = 1.989e30 kg  
**m** (jupiter) = 1.898e27 kg      
**G** (constant) = 6.67408e-11 m^3 kg^-1 s^-2  
**r** (semi-major axis) = 7.4052e11 m


#### **Stage 2**
#### **Stage 3**
#### **Stage 4**