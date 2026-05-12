# Turbulent Pipe Flow

A verification study of incompressible, fully developed turbulent flow in a circular pipe.  

The simulation performed in __Ansys Fluent__ is compared to the analytical Hagen–Poiseuille solution for velocity profile and pressure drop.

## 1. Problem Definition

<img width="1189" height="539" alt="Pasted image 20260507111542" src="https://github.com/user-attachments/assets/60136a45-0bf9-4677-bc17-b2c538a09ea8" />


The length of the pipe, $L$, is chosen such as to ensure fully developed flow at the outlet. 

$$L=1\; m$$
$$R=0.05\;m$$

**Flow Regime**  
The Reynolds number is defined as:

$$Re = \frac{\rho U D}{\mu}$$

, where 
- $D$ is the diameter of the pipe, 
- $\rho$ it the fluid density,
- $U$ is the __mean flow velocity__,
- $\mu$ is the __dynamic viscosity__.

The inlet velocity and fluid properties are chosen such that the Reynolds number is $Re\approx 10^5$. 

Therefore, the flow is __turbulent__.
## RANS model

We will use a Reynolds-averaged Navier-Stokes equation, aka __RANS__ model to describe the fluid flow. The principle in this model is to decompose an instantaneous quantity into its time-averaged and fluctuating component.

The equations describing the time-averaged solutions of the __Navier-Stokes equation__ for an incompressible fluid undergoing stationary flow are:

$$
\rho \bar{u}_j \frac{\partial \bar{u}_i}{\partial x_j}
=
\rho \bar{f}_i
+
\frac{\partial}{\partial x_j}
\left[
    -\bar{p}\,\delta_{ij}
    + \mu \left(
        \frac{\partial \bar{u}_i}{\partial x_j}
        + \frac{\partial \bar{u}_j}{\partial x_i}
      \right)
    - \rho\,\overline{u_i' u_j'}
\right]
$$
We will employ two RANS models namely __k-e__ and **k-w**.
### $k-\epsilon$ model

A two equation RANS turbulence model that predicts turbulent viscosity using transport equations for kinetic energy and dissipation. This model is applied inside the pipe.

### k–ω SST model 

Blends the near‑wall accuracy of k–ω with the free‑stream stability of k–ε and adds a shear‑stress limiter, giving highly reliable predictions for separation, adverse pressure gradients, and general‑purpose engineering flows.


