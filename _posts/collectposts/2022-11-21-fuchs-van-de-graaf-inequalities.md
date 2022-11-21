---
layout: post
title: "Fuchs-van de Graaf inequalities"
comments: true
tags: [Quantum informations]
---
<details><summary>
<span style="font-size:2em;font-family: Helvetica;">**Contents**</span>
</summary>
* Contents
{:toc}
</details>

## Fidelity
Fidelity measures the overlap between two states; it is related to the transmission probability from one state to the other. For the pure states $\rho=|\psi\rangle\langle \psi|$ and $\sigma = |\phi\rangle\langle \phi|$, the fidelity is defined as following:

$$
F(\rho,\sigma)=|\langle \psi|\phi\rangle|.
$$

For the mixed state case, we need to _purify_ the states $\rho$ and $\sigma$.

> **Definition.** Let $\rho$ be a density operator on Hilbert space $\mathcal{H}_A$. Then a **purification** $\lvert \Phi \rangle$ of the state $\sigma$ is a state on the Hilbert space $\mathcal{H}_A \otimes \mathcal{H}_B$ satisfying
>
>$$
\mathcal{\rho}=\textrm{Tr}_B\left[\lvert\Phi\rangle\langle\Phi\rvert\right].
>$$

> **Theorem.** Every density operator $\rho$ has its pure state.
<details><summary>**Proof.**
</summary>

Consider the diagonalization $\rho=\sum_{i} p_i \lvert \psi_i\rangle\langle\psi_i \rvert$, and vectors $\lvert \phi_i\rangle$ independent to $\lvert \psi_i\rangle$'s. Take

$$
|\Phi\rangle = \sum_i \sqrt{p_i} \lvert \psi_i \rangle \otimes \lvert \phi_i \rangle.
$$

</details>

Notice that purification is not unique.

> **Definition.** Let $\rho,\sigma$ be two density operators on a Hilbert space $\mathcal{H}$, and $P_{\rho}, P_{\sigma}$ be the set of their purifications respectively. Then, the **fidelity** between $\rho$ and $\sigma$ is defined as
>
>$$
F(\rho,\sigma) := \max_ {\lvert \Phi\rangle\in P_{\rho}, \lvert\Psi\rangle \in P_{\sigma}} \lvert \langle \Phi\rvert \Psi\rangle \rvert.
>$$