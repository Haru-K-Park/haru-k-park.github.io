---
layout: post
title: "가우시안 앙상블"
author: "YGLENA"
comments: true
tags: [Random matrix theory, Stastical physics]
---

<details><summary>
<span style="font-size:2em;">**목차**</span>
</summary>
* 목차
{:toc}
</details>

## 가우시안 앙상블
**가우시안 앙상블<sup>Gaussian ensemble</sup>**이란, 가우시안 분포와 관련된 분포를 가지는 임의행렬<sup>random matrix</sup>을 말한다. 일반적으로 다음 세 가지 앙상블을 주로 논한다.

## 가우시안 직교 앙상블
크기가 $N$인 대칭 행렬<sup>symmetric matrix</sup> $H$에 대하여 각 성분 $H_{ij}$가 (대칭 조건을 제외하고) 독립적인 실수 가우스 확률분포<sup>Gaussian random variable</sup>를 가지고,

1. $\mathbb{E}[ H_{ij} ]=0$
2. $\mathbb{E}[ (H_{ij})^2 ]_{i\neq j}=N^{-1}$
3. $\mathbb{E}[ (H_{ij})^2 ]_{i=j}=2N^{-1}$

이면, 이를 **가우시안 직교 앙상블<sup>Gaussian orthogonal ensemble</sup>**이라 한다.

### 성질
> 크기가 $N$인 행렬 $A$에 대하여 각 성분 $A_{ij}$가 독립적인 실수 표준정규분포<sup>standard normal distribution</sup>를 가진다고 하자. 그러면 $\frac{A+A^T}{\sqrt{2N}}$는 가우시안 직교 앙상블이다.

<details><summary>**증명.**
</summary>

대각 성분의 경우, $\sqrt{\frac{2}{N}}\mathcal{N}(0,1)\sim \mathcal{N}(0,2N^{-1})$이다. 이 이외에는 

$$\frac{\mathcal{N}(0,1)+\mathcal{N}(0,1)}{\sqrt{2N}}\sim \frac{\mathcal{N}(0,2)}{\sqrt{2N}}\sim \mathcal{N}(0,N^{-1})$$

이다. $\square$
</details>

> 크기가 $N$인 가우시안 직교 앙상블 $H$와 직교 행렬 $Q$에 대하여, $Q^T H Q$는 $Q$와 같은 분포를 가진다.

<details><summary>**증명.**
</summary>

$(Q^T H Q)_ {ij}=Q_{ki}H_{kl}Q_{lj}$이다. 따라서

$$
\mathbb{E}(Q_{ki}Q_{lj}H_{kl})=Q_{ki}Q_{lj}\mathbb{E}(H_{kl})=0
$$

이고,

$$
\mathrm{Var}(Q_{ki}Q_{lj}H_{kl})=Q_{ki}^2Q_{lj}^2\mathrm{Var}(H_{kl})=Q_{ki}^2Q_{lj}^2\frac{(1+\delta_{kl})}{N}\delta_{kk}\delta_{ll}=\frac{1+\delta_{ij}}{N}
$$

이다. $\square$
</details>

> 크기가 $N$인 가우시안 직교 앙상블 $H$에 대하여, 확률변수를 행렬의 각 원소들로 둘 때 확률밀도함수<sup>probability density function</sup>는 다음과 같다.
>
>$$
Z_1^{-1}\exp\left[ -\frac{N}{4}\mathrm{Tr} H^2 \right]
>$$
>
>이 때 $Z_1$는 정규화 상수<sup>normalization constant</sup>이다.

<details><summary>**증명.**
</summary>
$\mathcal{N}(0,\sigma^2)$의 확률밀도함수는 다음과 같다.

$$
\frac{1}{\sqrt{2\pi \sigma^2}}\exp\left[ -\frac{x^2}{2\sigma^2}\right]
$$

따라서 가우시안 직교 앙상블 $H$의 확률밀도함수는 다음과 같이 쓸 수 있다.

$$
\prod_{i< j} \sqrt{\frac{N}{2\pi}}\exp\left[ -N\frac{H_{ij}^2}{2}\right] \prod_{i} \sqrt{\frac{N}{\pi}}\exp\left[ -N\frac{H_{ii}^2}{4}\right]
$$

상수항을 $Z_1^{-1}$로 쓰고 정리하면 다음을 얻는다.

