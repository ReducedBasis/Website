---
title: NIRB 2-grid
weight: 4
---

# Description

Offline-Online Decomposition:
- A non-intrusive reduced basis method to return computationally efficient and accurate CFD simulations

- Two-grid finite element/finite volume scheme used.

- A user-friendly reduced basis method to reduce computational cost of CFD simulations.

- Parametric study


The design parameters can be of geometric nature or related to the boundary conditions. This motivates our interest on model reduction and particularly on reduced basis methods. As is well documented in the literature, the offline/online implementation of the standard RB method (a Galerkin approach within the reduced basis space) requires to modify the original CFD calculation code, which for a commercial one may be problematic even impossible. For this reason, we have proposed in a previous paper, with an application to a simple scalar convection diffusion problem, an alternative non-intrusive reduced basis approach (NIRB) based on a two-grid finite element discretization. Here also the process is two stages: offline, the construction of the reduced basis is performed on a fine mesh; online a new configuration is simulated using a coarse mesh. While such a coarse solution, can be computed quickly enough to be used in a rapid decision process, it is generally not accurate enough for practical use. In order to retrieve accuracy, we first project every such coarse solution into the reduced space, and then further improve them via a rectification technique. 
## Offline
 A Greedy or POD procedure;

## Online
Acoarse solution; may involve a rectification matrix  

# Code:
[Code with FreeFem++](/uploads/NIRB.edp)

# References

- [Chakir, R., Maday, Y., Parnaudeau, P. (2019). A non-intrusive reduced basis approach for parametrized heat transfer problems. Journal of Computational Physics, 376, 617-633.](https://www.sciencedirect.com/science/article/pii/S0021999118306570?casa_token=ypCz1682c_QAAAAA:Lluz2uJZyqwPWNiRxEfPn-yVjAE1wO2-fLUjnQnYUq7OQ6rsvi4xfo9SxvGCd1WqjTjn3Ad_rFU)

- [Grosjean, E., & Maday, Y. (2021). Error estimate of the non-intrusive reduced basis method with finite volume schemes. ESAIM: Mathematical Modelling and Numerical Analysis, 55(5), 1941-1961](https://www.esaim-m2an.org/articles/m2an/abs/2021/06/m2an210043/m2an210043.html)