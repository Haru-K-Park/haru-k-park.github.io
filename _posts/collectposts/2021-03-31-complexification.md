---
layout: post
title: "복소화"
author: "YGLENA"
comments: true
tags: [Abstract algebra, Complex analysis]
redirect_from: /complexification
---
<details><summary>
<span style="font-size:2em;font-family: Helvetica;">**목차**</span>
</summary>
* 목차
{:toc}
</details>

## 선형 복소 구조
실수 $\mathbb{R}$ 위에서 정의된 벡터 공간 $V$에 대하여, 선형 변환 $J:V\rightarrow V$이 $J^2=-1_V$를 만족시키면 이를 **선형 복소 구조<sup>linear complex structure</sup>**라 한다.

### 성질
>실수 벡터 공간 $V$에 선형 복소 구조 $J$가 부여되어 있으면, $V$에 복소 벡터 공간 구조를 부여한 복소 벡터 공간 $V_J$를 얻을 수 있다.

<details><summary>**증명.**
</summary>

다음과 같이 정의하자.

$$
(a+bi)v=av+bJ(v),\quad a,b\in \mathbb{R},\quad v\in V
$$

이것이 다음을 만족함을 보이기만 하면 된다.

$$
(a+bi)\left((c+di)v\right)=\left((a+bi)(c+di)\right)v
$$

좌변의 경우,

$$
(a+bi)\left(cv+dJ(v)\right)=acv+adJ(v)+bcJ(v)-bdv
$$

그리고 우변의 경우

$$
(ac-bd+(ad+bc)i)v=(ac-bd)v+(ad+bc)J(v)
$$

가 되어, 같은 결과를 준다.
</details>

## 복소화
실수 $\mathbb{R}$ 위에서 정의된 벡터 공간 $V$에 대하여, 이것의 **복소화<sup>complexification</sup>**는 다음과 같이 정의된 복소 벡터 공간이다.

$$
V^{\mathbb{C}}\equiv V\otimes_{\mathbb{R}}\mathbb{C}
$$

이는 실수 벡터 공간의 텐서곱<sup>tensor product</sup>이므로 실수 벡터 공간이지만, 다음과 같은 복소수 스칼라 곱을 자연스럽게 정의할 수 있다.

$$
\alpha(v\otimes \beta)\equiv(v\otimes\alpha\beta),\quad \alpha,\beta\in \mathbb{C}
$$

복소화 공간 $V^{\mathbb{C}}$ 위에서 켤레 복소는 다음 성질을 만족하도록 선형으로 정의된다.

$$
\overline{v\otimes z}= v\otimes \overline{z}
$$

또한, 선형 함수 $f:V\rightarrow W$로부터 자연스럽게 $f^{\mathbb{C}}:V^{\mathbb{C}}\rightarrow W^{\mathbb{C}}$를 정의할 수 있다. 이는 다음과 같은 성질을 가진다.

$$
f^{\mathbb{C}}(v\otimes \alpha)=f(v)\otimes \alpha
$$

### 성질
>모든 $v\in V^{\mathbb{C}}$는 유일한 $v_r,v_{im}\in V$에 대하여 $v_r\otimes 1+v_{im}\otimes i$로 쓰여진다.

<details><summary>**증명.**
</summary>

텐서곱의 정의에 의해, $v\in V^{\mathbb{C}}$는 유한합 $\sum_i v_i \otimes \alpha_i$로 써진다. $\alpha_i=a_i+b_i i$일 때 이는 $\sum_i v_i\otimes a_i + \sum_i v_i\otimes b_i i$가 되고,

$$
v_r\equiv \sum_i a_iv_i,\quad v_{im}\equiv \sum_i b_iv_i
$$

로 정의하면 $v=v_r\otimes 1+v_{im}\otimes i$가 된다.

</details>

>실수 벡터 공간 $V$의 자기 자신에 대한 직합 $V\oplus V$를 생각하고, 이 위에서 다음과 같이 정의된 선형 연산자를 생각하자.
>
>$$
J(v,w)=(-w,v),\quad \forall v,w\in V
>$$
>
>그렇다면 $J$는 $V\oplus V$ 위에서 정의된 선형 복소 구조이다.

<details><summary>**증명.**
</summary>

$J^2=-1_{V\oplus V}$이므로, 선형 복소 구조의 정의에 의해 성립한다.

</details>

>실수 벡터 공간 $V$ 위에 선형 복소 구조 $J$가 정의되어 있다면, $V$의 복소화 공간 $V^{\mathbb{C}}$를 다음과 같이 분해할 수 있다.
>
>$$
V^{\mathbb{C}}=V^+\oplus V^-
>$$
>
>이 때, 이 두 개의 공간은 변환 $J$의 고유 공간이고, $\mathbb{R}$ 벡터 공간으로써 $V_J$와 일치하며, $V^{\mathbb{C}}$ 위에서 서로의 복소 켤레가 된다. 또한,
>
>$$
V^{\pm}\equiv \{v\otimes 1\mp J(v)\otimes i:v\in V\}
>$$
>
>이라 쓸 수 있다.

<details><summary>**증명.**
</summary>

