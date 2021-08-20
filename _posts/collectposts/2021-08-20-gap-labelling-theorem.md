---
layout: post
title: "Gap Labeling Theorem"
comments: true
tags: [Algebra]
redirect_from: /gap-labelling-theorem
---
<details><summary>
<span style="font-size:2em;font-family: Helvetica;">**Contents**</span>
</summary>
* Contents
{:toc}
</details>

&ensp;Suppose that there is a gap on some Hamiltonian. Naturally, this gap separates the states with their eigenenergies below and above the gap, and thus we can correlate the gap by the projection operator $p$:

$$
p=p^*=p^2.
$$


&ensp;By the _Gelfand-Naimark theorem_, we can consider $A$ as $C(X,M_n(\mathbb{C}))$ for some manifold $X$. Due to the _Serre-Swan theorem_, we can identify the projective operators with the $\mathbb{C}^r$-vector bundles over $X$, where $r$ is the rank of the projective operator. Two vector bundles are isometrically equivalent if and only if there is a continuous vector-space isometries between their fibres, which is the map $v\in C(X,iso_r(\mathbb{C}))$, and thus, extending $v$ to $u\in C(X,M_n(\mathbb{C}))$, we get $u^* u=p$ and $uu^* =q$. Thus, in the $K$-theory perspect, we can define an equivalence relation between two projections in a $C^*$-algebra $A$.

> **Definition.** Let $p,q$ be projection operators. Then we say $p$ and $q$ are **Murray-von Neumann(MvN) equivalent**, writing $p\sim q$, if there is $u\in A$ such that $p=u^* u$ and $q=uu^*$.

&ensp;The unitary equivalence is not a very appropriate tool to describe this property, since there are MvN equivalent projection operators which are not unitary equivalent.

&ensp;Because the difference between two unequivalent projectors must be large, there is a lemma relating equivalence and norm of projections.

> **Lemma.** Let $p,q$ be projection operators. If $\|p-q\|<1$, then $p$ and $q$ are equivalent.

&ensp;Therefore, any norm continuous path $t\in \mathbb{R}\rightarrow P(t)$ of the projections is made of mutually equivalent projections.

&ensp;Due to this distancing-properties of projection operators, there are only countably many equivalence classes of projections in a separable $C^*$-algebra.