# 📊 Visualizing Various Problems in Nonlinear Dynamics

Author: Deepali Pandey  
Date: November 2025  

This repository contains numerical simulations and visualizations of classical nonlinear dynamical systems including bifurcations, chaos, limit cycles, strange attractors, and discrete maps.

---

# 🔹 SET I – Continuous Dynamical Systems

---

## 1️⃣ Homoclinic Bifurcation System

System of equations:

x_dot = y  
y_dot = -μ - x + x² - x y  

Fixed points obtained from:

y = 0  
x² - x - μ = 0  

Jacobian matrix:

| 0        1        |  
| -1 + 2x - y   -x  |

Stability depends on:
- Trace τ = -x
- Determinant Δ = 1 - 2x + y

Behavior with parameter μ:

- μ < 0 → No fixed points  
- μ = 0 → Center + Saddle  
- μ = 0.5 → Stable fixed point  
- μ = 1 → Unstable spiral + Saddle  

---

## 2️⃣ FitzHugh–Nagumo Type System

v_dot = v - (v³)/3 - w + R I_ext  
τ w_dot = v + a - b w  

Parameters:
a = 0.7  
b = 0.8  
τ = 12.5  
R = 0.1  
I_ext ∈ [-30, 30]

Limit cycles observed approximately in:

-6 < I_ext < 15

Time period T computed using peak detection.

---

## 3️⃣ Lorenz System

x_dot = σ (y - x)  
y_dot = r x - y - x z  
z_dot = x y - b z  

Parameters:
σ = 10  
r = 28  
b = 8/3  

Simulations include:
- 3D strange attractor
- Sensitive dependence on initial conditions
- Log-scale divergence plot
- First return map

---

# 🔹 SET II – Discrete Maps & Chaos

---

## 1️⃣ Logistic Map

x_(n+1) = r x_n (1 - x_n)

Implemented:

- Cobweb diagram (r = 3.8)
- Bifurcation diagram (r ∈ [3,4])
- Period-3 window at r ≈ 3.82891
- Lyapunov exponent:

λ(r) = lim (1/n) Σ log |f'(x_i)|

- Invariant density at r = 4:

P(x) = 1 / sqrt(x(1 - x))

---

## 2️⃣ Sine Circle Map

θ_(n+1) = θ_n + Ω - (K / 2π) sin(2π θ_n)

Implemented:
- Winding number vs Ω (Devil’s staircase)
- Arnold tongue heatmap in (K, Ω) plane

---

## 3️⃣ Chaotic Image Map

(x_(n+1), y_(n+1)) = (2x_n + y_n, x_n + y_n) mod 1

Simulates chaotic evolution of a 2D pixel grid and studies recurrence.

---

# 📈 Concepts Covered

- Phase portraits  
- Limit cycles  
- Bifurcation theory  
- Lyapunov exponents  
- Strange attractors  
- Period-doubling route to chaos  
- Arnold tongues  
- Sensitive dependence  

---

# 🛠 Installation

```bash
git clone https://github.com/freakingdark/Visualizing_varoius_problems_in_Non_Linear_dynamics.git
cd Visualizing_varoius_problems_in_Non_Linear_dynamics
pip install numpy matplotlib scipy