$J$가 $V$ 위의 선형 연산자이므로, 우리는 다음과 같이 $J$를 $V^{\mathbb{C}}$ 위의 선형 원산자 $J^{\mathbb{C}}$로 확장할 수 있다.

$$
J^\mathbb{C}(v\otimes z)=J(v)\otimes z
$$

$\mathbb{C}$가 대수적으로 닫혀 있으므로 $J^\mathbb{C}$는 $\lambda^2=-1$을 만족시키는 고유값 $\lambda$를 가져야 한다. 따라서 $J$의 고유값은 $\pm i$이고, $J$가 역행렬이 존재하기 때문에 각각의 고유 공간을 $V^{\pm}$으로 쓰면

$$
V^{\mathbb{C}}=V^+\oplus V^-
$$

를 얻는다.

$v\equiv v_r\otimes 1 + v_{im}\otimes i\in V^+$에 대하여 $J^{\mathbb{C}}(v)=v\otimes i$이고 $J^{\mathbb{C}}(v)=J(v_r)\otimes 1+J(v_{im})\otimes i$이다. 또한, $\overline{v}=v_r\otimes 1-v_{im}\otimes i$이므로, $J^{\mathbb{C}}(\overline{v})=J(v_r)\otimes 1-J(v_{im})\otimes i = \overline{J^{\mathbb{C}}(v)}=v\otimes (-i)$를 얻는다. 따라서 $\overline{v}\in V^{-}$이다. $V^-$에서 $V^+$로의 변환을 생각해도 마찬가지가 성립한다.

각 집합으로의 사영 변환 $P^{\pm}\equiv \frac{1}{2}\left( 1\mp iJ\right)$를 생각하면 $V^\pm$을 주어진 대로 적을 수 있다.
</details>

## 복소함수의 미분

미분 가능한 복소함수 $f:U\subset \mathbb{C}\rightarrow \mathbb{C}$를 생각하자. 우선 복소평면의 성질을 제거하고, 각 2차원 접평면상에서 $\partial_x,\partial_y$, $\partial_r,\partial_s$ 좌표계를 잡는다. 이후 2계변수 실함수로써 미분을 취하면 다음 야코비안을 얻는다.

$$
J_{\mathbb{R}}(f)=\begin{bmatrix}
\partial_x (r\circ f) & \partial_y (r\circ f)\\
\partial_x (s\circ f) & \partial_y (s\circ f)
\end{bmatrix}
$$

이제 $\partial_x,\partial_y$를 기저로 가지는 접평면을 복소화하면 $\partial_x\otimes 1$, $\partial_y\otimes 1$을 기저로 가지는 복소 벡터 공간을 얻는다. 이 복소 벡터 공간의 또 다른 기저를 다음과 같이 정의하자.

$$
\partial_z\equiv \frac{1}{2}\left(\partial_x -i\partial_y \right),\quad \partial_{\overline{z}}\equiv \frac{1}{2}\left(\partial_x+i\partial_y\right)
$$

혹은,

$$
\frac{1}{2}\begin{bmatrix}
1 & -i\\
1 & i
\end{bmatrix}
$$

마찬가지로, $\partial_w$와 $\partial_{\overline{w}}$를 $\partial_r$과 $\partial_s$를 이용해 정의한다. 그러면 위의 야코비안은 다음이 된다.

$$
\frac{1}{2}
\begin{bmatrix}
1 & 1\\ i & -i
\end{bmatrix}\begin{bmatrix}
\partial_x (r\circ f) & \partial_y (r\circ f)\\
\partial_x (s\circ f) & \partial_y (s\circ f)
\end{bmatrix}\begin{bmatrix}
1 & -i\\
1 & i
\end{bmatrix}=\begin{bmatrix}\partial_z (w\circ f) & \partial_{\overline{z}}(w\circ f)\\
\partial_z(\overline{w}\circ f) & \partial_{\overline{z}}(\overline{w}\circ f)
\end{bmatrix}
$$

$w\circ f$를 $f$라 쓰고, $\overline{w}\circ f$를 $\overline{f}$라 하면, $f$의 미분을 다음과 같이 쓸 수 있다.

$$
df=\begin{bmatrix}
\partial_z f & \partial_{\overline{z}} f\\
\partial_z \overline{f}& \partial_{\overline{z}} \overline{f}
\end{bmatrix}
$$

따라서, 복소함수 $f$가 $z$에서 정칙 함수<sup>holomorphic function</sup>임과 $df(z)$가 대각 행렬임이 동치이다. 거꾸로, 복소함수 $f$가 $z$에서 반정칙 함수<sup>antiholomorphic function</sup>임과 $df(z)$가 반대각 행렬임이 동치이다. 즉, $f=u+iv$가 정칙 함수임과

$$
(\partial_x+i\partial_y) u+(i\partial_x-\partial_y) v=0 \quad \Rightarrow \quad \partial_x u-\partial_y v = \partial_y u+\partial_x v=0
$$

임은 동치이다. 우측의 식을 **코시-리만 방정식<sup>Cauchy-Riemann equations</sup>**이라고도 한다.