$$
Z_1^{-1} \exp\left[-\frac{N}{4} \sum_{i,j}H_{ij}^2\right]
$$

대칭 행렬 조건에 의해 이는 준식과 같다. $\square$
</details>

### 위그너 행렬
실수 위그너 행렬<sup>real Wigner matrix</sup>은 가우시안 직교 앙상블의 일반화이다. 크기가 $N$인 대칭 행렬 $H$에 대하여, 각 성분 $H_{ij}$가 (대칭 조건을 제외하고) 독립적인 실수 변수이고,

1. $\mathbb{E}[ H_{ij} ]=0$
2. $i\neq j$일 때와 $i=j$일 때 각각 모든 분포가 동일하고,
3. $\mathbb{E}[ (H_{ij})^2 ]_{i\neq j}=N^{-1}$
4. $\mathbb{E}[ (H_{ij})^2 ]_{i=j}=CN^{-1}$
인 어떤 상수 $C$를 가질 때, 

이를 **실수 위그너 행렬**이라 한다.

## 가우시안 유니타리 앙상블
크기가 $N$인 에르미트 행렬<sup>Hermeitian matrix</sup> $H$에 대하여 각 성분 $H_{ij}$가 복소수 가우스 확률분포를 가지고,

1. $\mathbb{E}[ H_{ij} ]=0$
2. $\mathbb{E}[ \lvert H_{ij}\rvert^2 ]=N^{-1}$
3. $\mathbb{E}[ (H_{ij})^2 ]_{i\neq j}=0$

이면, 이를 **가우시안 유니타리 앙상블<sup>Gaussian unitary ensemble</sup>**이라 한다.

### 성질
> $H$가 가우시안 유니타리 앙상블임과 다음 조건들을 모두 만족함이 동치이다.
1. $H_{i,j}\rvert_{i\neq j}\sim \mathcal{N}(0,(2N)^{-1})+i\mathcal{N}(0,(2N)^{-1})$
2. $H_{i,j}\rvert_{i= j}\sim \mathcal{N}(0,N^{-1})$

<details><summary>**증명.**
</summary>

위의 조건을 만족하면 가우시안 유니타리 앙상블이 됨은 직접 계산을 통해 확인할 수 있다. $H$가 가우시안 유니타리 앙상블이라고 하면, 첫 번째 조건에 의하여 평균값은 0이 된다. $H_{ij}\sim X+iY$라 할 때, $i=j$이면 $X\simeq \mathcal{N}(0,1)$이며 $Y=0$이고, $i\neq j$이면 $\mathrm{Var}(X)+\mathrm{Var}(Y)=N^{-1}$이고 $\mathrm{Var}(X)-\mathrm{Var}(Y)=0$이므로 조건을 만족한다. $\square$
</details>

> 크기가 $N$인 행렬 $A$에 대하여 각 성분 $A_{ij}$가 독립적인 허수 표준정규분포를 가진다고 하자. 그러면 $\frac{A+A^*}{\sqrt{2N}}$는 가우시안 유니타리 앙상블이다.

<details><summary>**증명.**
</summary>

대각 성분의 경우, $\sqrt{\frac{2}{N}}\mathcal{N}(0,\frac{1}{2})\sim \mathcal{N}(0,N^{-1})$이다. 이 이외에는 허수부 및 실수부 모두

$$\frac{\mathcal{N}(0,\frac{1}{2})+\mathcal{N}(0,\frac{1}{2})}{\sqrt{2N}}\sim \frac{\mathcal{N}(0,1)}{\sqrt{2N}}\sim \mathcal{N}(0,(2N)^{-1})$$

이다. 위의 성질에 의하여 이는 가우시안 유니타리 앙상블이다.$\square$
</details>

> 크기가 $N$인 가우시안 유니타리 앙상블 $H$와 유니타리 행렬 $U$에 대하여, $U^* H U$는 $H$와 같은 분포를 가진다.

<details><summary>**증명.**
</summary>

$(U^* H U)_ {ij}=U_{ki}^*H_{kl}U_{lj}$이다. 따라서

$$
\mathbb{E}[ U_{ki}^*U_{lj}H_{kl} ]=Q_{ki}Q_{lj}\mathbb{E}[ H_{kl} ]=0
$$

이고,

