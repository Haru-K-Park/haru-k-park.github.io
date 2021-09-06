---
layout: post
title: "Eigenstate Thermalization Hypothesis"
comments: true
tags: [Quantum statistics, Ergodicity]
redirect_from: /gap-labelling-theorem
---
<details><summary>
<span style="font-size:2em;font-family: Helvetica;">**Contents**</span>
</summary>
* Contents
{:toc}
</details>

## Dynamics in isolated quantum systems
Consider the system with $L$ spins and Hamiltonian $H$, and its simple wavefunction $\vert\psi(t)\rangle=e^{-iHt}\vert\psi(0)\rangle$. We call this quantum system **ergodic** or **thermal** if, for any subsystem $\mathcal{A}$ with $L_{\mathcal{A}}\ll L$ spins, the reduced density matrix $\rho_\mathcal{A}(t):=\operatorname{Tr}_{\mathcal{A}^c}(\vert\psi(t)\rangle\langle\psi(t)\vert)$ evolves to a Gibbs density matrix:

$$
\lim_{t\rightarrow \infty} \rho_{\mathcal{A}}(t)=\rho_{\mathcal{A}}^{eq},\quad \rho^{eq}=\frac{1}{Z_\mathcal{A}}e^{-\beta H_{\mathcal{A}}}.
$$

Here $\beta$ is an inverse-temperature associated with the initial state, that is, the rest of the system acts like a thermal bath for the small subsystem $\mathcal{A}$.

The **Eigenstate Thermalization Hypothesis(ETH)** states that any eigenstate of the Hamiltonian at a finite energy density is thermal. Consider an initial state with energy variance $\Delta$, which is much smaller than the energy bandwidth $W$. Thus, we may represent $\vert\psi(0)\rangle = \sum_\alpha c_\alpha \vert E_\alpha\rangle$, where the coefficients $c_\alpha$ are significant only in an energy window $E\in [\overline{E}-\Delta,\overline{E}+\Delta].$ Then for some local operator $\hat{O}$, we have the expectation value

$$
\langle \hat{O}(t)\rangle=\sum_\alpha \lvert c_\alpha\rvert^2 O_{\alpha\alpha} + \sum_{\alpha\neq \beta}c_\alpha^* c_\beta O_{\alpha\beta}e^{i(E_\alpha-E_\beta)t}
$$

with $O_{\alpha\beta}=\langle E_\alpha\vert \hat{O}\vert E_\beta\rangle$. If there is no degeneracies in this spectrum, the time-averaging gives

$$
\lim_{T\rightarrow \infty}\frac{1}{T}\int_0^T dt\langle \hat{O}(t)\rangle = \sum_\alpha \lvert c_\alpha\rvert^2 O_{\alpha\alpha}.
$$

ETH hypothesis says that the long-time average is equal to the expectation value of a local operator in a microcanonical ensemble around energy $\overline{E}$, hence

$$
 \sum_\alpha \lvert c_\alpha\rvert^2 O_{\alpha\alpha} = \sum_{E_\alpha\in \left[ \overline{E}-\Delta,\overline{E}+\Delta \right]}O_{\alpha\alpha}.
$$

With the fact that $c_\alpha$'s are significant in the given energy window, we get

$$
\sum_{E_\alpha\in \left[\overline{E}-\Delta,\overline{E}+\Delta\right]}O_{\alpha\alpha}=\sum_{E_\alpha\in \left[\overline{E}-\Delta,\overline{E}+\Delta\right]}\lvert c_\alpha\rvert^2 O_{\alpha\alpha}.
$$

Thus, to satisfy the ETH hypothesis, $O_{\alpha\alpha}$ must depends on the energy $\overline{E}$, not its eigenstate energy $E_\alpha$. The formal ETH hypothesis is written in the form

$$
\langle E_m\vert \hat{O}\vert E_n\rangle = \overline{O}(E)\delta_{m,n} R_{m,n}\Omega(E)^{-1/2} f_0(E,\omega),
$$

where $E$ is the mean of $E_m,E_n$ and $\omega$ the difference, $R_{m,n}$ a pseudorandom variable with zero mean and unit variance, $\hat{O}(E)$ the thermal expectation value at $E$, $f_O(E,\omega)$ a smooth function, and $\Omega(E)$ the density of states(DOS).

## Broken Ergodicity

It is believed that most of the local interacting Hamiltonians are fully ergodic, and this is proven theoretically, experimentally and numerically in various systems. The problem is, in general, how we can prevent the system having a thermal distribution at all time.

### Integrability
The **integrable system** has an extensive number of conserved quantities, thus its energy spectrum can be completely solvable in principle. There are some examples such as non-interaction Hamiltonian, toric code, Bethe ansatz, and more. Because of the deterministic property of integrable system, it does not satisfies the ETH hypothesis.

However, because of the strict condition of integrability, it is not a robust property and a little perturbation can break integrability. Therefore, a fine-tuned experiment can only realize the interaction integrable system, which is a very hard task.

### Many-body localization
Many-body localization (MBL) is the generalization of Anderson localization to interacting systems. It is believed that in the presence of strong disorder or quasiperiodicity MBL occurs, but its stability in thermodynamical limit is not determined and still in debate.

MBL eigenstates are however easier to distinguish from thermal eigenstates than integrable eigenstates, because the former ones are area-low entangled but the latter and ergodic eigenstates are volume-law entangled.

### Quantum scars
Ergodicity breaking can be strongly broken, which implies that a lots of states lose their ergodicity, but also can be **weakly broken**, that is, a small (mathematically, measure zero) portion of the initial states only violates ETH. We call such ETH-violating eigenstates in the middle of the spectrum as **quantum many-body scars (QMBS)**.

### Hilbert space fragmentation
Finally, suppose that the Hilbert space splits into exponentially many dynamically disconnected parts, so that some particular initial states cannot evolve into the large part of states. Such inaccessibility can occur on a measure zero set, called **weak fragmentation**, or not, called **strong fragmentation**. As we can expect, weakly fragmented system only breaks strong ETH, but strongly fragmented system breaks both strong and weak ETH.

## References
1. S. Moudgalya, B. Andrei Bernevig, and N. Regnaul, [Quantum Many-Body Scars and Hilbert Space Fragmentation: A Review of Exact Results](https://arxiv.org/pdf/2109.00548.pdf), arxiv:2019.00548
2. M. Sredniki, [Chaos and quantum thermalization](https://journals.aps.org/pre/pdf/10.1103/PhysRevE.50.888), Phys. Rev. E 50, 888 (1994)