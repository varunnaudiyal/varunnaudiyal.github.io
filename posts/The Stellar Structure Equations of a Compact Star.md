
```table-of-contents
```

The equations for Hydrostatic Equilibrium in Newtonian gravity are very well known and a bit trivial to derive. However when we consider very compact stars like Neutron Stars (and perhaps even white-dwarfs), we move into the regime of Einstein's General Relativity.

Before we discuss the actually start the discussion of the Stellar Structure equations for such a compact star, we would want to get a quick overview of the "Structure of Spacetime" in the vicinity of (and within) such objects.

## The Spherically Symmetric Space-time :

In special relativity, we are very well aware of the "space-time" interval. It is the fundamental quantity which is invariant under lorentz transformations. However it hides something deeper about the structure of spacetime itself.

Though I will not get into the geometrical structures* (which come from Differential Geometry) which are used to describe a "**space**" (or space-time in our case), but the space-time interval is actually a manifestation of a quantity called the "**metric**", which defines how "**lengths**" are measured in a "**space**" (space-time). It can also be shown that the notions of "**shape**" or "**curvature**" can also be derived from a metric.

For special relativity, we have : $$ds^2 = -dt^2 + dx^2 + dy^2 + dz^2$$
Notice that seems very similar to the notion of an infinitesimal step in a 4D euclidean space, except the "$dt$" component has a negative sign. In our standard euclidean space, the magnitude of some infinitesimal step $d\vec{r}$, would be given as :
$$
d\vec{r} \cdot d \vec{r} = dt^2 + dx^2 + dy^2 + dz^2
$$
Alternatively you can also write this as,
$$
d \vec{r} \cdot d \vec{r} = \left(\begin{matrix}
dt ~ dx ~ dy ~ dz 
\end{matrix}\right) \left(\begin{matrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 
\end{matrix}\right) 
\left(
\begin{matrix}
dt \\
dx \\
dy \\
dz
\end{matrix}
\right)
$$
The **matrix** in the middle is what is known as the **metric** for flat euclidean space-time. In special relativity we have a lorentzian space-time thus our flat metric looks like, 
$$
\begin{bmatrix}
- 1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 
\end{bmatrix}
$$
However, special relativity is a theory without "gravity". Gravity falls under the purview of General Relativity where the structure of the space-time is coupled to mass-energy present in the region as follows :
$$
R_{\mu \nu} - \frac{1}{2}R g_{\mu \nu} = 8 \pi T_{\mu \nu} 
$$
Here, the quantities on the **LHS** are "**tensors**" constructed from the metric which encode information about the structure of space-time (we actually call the entire LHS the **Einstein Tensor**, $G_{\mu \nu}$). On the **RHS** we have the **Energy-momentum** / **Stress-Energy** Tensor, which encodes the information about the mass-energy content of the space-time.

If we want to talk about the stellar-structure equations of compact stars, then these are the equations that we have to solve. However, before we begin, we need to know what the "metric" will be. The most commonly used ansatz for a spherically-symmetric space time is,
$$
g_{\mu \nu} = \begin{bmatrix}
- e^{\nu(r)} & 0 & 0 & 0  \\
0 & e^{\lambda(r)} & 0 & 0  \\
0 & 0 & r^2 & 0 \\
0 & 0 & 0 & r^2 \sin^2(\theta)
\end{bmatrix}
$$
Using this, our **Einstein's Field Equations** reduce to a set of 4 coupled equations and our **Einstein Tensor** comes out to be, 
$$
G_{tt} = \frac{e^\nu}{r^2} (1 + e^{-\lambda}(r \lambda' - 1))$$
$$
G_{rr} = \frac{\nu'}{r} - \frac{e^\lambda}{r^2}(1 - e^{-\lambda})
$$
$$
G_{\theta \theta} = r^2 e^{-\lambda} \left( \frac{\nu''}{2} + \frac{\nu'^2}{4} = \frac{\nu'\lambda'}{4} + \frac{\nu' - \lambda'}{2r}  \right)
$$
$$
G_{\phi \phi} = \sin^2(\theta) G_{\theta \theta}
$$
Now our **LHS** is ready, but we still have one very important thing left to define and that is our energy momentum tensor, which will encode information about the mass-energy content of our compact body.
## The Energy Momentum Tensor :

![[A basic introduction to Neutron Star Equation of State (Polytropic Approach)-1786609947635.webp|628x437]]
This is the basic structure of a general Energy Momentum Tensor. For studying compact star interiors, we have to make certain assumptions about the matter content. We consider the matter to be a **perfect fluid**.

The **perfect fluid** is described as one with **no viscosity or conductivity** and if you consider an observer momentarily at rest with a *fluid element* (that is, the ***Momentarily co-moving Rest Frame (MCRF)***), you will also have a **constant, isotropic pressure (P)**. So we define the **Energy-Momentum Tensor for a Perfect Fluid** as follows,
$$
T^{\mu \nu} = (\epsilon + P) u^\mu u^\nu + (P)g^{\mu \nu}
$$
For our spherically symmetric space-time this comes out as,
$$
T^{\mu \nu} = 
\begin{bmatrix}
\epsilon ~ e^{-\nu} & 0 & 0 & 0 \\
0 & P ~ e^{-\lambda} & 0 & 0  \\
0 & 0 & P ~ r^{-2} & 0  \\
0 & 0 & 0 & P ~ (r^2 \sin^2\theta)^{-1}
\end{bmatrix}
$$
The covariant formulation (lower-indices) of the same will be,

$$
T_{}{\mu \nu} = 
\begin{bmatrix}
\epsilon ~ e^{\nu} & 0 & 0 & 0 \\
0 & P ~ e^{\lambda} & 0 & 0  \\
0 & 0 & P ~ r^{2} & 0  \\
0 & 0 & 0 & P ~ (r^2 \sin^2\theta)
\end{bmatrix}
$$
Now that we have fixed both the **LHS** and the **RHS**, we can write out the field equations as follows,
$$
\frac{\nu'}{r} - \frac{e^\lambda}{r^2}(1 - e^{-\lambda}) = 8 \pi \epsilon ~ e^\nu
$$
$$
\frac{\nu'}{r} - \frac{e^\lambda}{r^2}(1 - e^{-\lambda}) = 8 \pi P e^\lambda
$$
$$
r^2 e^{-\lambda} \left( \frac{\nu''}{2} + \frac{\nu'^2}{4} = \frac{\nu'\lambda'}{4} + \frac{\nu' - \lambda'}{2r}  \right) = 8 \pi Pr^2
$$
(The last equation corresponds to the $\theta \theta$ component and its the same as that for the $\phi \phi$ component, since the $sin^2 \theta$ will get cancelled out).

## Getting the Stellar Structure (TOV) Equations :

The first $tt$ equation can be written in the form of a "**mass equation**", 
$$
e^{-\lambda} = 1 - \frac{2}{r} \int^r_{0} 4 \pi r^2 \epsilon(r) ~ dr
$$
where we call the integral $\int^r_{0} 4\pi r^2 \epsilon(r) ~dr$ as the **gravitational mass enclosed within radius r**. We can re-write the equation as, 
$$
e^{-\lambda} = 1 - \frac{2m(r)}{r}
$$
When we reach the stellar surface, the above term actually matches that of the **Schwarzschild Metric** for spherically symmetric vacuum space-times, which ensures that our formulation is consistent and there are no discontinuities in our space-time. We can express the **rate-of-change for gravitational mass** as,
$$
\frac{dm}{dr} = 4 \pi r^2 \epsilon(r)
$$
We can solve the $rr$ equation to get a functional form for $\nu'$,
$$
\nu' = \left(1 + \frac{2m}{r}\right)^{-1} \left(8 \pi P r - \frac{2m}{r^2}\right)
$$
and we can also apply the **conservation of energy-momentum**, $\nabla_{\mu}T^{\mu \nu} = 0$, for the $r$ component.

We will eventually get a relation between the **pressure differential** and $\nu$ **differential** as,
$$
- \left(\frac{\epsilon + P}{2} \right) \frac{d\nu}{dr} = \frac{dP}{dr}
$$
On subsituting the the functional form for $\nu'$, we get the following relation,

$$
\frac{dP}{dr} = -\frac{(\epsilon + P)(4\pi Pr^3 + m)}{r(r-2m)}
$$
In fact we can re-arrange this and express it in the following fashion,
$$
\frac{dP}{dr} = - \frac{m}{r^2}(\epsilon + P) \left[1 + \frac{4\pi r^3P}{m}\right]\left[1 + \frac{2m}{r}\right]^{-1}
$$
In this form, the additional correction terms from **GR** are clearly visible when compared with the **Newtonian** expression for the same, 
$$
\frac{dP}{dr} = -\frac{m\rho}{r^2}
$$
where $\rho$ represents the rest-mass density.

> **Note:** We have taken the units c = G = 1

Thus in the end, we have the following **stellar-structure equations** (also known as the **Tolmann-Oppenheimer-Volkoff (TOV) equations**),

$$
\boxed{\frac{dP}{dr} = -\frac{(\epsilon + P)(4\pi Pr^3 + m)}{r(r-2m)}}
$$
$$
\boxed{\frac{dm}{dr} = 4 \pi r^2 \epsilon(r) }
$$

**YAYYYY!!!!**

However, if you look closely there's till something missing. We have a system of two coupled differential equations, but we have a total of three unknown variables, the **pressure**, the **energ-density** and the **mass**.

Thus to fully solve this system of equations, we need something more. A relation between the **pressure** and **energy density** within our compact star, something we call the **equation of state**.

_______