$$
\mathbb{E}[ \lvert U_ {ki}^* U_ {lj}H_ {kl}\rvert^2 ]=\mathbb{E}[ \lvert U_{ki}^*\rvert^2\lvert U_{lj}\rvert^2\lvert H_{kl}\rvert^2 ]=\mathbb{E}[ \lvert H_{kl}\rvert^2 ]=N^{-1}
$$

이며,

$$
\mathbb{E}[ ( U_ {ki}^* U_ {lj}H_ {kl} )^2 ]=( U_ {ki}^* U_ {lj})^2\mathbb{E}[ H_ {kl} ^2 ]=0
$$

이다. $\square$
</details>

>크기가 $N$인 가우시안 유니타리 앙상블 $H$에 대하여, 확률변수를 행렬의 각 원소들로 둘 때 확률밀도함수는 다음과 같다.
>
>$$
Z_2^{-1}\exp\left[ -\frac{N}{2}\mathrm{Tr} H^2\right]
>$$
>
>이 때 $Z_2$는 정규화 상수이다.

<details><summary>**증명.**
</summary>

$\mathcal{N}(0,\sigma^2/2)+i\mathcal{N}(0,\sigma^2/2)$의 확률분포함수는 다음과 같다.

$$
\frac{1}{\sqrt{\pi\sigma^2}}\exp\left[ -\frac{|z|^2}{\sigma^2}\right]
$$

따라서 가우시안 유니타리 앙상블 $H$의 확률밀도함수는 다음과 같이 쓸 수 있다.

$$
\prod_{i< j}\sqrt{\frac{N}{\pi}}\exp\left[ -N\lvert H_{ij}\rvert ^2\right]\prod_{i}\sqrt{\frac{N}{2\pi}}\exp\left[-\frac{N}{2}H_{ii}^2 \right]
$$

상수항을 $Z_2^{-1}$로 쓰고 정리하면 다음을 얻는다.

$$
Z_2^{-1}\exp\left[-\frac{N}{2}\sum_{i,j}\lvert H_{i,j}\rvert^2 \right]
$$

에르미트 행렬 조건에 의해 이는 준식과 같다. $\square$

</details>

## 가우시안 심플렉틱 앙상블
크기가 $N$인 에르미트 사원수 행렬<sup>quaternionic matrix</sup> 에 대하여 각 성분 $H_{ij}$가

1. $H_{i,j}\rvert_{i\neq j}\simeq \mathcal{N}(0,(4N)^{-1})+i\mathcal{N}(0,(4N)^{-1})+j\mathcal{N}(0,(4N)^{-1})+k\mathcal{N}(0,(4N)^{-1})$
2. $H_{i,j}\rvert_{i=j}\simeq \mathcal{N}(0,(2N)^{-1})$

이면, 이를 **가우시안 심플렉틱 앙상블<sup>Gaussian symplectic ensemble</sup>**이라 한다.

### 성질
>크기가 $N$인 행렬 $A$에 대하여 각 성분 $A_{ij}$가 독립적인 사원수 표준정규분포를 가진다고 하자. 그러면 $\frac{A+A^*}{\sqrt{2N}}$는 가우시안 심플렉틱 앙상블이다.

<details><summary>**증명.**
</summary>

대각 성분의 경우, $\sqrt{\frac{2}{N}}\mathcal{N}(0,\frac{1}{4})\sim \mathcal{N}(0,(2N)^{-1})$이다. 이 이외에는 실수부 및 $i,j,k$항 모두

$$
\frac{\mathcal{N}(0,\frac{1}{4})+\mathcal{N}(0,\frac{1}{4})}{\sqrt{2N}}\sim \frac{\mathcal{N}(0,\frac{1}{2})}{\sqrt{2N}}\sim \mathcal{N}(0,(4N)^{-1})
$$

이다. $\square$
</details>

>크기가 $N$인 가우시안 심플렉틱 앙상블 $H$와 사원수 유니타리 행렬 $U$에 대하여, $U^{ *}HU$는 $H$와 같은 분포를 가진다. 사원수 행렬들을 크기가 $2N$인 복소 행렬로 나타내는 표현<sup>representation</sup>이 $\rho$이면, $\rho(U^{ *})\rho(H)\rho(U)$는 $\rho(H)$와 같은 분포를 가진다. 이 때 $\rho(U)$는 심플렉틱 행렬<sup>symplectic matrix</sup>이다.

<details><summary>**증명.**
</summary>

