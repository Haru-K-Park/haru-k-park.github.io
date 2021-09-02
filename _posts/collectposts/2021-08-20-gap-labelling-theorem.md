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

Suppose that there is a gap on some Hamiltonian. Naturally, this gap separates the states with their eigenenergies below and above the gap, and thus we can correlate the gap by the projection operator $p$:

$$
p=p^*=p^2.
$$


By the _Gelfand-Naimark theorem_, we can consider $A$ as $C(X,M_n(\mathbb{C}))$ for some manifold $X$. Due to the _Serre-Swan theorem_, we can identify the projective operators with the $\mathbb{C}^r$-vector bundles over $X$, where $r$ is the rank of the projective operator. Two vector bundles are isometrically equivalent if and only if there is a continuous vector-space isometries between their fibres, which is the map $v\in C(X,iso_r(\mathbb{C}))$, and thus, extending $v$ to $u\in C(X,M_n(\mathbb{C}))$, we get $u^* u=p$ and $uu^* =q$. Thus, in the $K$-theory perspect, we can define an equivalence relation between two projections in a $C^*$-algebra $A$.

> **Definition.** Let $p,q$ be projection operators. Then we say $p$ and $q$ are **Murray-von Neumann(MvN) equivalent**, writing $p\sim q$, if there is $u\in A$ such that $p=u^* u$ and $q=uu^*$.

The unitary equivalence is not a very appropriate tool to describe this property, since there are MvN equivalent projection operators which are not unitary equivalent. Indeed, the following holds.

> **Proposition.** Let $p,q$ be projection operators. Then they are unitary equivalent if and only if the pairs $p,q$ and $1-p, 1-q$ are both MvN equivalent. 

Because the difference between two unequivalent projectors must be large, there is a lemma relating equivalence and norm of projections.

> **Lemma.** Let $p,q$ be projection operators. If $\lVert p-q\rVert<1$, then $p$ and $q$ are equivalent.

Therefore, any norm continuous path $t\in \mathbb{R}\rightarrow p(t)$ of the projections is made of mutually equivalent projections. Due to this distancing-properties of projection operators, there are only countably many equivalence classes of projections in a separable $C^*$-algebra.

Now, for the orthogonal projections, i.e. $pq=qp=0$, we can define their direct sum as $p+q$. This direct sum, actually, can be used to define the summation of two equivalence classes of projections.

> **Definition.** Let $p,q$ be projection operators. If there exists an orthogonal pair $p',q'$, satisfying $p\sim p'$ and $q\sim q'$, then we define $[p]+[q]$ as $[p+q]$.

This definition does not depends on the choice of $p'$ and $q'$. However, the existence of such orthogonal projection pair is not always insured. Hence we need to extend the $C^* $-algebra $A$.

> **Definition.** Denote $\mathcal{K}$ as the $C^* $-algebra of compact operators. We say a $C^* $-algebra $A$ is **stable** if $A\simeq A\otimes \mathcal{K}$.

Each elements in $A\otimes \mathcal{K}$ can be approximated in norm by a finite matrix $A\otimes M_N(\mathbb{C})$ for some $N\in \mathbb{N}$. This approximation also applies on the projections, and due to the equivalence between projections when their distance is not so far, we get the following lemma.

> **Lemma.** Let $p,q$ be projection operators in the stable $C^* $-algebra $A$. Then there is always a pair of orthogonal projectors, $p',q'\in A$, such that $p\sim p'$ and $q\sim q'$.

This makes the definition of summation of equivalence classes rigorously, and makes the commutative monoid of equivalence classes of the projectors.

It is possible to make an abelian group from the commutative monoid, which is called the _Grothendieck group_, by equating $[p]-[q]=[p']-[q']$ if $[p]+[q']=[p']+[q]$. We call this group $K_0(A)$, the **$0$-th K-group** of $A$. Naturally, the real-valued map defined on the equivalence classes of projections which is monoid homomorphism gives a group homomorphism from $K_0(A)$ to $\mathbb{R}$. For example, the trace map on $A$ gives a group homomorphism from $K_0(A)$ to $\mathbb{R}$, defined as we desire.