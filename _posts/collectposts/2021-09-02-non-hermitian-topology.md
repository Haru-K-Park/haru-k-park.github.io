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

## Topology and non-Hermitian system

Consider, on a 2-dimensional momentum space $\vec{k}=(k_x,k_y)$, a following non-Hermitian Hamiltonian.

$$
\hat{H}=\begin{bmatrix}
    k_x-isk_y & m\\
    m& -k_x+is k_y
\end{bmatrix} = (k_x-isk_y)\hat{\sigma_z}+m\hat{\sigma_x}.
$$

Here the parameter $m$, called "mass", is real, and $s=\pm 1$. We may set $\vec{B}=(B_x,B_y,0)$ with $B_x=k_x-isk_y$ and $B_y=m$ as an effective complex-valued magnetic field, thus can write $\hat{H}=\vec{B}\cdot \vec{\hat{\sigma}}$ where $\vec{\hat{\sigma}}=(\hat{\sigma}_z,\hat{\sigma}_x,\hat{\sigma}_y)$.

Notice that the Hamiltonian $\hat{H}$ has both the chiral symmetry $\{\hat{H},\hat{\sigma}_y\}=0$ and $\mathcal{PT}$-symmetry when we consider $\mathcal{P}$ the reflection $x\rightarrow -x$.

Now, the eigenvalues and eigenvectors of $\hat{H}$ are the followings.

$$
\lambda^\pm = \pm\sqrt{m^2+(k_x-isk_y)^2},\quad \psi^\pm=\begin{bmatrix} 1 \\ B_y/(B_x+\lambda^\pm)\end{bmatrix}
$$

Consider the $k_y$ axis, i.e. $k_x=0$. Then $\lambda^\pm=\pm\sqrt{m^2-k_y^2}$, implying that the eigenenergies are purely imaginary when $\lvert k_y\rvert > \lvert m\rvert$, which gives ungapped spectrum of $\operatorname{Re}(\lambda)$, and purely real when $\lvert k_y\rvert<\lvert m\rvert$, giving gapped spectrum.

Notice that, at the exceptional point $(0,\pm\lvert m\rvert)$, we obtain not just the zero eigenvalues, but also the defective single chiral eigenmode, an eigenvector of $\hat{\sigma}_y$.

By taking $\hat{\vec{k}}=-i\vec{\nabla}$, we get

$$
\hat{H}=\left[-i\partial_x -s(x,y)\partial_y \right]\hat{\sigma}_z+m(x,y)\hat{\sigma}_x.
$$

Suppose that there are two uniform media with different $m_i,s_i$ values for $i=1,2$. for edge mode, we have the solution

$$
\begin{bmatrix}
\alpha\\ \beta
\end{bmatrix} \begin{cases}
e^{ik_yy+\kappa_1 x},& x>0\\
e^{ik_yy+\kappa_2 x},& x<0
\end{cases}
$$

which can be normalized when $\operatorname{Re}\kappa_1 < 0$ and $\operatorname{Re}\kappa_2 > 0$. In the zero-energy case, we have conditions $-\kappa_i=s_i k_y\pm m_i$.

Suppose that $s_1=s_2=s$ and $m_1=-m_2=m$, thus the conditions become

$$
-\kappa_1=sk_y \pm m,\quad -\kappa_2=sk_y\mp m.
$$

Mutliplying these gives $\kappa_1 \kappa_2 = k_y^2-m^2 < 0$, thus there is only one solution when $\lvert k_y\rvert<m$ and no solution when $\lvert k_y\rvert>m$. Notice that $k_y=0$ case has one solution, which makes the Hamiltonian $\hat{H}$ the _Jackiw-Rebbi model_.

Now suppose that $s_1=-s_2=s$ and $m_1=m_2=m$, thus the conditions become

$$
-\kappa_1=sk_y\pm m,\quad -\kappa_2=-sk_y\pm m
$$

and again multiplying these gives $\kappa_1\kappa_2=m^2-k_y^2$. Thus, in this case, there are two edge modes when $k\in \operatorname{sgn}(s)(\lvert m\rvert,\infty)$, with opposite chiralities.

From the Jackiw-Rebbi model case, we expect to find out some topological winding number which can distinguish the different topological states. One may expect that the winding number of eigenvectors

$$
\psi^\pm=\begin{bmatrix} 1 \\ B_y/(B_x+\lambda^\pm)\end{bmatrix}
$$

may play the role. However, winding the exceptional point swaps the band, which makes impossible to distinguish two bands.

Consider the spherical representation of the "magnetic" field $\vec{B}$, $\vec{B}=B(\sin\theta \cos\phi,\sin\theta \sin\phi,\cos\theta)$. Because, in our case, $\vec{B}$ is an imaginary vector, the values $B,\theta,\phi$ may be complex. Due to the chiral symmetry, we have $\theta=\pi/2$.

Now define

$$
w_1=\frac{1}{2\pi}\int_{k_x=-\infty}^{+\infty} \vec{\nabla}_{\vec{k}}\phi\cdot d\vec{k}
$$

as the winding number. Here, the integration is done along the $k_x$-axis. Then, for the Hamiltonian $\hat{H}$, we get

$$
w_1=\begin{cases}
-\frac{1}{2}\operatorname{sgn}(m),&\lvert k_y\rvert < \lvert m \rvert \\
0,&\lvert k_y\rvert>\lvert m\rvert.
\end{cases}
$$

This explains the appearance of edge current when $s_1=s_2=s$ and $m_1=-m_2=m$. However, because $w_1$ only depends on $m$, it does not explains the appearance of edge current when $m_1=m_2=m$ and $s_1=-s_2=s$. To do this, we define another winding number

$$
w_2=\frac{1}{2\pi} \int_{k_x=-\infty}^{+\infty} \vec{\nabla}_{\vec{k}}\operatorname{Arg}(\lambda^+)\cdot d\vec{k}.
$$

This gives

$$
w_2=\begin{cases}
0,&\lvert k_y\rvert<\lvert m\rvert\\
\frac{1}{2}\operatorname{sgn}(sk_y),& \lvert k_y\rvert > \lvert m\rvert,
\end{cases}
$$

and explains the other appearance of edge current.

## References
D. Leykam, K. Y. Bliokh, C. Huang, Y. D. Chong, and F. Nori, [Edge Modes, Degeneracies, and Topological Numbers in Non-Hermitian Systems, Phys. Rev. Lett. 118, 040401](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.040401)