사원수 $w+xi+yj+zk$에 대하여, $(i,j,k)$를 $(i,j,-k)$, $(i,-j,-k)$, $(-i,-j,-k)$로 보내는 세 가지 함수 $f,g,h$와 그 자신을 생각할 수 있다. 이들의 곱이 주어져 있을 때 $w,x,y,z$들의 곱을 구할 수 있기 때문에, $H_{ij}$가 가우시안 심플렉틱 앙상블에 따른 분포를 가짐과, 각 성분 $H_{ij}$가 사원수 가우스 확률분포를 가지고 $\mathbb{E}[ H_{ij}]=0$이고 $\mathbb{E}[ \lambda(H_{ij})\lambda'(H_{ij})]$가 특정한 상수임이 동치이다. 이 때 $\lambda,\lambda'\in \\{ 1, f, g, h\\}$이다. 이들이 사원수 유니타리 행렬 변화에 대해 불변임은 가우시안 직교 및 유니타리 앙상블에 대해서 보인 것과 동일하게 보일 수 있다. $\square$
</details>

>크기가 $N$인 가우시안 심플렉틱 앙상블 $H$에 대하여, 확률변수를 행렬의 각 원소들로 둘 때 확률밀도함수는 다음과 같다.
>
>$$
Z_4^{-1}\exp\left[-N\mathrm{Tr}H^2 \right]
>$$
>
>이 때 $Z_4$는 정규화 상수<sup>normalization constant</sup>이다.

<details><summary>**증명.**
</summary>

$\mathcal{N}(0,\sigma^2/4)+i\mathcal{N}(0,\sigma^2/4)+j\mathcal{N}(0,\sigma^2/4)+k\mathcal{N}(0,\sigma^2/4)$의 확률분포함수는 다음과 같다.

$$
\sqrt{\frac{2}{\pi\sigma^2}}\exp\left[-\frac{2\lvert z\rvert^2}{\sigma^2} \right]
$$

따라서 가우시안 심플렉틱 앙상블 $H$의 확률밀도함수는 다음과 같이 쓸 수 있다.

$$
\prod_{i < j}\sqrt{\frac{2N}{\pi}}\exp\left[-2N\lvert H_{ij}\rvert^2 \right] \prod_{i}\sqrt{\frac{N}{2\pi}}\exp\left[ -N H_{ii}^2\right]
$$

상수항을 $Z_4^{-1}$로 쓰고 정리하면 다음을 얻는다.

$$
Z_4^{-1}\exp\left[ -N\sum_{i,j} \lvert H_{i,j}\rvert^2 \right]
$$

사원수 에르미트 행렬 조건에 의해 이는 준식과 같다. $\square$
</details>

## 일반화
위의 행렬이 모두 대각화 가능하며 실수 고유값을 가지기 때문에, 실수 고유값을 변수로 하여 확률밀도함수를 계산할 수 있다. 조금 더 구체적으로 다음을 얻는다.

> 가우시안 직교($\beta=1$), 유니타리($\beta=2$), 심플렉틱($\beta=4$) 앙상블에 대하여 확률밀도함수를 다음과 같이 쓸 수 있다.
>
>$$
Z_\beta^{-1}\prod_{i< j } \lvert \lambda_i - \lambda_j\rvert^\beta \exp\left[-\frac{\beta N}{4}\sum_{i=1}^n \lambda_i^2 \right]
>$$

<details><summary>**증명.**
</summary>

가우시안 직교 앙상블의 경우, 다음 곡선을 생각하자.

$$
t\mapsto M(t)=Q(t)\Lambda(t)Q(t)^T
$$

이 때, $M(0)$는 대칭 행렬이고, $\lambda(0)$는 그의 대각화이고, $Q(0)$는 $M$을 대각화시키는 직교 행렬이다. 이를 $t$에 관해 미분하고 $t=0$을 잡으면 다음을 얻는다.

$$
M'=Q'\Lambda Q^T+Q\Lambda'Q^T+Q\Lambda (Q^T)'
$$

이제 $Q'Q^T+Q(Q^T)'=0$이므로 $(Q^T)'=-Q^T Q' Q^T$이다. 따라서 다음을 얻는다.

$$
M'=Q\left(\Lambda'+\left[Q^T Q', \Lambda \right]\right) Q^T
$$

따라서, $Q^T Q'=A'$로 두면,

$$
dM^2=Q\left(d\Lambda^2 + d\Lambda\left[dA,\Lambda \right]+\left[dA,\Lambda \right]d\Lambda+\left[dA,\Lambda \right]^2\right)Q^T
$$

성분별로 나눈 뒤에 대각합을 취하면 $\mathrm{Tr}(d\Lambda [ dA,\Lambda])=0$임을 알 수 있다. 따라서

$$
\mathrm{Tr}(dM^2)=\sum_{j}d\lambda_j^2+\sum_{ij}(dA_{ij}\Lambda_{j}-\Lambda_{i}dA_{ij})(dA_{ji}\Lambda_{i}-\Lambda_{j}dA_{ji})
$$

$dA_{ij}=-dA_{ji}$이므로

$$
\mathrm{Tr}(dM^2)=\sum_{j}d\lambda_j^2+2\sum_{i< j}(\lambda_{i}-\lambda_{j})^2 dA_{ij}^2
$$


거리가 $ds^2=\sum_{ij}g_{ij}dx_i dx_j$로 주어질 때 부피 형식은 $Dx=\sqrt{\det(g)}\prod_{i}dx_i$이다. 따라서,

$$
DM=2^{n(n-1)/4}\prod_{i}d\lambda_i\prod_{i< j}\lvert \lambda_i - \lambda_j \rvert dA_{ij}
$$

그런데 또한

$$
\mathrm{Tr}(dM^2)=\sum_i M_{ii}^2+2\sum_{i< j} M_{ij}^2
$$

이므로,

$$
DM=2^{n(n-1)/4}\prod_{i}dM_{ii} \prod_{i< j} dM_{ij}
$$

이다. 따라서

$$
\prod_{i}dM_{ii} \prod_{i< j} dM_{ij}=\prod_{i}d\lambda_i\prod_{i< j}\lvert \lambda_i - \lambda_j \rvert dA_{ij}
$$

이다. 따라서 $\prod_{i< j}\lvert \lambda_i - \lambda_j \rvert$ 항이 곱해지게 된다.

가우시안 유니타리 앙상블의 경우, 실수부와 허수부 두 개의 행렬로 나뉘고, 각각이 $\prod_{i< j}\lvert \lambda_i - \lambda_j \rvert$ 항을 주게 된다. 따라서 $\prod_{i< j}\lvert \lambda_i - \lambda_j \rvert^2$ 항을 주게 된다. 마찬가지로 가우시안 심플렉틱 앙상블의 경우 $\prod_{i< j}\lvert \lambda_i - \lambda_j \rvert^4$ 항을 주게 된다.[^1] $\square$

</details>

[^1]: 이상의 증명은 G. Menon의 Lectures on Random Matrix Theory를 참고하였다.

이를 이용하여, 다음과 같이 일반적인 $\beta>0$에 대하여 가우시안 앙상블의 확률밀도함수를 일반화시킬 수 있다.

$$
Z_\beta^{-1}\prod_{i< j } \lvert \lambda_i - \lambda_j\rvert^\beta \exp\left[-\frac{\beta N}{4}\sum_{i=1}^n \lambda_i^2 \right]
$$

이를 **가우시안 $\beta$-앙상블<sup>Gaussian $\beta$-ensemble</sup>**이라 한다.

다음과 같은 행렬의 분포가 가우시안 $\beta$-앙상블의 확률밀도함수를 줌이 알려져 있다. 비어 있는 칸은 0을 의미하고, $\chi_k$는 카이 분포<sup>Chi distribution</sup>이다. $n$은 행렬의 크기이다. [^2]

$$
H_\beta \sim \frac{1}{\sqrt{2}}\begin{bmatrix}
\mathcal{N}(0,2) & \chi_{(n-1)\beta} &  & \cdots & \\\
\chi_{(n-1)\beta} & \mathcal{N}(0,2) & \chi_{(n-2)\beta} & \cdots &  \\\
 & \chi_{(n-2)\beta} & \mathcal{N}(0,2) & \cdots & \\\
\vdots & \vdots & \vdots & \ddots & \chi_\beta \\\
 &  & & \chi_\beta & \mathcal{N}(0,2)
\end{bmatrix}
$$

[^2]:I. Dumitriu와 A. Edelman의 [Matrix Models for Beta Ensembles](https://arxiv.org/abs/math-ph/0206043)를 참고하였다. 지수의 계수에서 약간의 차이가 있지만 이는 적절한 정규화를 통해 없앨 수 있다.

---