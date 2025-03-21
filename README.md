# Harmonic Oscillation Simulations  

This repository contains Python scripts for simulating and visualizing different types of harmonic oscillations using `numpy` and `matplotlib`.  

## Overview  

The code implements three different cases of oscillatory motion:  

1. **Damped Harmonic Oscillator**  
2. **Phase Space Representation of the Damped Oscillator**  
3. **Forced Damped Oscillation**  

Each section computes and visualizes the oscillatory motion with different damping and external force conditions.  

---

## 1. Damped Harmonic Oscillator  

This simulation models a **damped harmonic oscillator**, where the system gradually loses energy due to damping.  

### **Equation of Motion:**  

\[
x(t) = A e^{-\beta t} \sin(w_1 t - \alpha)
\]

where:  
- \( A \) = Initial amplitude  
- \( \beta \) = Damping coefficient  
- \( \alpha \) = Phase shift  
- \( w_0 \) = Natural frequency  
- \( w_1 = \sqrt{w_0^2 - \beta^2} \) = Damped frequency  

### **Implementation:**  
- Defines parameters for damping and frequency.  
- Computes \( x(t) \) iteratively for a given time range.  
- Plots the displacement vs. time graph, showing **damped oscillations**.  

---

## 2. Phase Space Representation of the Damped Oscillator  

This section plots **velocity (\(\dot{x}\)) vs. displacement (\(x\))** to show the phase space trajectory of the damped oscillator.  

### **Velocity Equation:**  

\[
\dot{x} = -\beta A e^{-\beta t} \sin(w_1 t - \alpha) + A w_1 e^{-\beta t} \cos(w_1 t - \alpha)
\]

### **Implementation:**  
- Computes both displacement \( x(t) \) and velocity \( \dot{x}(t) \).  
- Plots **phase space** trajectory, showing an inward spiral due to damping.  

---

## 3. Forced Damped Oscillation  

This section models an oscillator subjected to an external **periodic driving force**.  

### **Equation of Motion:**  

The total displacement consists of:  

1. **Natural Response (Complementary Solution):**  
   \[
   x_c = A e^{-\beta t} \cos(w_1 t - \alpha)
   \]
2. **Steady-State Response (Particular Solution):**  
   \[
   x_p = \frac{F_0 \cos(w t)}{\sqrt{(w_0^2 - w^2)^2 + (4 \beta^2 w^2)}}
   \]

### **Implementation:**  
- Defines the parameters for the driving force.  
- Computes the **total displacement** by summing the natural and particular solutions.  
- Plots:
  - **Total motion** (solid line)  
  - **Steady-state response** (dashed line)  

This demonstrates how transient oscillations decay over time, leaving only the steady-state oscillation.  

---

## **Requirements**  

Ensure you have the following Python libraries installed before running the scripts:  

```bash
pip install numpy matplotlib
