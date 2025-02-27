# Stimulated-Raman-Adiabatic-Passage-STIRAP-
This project explores the implementation and numerical simulation of Stimulated Raman Adiabatic Passage (STIRAP)—a coherent quantum state transfer technique. STIRAP enables population transfer between quantum states without losses due to spontaneous emission.



The instant eigenstates of the of the effective Hamiltonian also known ad adiabatic state:
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
\varepsilon_- = \frac{1}{2} \left[ \Delta - \sqrt{\Delta^2 + \Omega_{\text{rms}}^2(t)} \right],
$$

#### Dark state (associated with \(\varepsilon_0\))

$$
\Phi_0 = 
\begin{bmatrix}
\cos\theta(t) \\
0 \\
-\sin\theta(t)
\end{bmatrix}, \quad 
\varepsilon_0 = 0,
$$

$$
\tan\theta(t) = \frac{\Omega_P(t)}{\Omega_S(t)}, \quad 
\tan\varphi(t) = \frac{\Omega_{\text{rms}}(t)}{\sqrt{\Omega_{\text{rms}}^2(t) + \Delta^2 + \Delta}}, \quad 
\Omega_{\text{rms}}(t) = \sqrt{\Omega_P^2(t) + \Omega_S^2(t)}.
$$

