---
layout: post
title: "Topology on Non-Hermitian Systems"
comments: true
tags: [Topology, Non-Hermitian system]
redirect_from: /gap-labelling-theorem
---
<details><summary>
<span style="font-size:2em;font-family: Helvetica;">**Contents**</span>
</summary>
* Contents
{:toc}
</details>

Consider, on a 2-dimensional momentum space $\vec{k}=(k_x,k_y)$, a following non-Hermitian Hamiltonian.

$$
\hat{H}=\begin{bmatrix}
    k_x-isk_y & m\\
    m& -k_x+is k_y
\end{bmatrix} = (k_x-isk_y)\hat{\sigma_z}+m\hat{\sigma_x}.
$$

Here the parameter $m$, called "mass", is real, and $s=\pm 1$. We may set $\vec{B}=(B_x,B_y,0)$ with $B_x=k_x-isk_y$ and $B_y=m$ as an effective complex-valued magnetic field, thus can write $\hat{H}=\vec{B}\cdot \vec{\hat{\sigma}}$ where $\vec{\hat{\sigma}}=(\hat{\sigma}_z,\hat{\sigma}_x,\hat{\sigma}_y)$.

Notice that the Hamiltonian $\hat{H}$ has both the chiral symmetry $\{\hat{H},\hat{\sigma}_y\}=0$ and $\mathcal{PT}$-symmetry when we consider $\mathcal{P}$ the reflection $x\rightarrow -x$.

Now, the eigenvalues of $\hat{H}$ are $\lambda^\pm = \pm\sqrt{m^2+(k_x-isk_y)^2}$ with eigenvectors $\psi=\begin{bmatrix} 1 \\ B_y/(B_x+\lambda^\pm)\end{bmatrix}$.

<script src="https://utteranc.es/client.js"
        repo="[ENTER REPO HERE]"
        issue-term="pathname"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>