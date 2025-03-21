This script analyzes three different cases of harmonic oscillation:

Damped Harmonic Oscillator
Phase Space Representation of the Damped Oscillator
Forced Damped Oscillation
Each section uses Python’s numpy and matplotlib libraries to compute and visualize the oscillations.

1. Damped Harmonic Oscillator
This section simulates the motion of a damped harmonic oscillator, where the system loses energy over time due to damping.

Mathematical Model:

The equation governing the motion is:

x
(
t
)
=
A
e
−
β
t
sin
⁡
(
w
1
t
−
α
)
x(t)=Ae 
−βt
 sin(w 
1
​	
 t−α)
where:

A
A is the initial amplitude
β
β is the damping coefficient
α
α is the phase shift
w
0
w 
0
​	
  is the natural frequency
w
1
=
w
0
2
−
β
2
w 
1
​	
 = 
w 
0
2
​	
 −β 
2
 
​	
  is the damped frequency
The script:

Defines the parameters for damping and frequency.
Iterates over time values, computing the displacement 
x
(
t
)
x(t) at each step.
Stores the values in arrays for plotting.
The trajectory is plotted, showing an oscillation that decays exponentially over time.
2. Phase Space Representation of the Damped Oscillator
This section plots the phase space of the damped oscillator, representing velocity (
x
˙
x
˙
 ) versus displacement (
x
x).

Mathematical Model:

Velocity is computed as:

x
˙
=
−
β
A
e
−
β
t
sin
⁡
(
w
1
t
−
α
)
+
A
w
1
e
−
β
t
cos
⁡
(
w
1
t
−
α
)
x
˙
 =−βAe 
−βt
 sin(w 
1
​	
 t−α)+Aw 
1
​	
 e 
−βt
 cos(w 
1
​	
 t−α)
The script:

Computes both 
x
(
t
)
x(t) and its derivative 
x
˙
(
t
)
x
˙
 (t).
Plots the phase space trajectory, which spirals inward, indicating energy dissipation due to damping.
3. Forced Damped Oscillation
This section simulates a damped oscillator subjected to an external periodic driving force.

Mathematical Model:

The total displacement consists of:

Complementary Solution (natural response):
x
c
=
A
e
−
β
t
cos
⁡
(
w
1
t
−
α
)
x 
c
​	
 =Ae 
−βt
 cos(w 
1
​	
 t−α)
Particular Solution (steady-state response):
x
p
=
F
0
cos
⁡
(
w
t
)
(
w
0
2
−
w
2
)
2
+
(
4
β
2
w
2
)
x 
p
​	
 = 
(w 
0
2
​	
 −w 
2
 ) 
2
 +(4β 
2
 w 
2
 )
​	
 
F 
0
​	
 cos(wt)
​	
 
The script:

Defines the parameters for the driving force.
Computes the general and particular solutions for 
x
(
t
)
x(t).
Plots the total response (solid line) and the steady-state response (dashed line) over time.
The graph shows transient oscillations that decay due to damping, followed by a steady-state oscillation at the driving frequency.
