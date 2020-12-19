---
layout: post
title: "크리스토펠-다르부 식"
author: "YGLENA"
comments: true
tags: [Calculus]
---
* 
{:toc}
## 정의
### 적률 범함수
$\\{\mu_n\\}_{n=0}^{\infty}$가 복소수 순열이고, $\mathcal{L}$이 실변수 다항식에서 복소수로 향하는 선형함수라 할 때, 다음을 만족한다고 하자.

$$
\mathcal{L}\left[ x^n \right]=\mu_n
$$

그러면 $\mathcal{L}$을 **적률 범함수<sup>moment functional</sup>**이라 하고, $\\{\mu_n\\}$을 **적률 순열<sup>moment sequence</sup>** 혹은 단순히 **적률<sup>moment</sup>**이라 한다. 

적률 범함수 $\mathcal{L}$이 $0$이 아니고 항상 $p(x)\geq 0$인 다항함수 $p$에 대하여 $\mathcal{L}[p(x) ]>0$일 때, 이를 **양의 정부호<sup>positive definite</sup>** 적률 범함수라 한다.

### 직교 다항식
적률 범함수 $\mathcal{L}$에 대하여, 다항함수 순열 $\\{P_{n}(x)\\}_{n=0}^{\infty}$가 다음을 만족한다고 하자.

1. $P_n(x)$는 $n$차 다항식이다.
2. **[직교성 조건.]** $\mathcal{L}\left[P_m(x)P_n(x) \right]=K_n \delta_{mn}$이다. 이 때 $K_n\neq 0$이다.

이 때 이 다항함수 순열을 **직교 다항식<sup>orthogonal polynomial</sup>**이라 한다.

## 성질
복소수 $\mu_0,\cdots,\mu_{2n}$에 대하여, 행렬

$$
(\mu_{i+j})_{i+1,j+1}=\begin{bmatrix}
\mu_0&\mu_1&\cdots&\mu_n\\\
\mu_1&\mu_2&\cdots&\mu_{n+1}\\\
\vdots&\vdots&\ddots&\vdots\\\
\mu_n&\mu_{n+1}&\cdots&\mu_{2n}
\end{bmatrix}
$$

을 **한켈 행렬<sup>Hankel matrix</sup>**이라 한다.

> 적률 범함수 $\mathcal{L}$이 적률 순열 $\\{\mu_n\\}$를 가진다고 하자. 이 때 적률 범함수가 직교 다항식을 가짐과, 적률 순열의 부분순열 $\\{\mu_n\\}\rvert_{0,\cdots,m}$에 대한 한켈 행렬의 행렬식 $\Delta_m$이 항상 $0$이 아님이 동치이다.

<details><summary>**증명.**
</summary>

어떤 다항식 $P_n=\sum_{k=0}^n c_{nk}x^k$에 대하여, $m\leq n$일 때 $\mathcal{L}\left[ x^m P_n(x)\right]=\sum_{k=0}^n c_{nk}\mu_{k+m}$이므로, 직교성 조건은 다음과 동치이다.

$$
\begin{bmatrix}
\mu_0&\mu_1&\cdots&\mu_n\\\
\mu_1&\mu_2&\cdots&\mu_{n+1}\\\
\vdots&\vdots&\ddots&\vdots\\\
\mu_{n}&\mu_{n+1}&\cdots&\mu_{2n}
\end{bmatrix}\begin{bmatrix}
c_{n0}\\\ c_{n1}\\\ \vdots \\\ c_{nn}
\end{bmatrix}=\begin{bmatrix}
0\\\  0\\\ \vdots \\\ K_n
\end{bmatrix}
$$

직교다항식이 존재한다면 위의 식이 단일해를 가지므로 $\Delta_n\neq 0$이다. 거꾸로 $\Delta_n\neq 0$이면 어떤 $K_n$\neq 0에 대하여 위의 식이 단일해를 가진다. 또한 $\mu_{0,\cdots, 2n}$의 한켈 행렬의 역행렬 $(n+1,n+1)$-성분값이 $\frac{\Delta_{n-1}}{\Delta_n}$이므로,

$$
c_{nn}=\frac{K_n \Delta_{n-1}}{\Delta_n}\neq 0
$$

이고 따라서 $P_n$은 $n$차 다항식이다. $\square$

</details>

> 양의 정부호 적률 범함수는 실수 적률과 실수 직교 다항식을 가진다.

<details><summary>**증명.**
</summary>

$\mu_{2n}=\mathcal{L}[x^n{2n} ]>0$이므로 짝수 적률은 모두 실수이다. 또한

$$
\mathcal{L}[ (x+1)^{2n}]=\sum_{k=0}^{2n+1}\binom{2n}{k}\mu_{2n-k}>0
$$

이므로, 귀납법을 사용하면 홀수 적률 또한 실수이다. 

$p_0(x)=\mu_0^{-1/2}$로 두고, $a_k=\mathcal{L}[ x^{n+1} p_k(x)]$로 정의하여 귀납적으로 $P_{n+1}(x)=x^{n+1}-\sum_{k=0}^n a_k p_k(x)$로 쓴다. 그러면

$$
\mathcal{L}[ p_j(x)P_{n+1}(x)]=\mathcal{L}[ x^{n+1} p_j(x)]-\sum_{k=0}^n a_k \mathcal{L}[ p_j(x) p_k(x)]=a_j-a_j=0
$$

$\square$

</details>