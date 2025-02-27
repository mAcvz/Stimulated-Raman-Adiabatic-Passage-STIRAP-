# Stimulated-Raman-Adiabatic-Passage-STIRAP-
This project explores the implementation and numerical simulation of Stimulated Raman Adiabatic Passage (STIRAP)—a coherent quantum state transfer technique. STIRAP enables population transfer between quantum states without losses due to spontaneous emission.



# Efficient Quantum State Transfer via Stimulated Raman Adiabatic Passage (STIRAP)

## Overview
This project focuses on the numerical simulation of **Stimulated Raman Adiabatic Passage (STIRAP)**—a quantum control technique that enables robust and efficient population transfer between quantum states. STIRAP operates via a counterintuitive pulse sequence that prevents population loss due to spontaneous emission, making it a fundamental tool in quantum information processing, atomic physics, and beyond.

## Problem Statement
STIRAP is a three-state quantum process that allows full population transfer from an initial state to a final state, without significant population in the intermediate state. This is achieved through the application of two coherent laser pulses—the **Stokes** (S) and **Pump** (P) pulses—arranged in a counterintuitive order. The system follows the **dark state**, ensuring robustness against experimental imperfections.

## Theoretical Background
### Hamiltonian of the System
The system is described by the time-dependent Hamiltonian:

$$
H(t) = \hbar
\begin{bmatrix}
0 & \frac{1}{2}\Omega_P(t) & 0 \\
\frac{1}{2}\Omega_P(t) & \Delta & \frac{1}{2}\Omega_S(t) \\
0 & \frac{1}{2}\Omega_S(t) & \delta
\end{bmatrix}.
$$

The Rabi frequencies are given by:

$$
\Omega_P(t) = -\frac{d_{12} \mathcal{E}_P(t)}{\hbar}, \quad
\Omega_S(t) = -\frac{d_{23} \mathcal{E}_S(t)}{\hbar}.
$$

### Detunings
#### Single-Photon Detuning
$$
\hbar \Delta_P = E_2 - E_1 - \hbar \omega_P, \quad
\hbar \Delta_S = E_2 - E_3 - \hbar \omega_S.
$$

#### Two-Photon Detuning
$$
\delta = \Delta_P - \Delta_S.
$$
In our case, we assume **resonant two-photon transitions**, meaning \(\delta = 0\).

### Instantaneous Eigenstates (Adiabatic States)
The eigenstates of the effective Hamiltonian are:

#### Bright States:
$$
\Phi_+ =
\begin{bmatrix}
\sin\theta(t) \sin\varphi(t) \\
\cos\varphi(t) \\
\cos\theta(t) \sin\varphi(t)
\end{bmatrix}, \quad
\varepsilon_+ = \frac{1}{2} \left[ \Delta + \sqrt{\Delta^2 + \Omega_{\text{rms}}^2(t)} \right],
$$

$$
\Phi_- =
\begin{bmatrix}
\sin\theta(t) \cos\varphi(t) \\
-\sin\varphi(t) \\
\cos\theta(t) \cos\varphi(t)
\end{bmatrix}, \quad
\varepsilon_- = \frac{1}{2} \left[ \Delta - \sqrt{\Delta^2 + \Omega_{\text{rms}}^2(t)} \right].
$$

#### Dark State (Associated with \(\varepsilon_0\))
The **dark state** is crucial in STIRAP since it avoids population in the lossy intermediate state:

$$
\Phi_0 =
\begin{bmatrix}
\cos\theta(t) \\
0 \\
-\sin\theta(t)
\end{bmatrix}, \quad
\varepsilon_0 = 0.
$$

where the mixing angles are defined as:

$$
\tan\theta(t) = \frac{\Omega_P(t)}{\Omega_S(t)}, \quad
\tan\varphi(t) = \frac{\Omega_{\text{rms}}(t)}{\sqrt{\Omega_{\text{rms}}^2(t) + \Delta^2 + \Delta}},
$$

and the root-mean-square Rabi frequency is:

$$
\Omega_{\text{rms}}(t) = \sqrt{\Omega_P^2(t) + \Omega_S^2(t)}.
$$

## Implementation Details
- **Programming Language**: Python
- **Simulation Tools**: Jupyter Notebook, NumPy, SciPy, Matplotlib
- **Key Features**:
  - Time evolution of the quantum system using numerical integration.
  - Visualization of state populations and adiabatic eigenenergies.
  - Analysis of the robustness of STIRAP against detuning and pulse imperfections.

## References
- N. V. Vitanov et al., "Stimulated Raman Adiabatic Passage in Physics, Chemistry and Beyond," [arXiv:1605.00224](https://arxiv.org/abs/1605.00224)

---
This `README.md` serves as an introduction to the theoretical background and numerical simulation aspects of STIRAP. Let me know if you'd like to refine any section!

