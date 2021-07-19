---
layout: post
title: "스튀름-리우빌 이론"
author: "YGLENA"
comments: true
tags: [Calculus]
redirect_from: /sturm-liouville-theory
---
<details><summary>
<span style="font-size:2em;font-family: Helvetica;">**목차**</span>
</summary>
* 목차
{:toc}
</details>

## 정의

**스튀름-리우빌 방정식<sup>Sturm-Liouville equation</sup>**이란 구간 $[a, b]$ 위에서의 다음과 같은 형태의 2계 미분 방정식을 말한다.

$$
\frac{d}{dx} \left[p(x) \frac{dy}{dx}\right] + q(x)y=-\lambda w(x)y
$$

스튀름-리우빌 방정식이 다음 조건을 만족시킨다 하자.

1. $p(x),w(x)>0$이다.
2. $p(x), dp(x)/dx, q(x), w(x)$가 모두 $[a, b]$ 위에서 연속함수이다.
3. $\alpha_1 y(a)+\alpha_2 y'(a)=0$이다. 이 때, $\alpha_1^2+\alpha_2^2>0$이다.
4. $\beta_1 y(b)+\beta_2 y'(b)=0$이다. 이 때, $\beta_1^2+\beta_2^2>0$이다.

그러면 우리는 이를 **정규 스튀름-리우빌 방정식<sup>regular Sturm-Liouville equation</sup>**이라 한다.

## 스튀름-리우빌 정리

> **스튀름-리우빌 정리.** 정규 스튀름-리우빌 방정식에 대하여, 다음이 성립한다.
> 1. 정규 스튀름-리우빌 방정식을 만족시키는 고유값들 $\lambda_0,\cdots,\lambda_n,\cdots$는 모두 실수이며, $\lambda_0<\lambda_1<\cdots < \lambda_n < \cdots \rightarrow \infty$와 같이 번호매겨질 수 있다.
> 2. 각각의 고유값 $\lambda_n$에 대하여, 상수 배 하에서 유일한 고유 함수 $y_n(x)$이 존재하고, 이것이 구간 $(a,b)$ 사이에서 $n$개의 영점을 가진다.
> 3. 정규화<sup>normalized</sup>된 고유 함수들은 $w$-가중 내적 위에서 정규 직교 기저<sup>orthonormal basis</sup>를 이룬다. 즉, 다음이 성립한다.
>
> $$
> \int_a^b y_n(x) y_m(x) w(x) dx = \delta_{mn}
> $$

### 프뤼퍼 대체

정규 스튀름-리우빌 방정식은 다음 형태로 고쳐 쓸 수 있다.

$$
\frac{d}{dx}\left[P(x) \frac{dy}{dx}\right] + Q(x) y = 0
$$

여기서, $P(x)=p(x)$이고 $Q(x)=q(x)+\lambda w(x)$이다. 이제 다음 변수 $r,\theta$를 정의하자.

$$
r^2=y^2+P^2y'^2,\quad \tan\theta=\frac{y}{Py'}
$$

이는 곧 다음과 같다.

$$
Py'=r\cos \theta,\quad y=r\sin\theta
$$

$\cot\theta = Py'/y$이므로, 양변을 미분하면 다음을 얻는다.

$$
- \theta'\csc^2\theta = \frac{(Py')'}{y}-\frac{Py'^2}{y^2}=-Q-\frac{\cot^2 \theta}{P}
$$

양변에 $-\sin^2\theta$를 곱하면 다음을 얻는다.

$$
\theta'=Q\sin^2\theta+\frac{\cos^2\theta}{P}=\left[q+\lambda w\right]\sin^2(\theta)+\frac{\cos^2\theta}{p}
$$

또한, $r^2=(Py')^2+y^2$를 미분하면 다음을 얻는다.

$$
r'=\frac{1}{2}\left[ \frac{1}{P}-Q\right] r\sin 2\theta = \frac{1}{2}\left[ \frac{1}{p}-q-\lambda w\right]r\sin 2\theta
$$

이 두 식은 **프뤼퍼 방정식<sup>Prüfer system</sup>**이라 불리며, 정규 스튀름-리우빌 방정식과 동치이다.

스튀름-리우빌 방정식에서 $y$의 근은 곧 프뤼퍼 방정식에서 $\sin \theta=0$임을 의미하므로, $n\in \mathbb{Z}$에 대해 $\theta=n\pi$임과 대응됨을 기억하라.

초기조건이 $\theta(a)=\gamma$라 했을 때, $\gamma$는 다음 식에 의해 결정된다.

$$
\tan\gamma=\frac{y(a)}{p(a)y'(a)}=-\frac{\alpha_2}{p(a)\alpha_1},\quad 0\leq \gamma<\pi, \alpha_1\neq 0
$$

$\alpha_1=0$이라면 $\gamma=\pi/2$로 둘 수 있다.

### 비교 정리

> 범위 $[a, b]$ 사이에서, $f$가 미분방정식 $y'=F(x,y)$의 해이고, $g$가 미분방정식 $z'=G(x,z)$의 해라 하자. 또한 초기조건이 $f(a)=g(a)$로 서로 같다고 하자. $F(x,y)$ 또는 $G(x,z)$가 **립시츠 조건<sup>Lipschitz condition</sup>**을 만족시킨다 하자. 즉,
>
>$$
>|F(x,y_1)-F(x,y_2)|\leq L|y_1-y_2| \lor |G(x,z_1)-G(x,z_2)|\leq L|z_1-z_2|
>$$
>
>를 만족시키는 $L>0$이 있다고 생각하자. 또한 주어진 영역의 $x,y$에 대하여 항상 $F(x,y)\leq G(x,y)$라 하자. 그렇다면 다음이 항상 참이다.
>
>$$
>f(x)\leq g(x),\forall x>a
>$$

비교 정리로부터 다음 따름정리를 얻을 수 있다.

> 비교 정리의 조건 하에서, 모든 $x_1>a$에 대해 $f(x_1)< g(x_1)$이거나, $[a, b]$ 위에서 $f(x)\equiv g(x)$이다.

### 스튀름 비교 정리
> 고정된 $x_n>a$에 대하여 $\theta(x_n,\lambda)=n\pi$라 하자. 그러면 모든 $x>x_n$에 대하여 $\theta(x,\lambda)>n\pi$이다.

<details><summary>**증명.**
</summary>

원 식에서 다음을 얻는다.

$$
\left.\frac{d\theta(x,\lambda)}{dx}\right\rvert_{x_n}=\frac{1}{p(x_n)}>0
$$

따라서 $x>x_n$에서 $\theta(x,\lambda)$의 값은 $\theta(x_n,\lambda)$보다 항상 크다. $\square$

</details>

따라서 $y(x)$의 $n$번째 해는 $\theta=n\pi$로 주어진다.

> **스튀름 비교 정리.** 다음 두 미분방정식을 생각하자.
>
> $$
>\begin{align*}
> \frac{d}{dx}\left(P(x)\frac{dy}{dx}\right)+Q(x)y&=0\\
> \frac{d}{dx}\left(P_1(x)\frac{dy}{dx}\right)+Q_1(x)y&=0
>\end{align*}
> $$
>
> $P(x)\geq P_1(x)>0$이고 $Q_1(x)\geq Q(x)$라면, 첫번째 식의 비자명한 해의 두 영점 사이에, 모든 두번째 식의 해에 대하여 적어도 하나의 영점이 존재한다.

<details><summary>**증명.**
</summary>

첫 번째 스튀름-리우빌 방정식의 해가 $y$이고 두 번째의 해가 $y_1$이라 하자. 각 스튀름-리우빌 방정식에 대응하는 다음 프뤼퍼 방정식을 생각하자.

$$
\begin{align*}
\theta'&=Q\sin^2\theta+\frac{1}{P}\cos^2\theta\\
\theta'&=Q_1\sin^2\theta+\frac{1}{P_1}\cos^2\theta
\end{align*}
$$

첫 번째 식의 해가 $\theta$이고 두 번째 식의 해가 $\theta_1$이라 하자. $y(x)=0$인 $x$를 찾는 것은 $\sin\theta(x)=0$인 것을 찾는 것과 같고, 따라서 $\theta(x)=n\pi$임과 같다. 마찬가지로 $y_1(x)=0$인 $x$를 찾는 것은 $\theta(x)=m\pi$임과 같다.

$\theta(a)=\gamma, \theta_1(a)=\gamma_1$이라 했을 때 $0\leq \gamma\leq \gamma_1<\pi$이므로, $y$의 $n$번째 영점은 $\theta(x)=n\pi$에서 나타난다. 비교 정리에 의하여 $\theta(x)\leq \theta_1(x)$이므로, $\theta(x_1)=n\pi$이고 $\theta(x_2)=(n+1)\pi$일 때, $\theta(x)>\theta_1(x)$이라면, $x_1< x_3< x_2$가 존재하여 $\theta_1(x_3)=(n+1)\pi$를 만족시킨다. 만약 어떤 $x\in [a, b]$에 대하여 $\theta(x)=\theta_1(z)$라면 비교 정리의 따름정리에 의하여 $x\in [a, z]$에서 $\theta(x)=\theta_1(x)$이므로, $y$와 $y_1$은 같은 영점을 가진다. $\square$
</details>

> 고정된 $x>a$에 대하여, $\theta(x,\lambda)$가 주어진 $\lambda$ 하에서의 위치 $x$에서의 함수값이라 하자. 그렇다면 $\theta(x,\lambda)$는 $\lambda$에 대하여 강한 단조 증가 함수<sup>strictly increasing function</sup>이다.

<details><summary>**증명.**
</summary>

이는 스튀름 비교 정리와 비교 정리의 따름정리에 의해서 자명하다. $\square$

</details>

> 주어진 양의 정수 $n$에 대하여, $x_n(\lambda)$가 $\theta(x,\lambda)=n\pi$를 만족시키는 최소의 $x$라 하자. 이 함수는 충분히 큰 $\lambda$에 대하여 잘 정의되며 연속이다. 또한 이는 $\lambda$에 대하여 강한 단조 감소 함수이며, $\lim_{\lambda\rightarrow \infty} x_n(\lambda)=a$이다.

<details><summary>**증명.**
</summary>

연속이고 강한 단조 감소 함수임은 $\theta(x,\lambda)$가 $\lambda$에 대해 연속이고 강한 단조 증가 함수임과 동치이다. $\lambda$가 충분히 크다고 가정하자. $q_m$과 $w_m$을 각각 $q$와 $w$의 최대 하한으로, $p_M$을 $p$의 최소 상한으로 잡자. 이제 다음 미분방정식을 생각한다.

$$
p_M y''+(\lambda w_m+q_m)y=0
$$

$\lambda$가 충분히 크다고 가정했으므로 우리는 $\lambda>-q_m/w_m$이라 생각할 수 있다. 따라서 위의 미분방정식은 다음 해를 가진다.

$$
y_1(x)=\sin(kx),\quad k=\sqrt{\frac{\lambda w_m+q_m}{p_M}}
$$

또한, 이 함수의 영점은 $\sqrt{p_M/(\lambda w_m+q_m)}\pi$만큼 서로 떨어져 있다. 스튀름 비교 정리에 의하여, 원래 식의 해가 $y(x)$라 하면, $y\leq y_1$이다. 또한 $y_1(x)$의 두 영점 사이에서, 반드시 적어도 하나의 영점을 가져야만 한다. $\lambda$가 충분히 크다면 $y_1(x)$는 $(a,b)$에서 $n$개의 영점을 가지므로, $u(x)$ 또한 적으도 $n$개의 영점을 가진다. 따라서 $\theta(x,\lambda)$는 잘 정의된다.

$x_n(\lambda)$가 $y_1(x)$의 연속한 두 영점 사이에 위치하고, $\lambda\rightarrow \infty$로 갈수록 이 영점들은 $a$로 향하므로, $\lim_{\lambda\rightarrow \infty} x_n(\lambda)=0$이다. $\square$

</details>

### 진동 정리

> **진동 정리.** 프뤼퍼 방정식의 해 $\theta(x,\lambda)$가 모든 $\lambda$에 대하여 초기조건 $\theta(a,\lambda)=\gamma<\pi$을 만족할 때, 이 해는 연속이며 고정된 $x\in (a,b]$에서 $\lambda$에 대하여 강한 단조 증가 함수이다. 또한 다음이 성립한다.
>
>$$
>\lim_{\lambda\rightarrow \infty} \theta(x,\lambda)=\infty,\quad \lim_{\lambda\rightarrow -\infty}\theta(x,\lambda)=0.
>$$

<details><summary>**증명.**
</summary>

첫 번째 문장과 첫 번째 극한식은 위에서 증명하였다. 두 번째 식의 경우, $\gamma<\gamma_1<\pi$와 $\epsilon>0$을 만족하는 $\gamma_1,\epsilon$을 고르자. $(a,\gamma_1)$과 $(x_1,\epsilon)$ 사이를 잇는 선 위의 어떤 점 $(x,\theta)$에 대하여, $\theta(x,\lambda)$의 기울기

$$
\frac{d\theta}{dx}=\left[q+\lambda w\right]\sin^2\theta + \frac{1}{p}\cos^2\theta
$$

는 $\lambda$가 충분히 작은 음수일 때, 선의 기울기 $(\epsilon-\gamma_1)/(x_1-a)$보다 작도록 할 수 있다. 따라서 $\theta(x,\lambda)$는 항상 선보다 아래 존재하고, 따라서 충분히 작은 음수 $\lambda$에 대하여 $\theta(x,\lambda)<\epsilon$이며, $\theta(x_1,\lambda)>0$이므로 주어진 극한식이 성립한다. $\square$

</details>

<details><summary>**스튀름-리우빌 정리 1.과 2.의 증명.**
</summary>

스튀름-리우빌 정리의 경계조건을 프뤼퍼 경계조건에서는 다음과 같이 쓸 수 있다.

$$
\theta(a,\lambda)=\gamma, \quad \theta(b,\lambda)=\delta+n\pi,\quad n\in\mathbb{N}_{\geq 0}
$$

이 때, $0\leq \gamma < \pi$는 $p(a)\tan(\gamma)=-\alpha_2/\alpha_1$을 만족시키는 가장 작은 $\gamma$이고, $0<\delta\leq \pi$는 $p(b)\tan(\delta)=-\beta_2/\beta_1$을 만족시키는 가장 작은 $\delta$이다. $\alpha_1=0$이면 $\gamma=\pi/2$로 두고, $\beta_1=0$이면 $\delta=\pi/2$로 둔다.

프뤼퍼 방정식을 만족시키는 $\theta(x,\lambda)$의 초기조건이 $\theta(a,\lambda)=\gamma$라 하자. $\theta(b,\lambda)$가 $\lambda$에 대하여 강한 단조 증가 함수이고 $\theta(b,\lambda)>0$이므로, $\lambda$는 $-\infty$에서 서서히 증가하여 $\theta(b,\lambda_0)=\delta$를 만족시키는 $\lambda_0$를 얻는다. 이를 반복하여 $\theta(b,\lambda_n)=\delta+n\pi$를 만족시키는 $\lambda_n$의 순열을 찾을 수 있고, 이는 $n\rightarrow \infty$에서 무한으로 발산한다. 또한 고정된 $\lambda_n$에 대하여, 스튀름-리우빌 방정식의 해 $y(x)=r(x)\sin\theta(x,\lambda_n)$은 $n$개의 해를 가진다. $\square$

</details>

### 정규 직교 기저

> **베셀 부등식<sup>Bessel's inequality</sup>.** 내적 공간 $(V,\langle-,-\rangle)$의 가산 정규 직교 집합 $B\subset V$를 생각하자. 임의의 벡터 $v\in V$에 대하여 다음이 참이다.
>
>$$
>\sum_{e\in B}|\langle v,e\rangle|^2\leq \lVert v\rVert^2
>$$

<details><summary>**증명.**
</summary>

임의의 유한 집합 $B'\subset B$에 대하여 다음이 성립한다.

$$
\begin{align*}
0&\leq \lVert v-\sum_{e\in B'}\langle v,e\rangle e\rVert^2\\
&= \lVert v\rVert^2 + \left\lVert \sum_{e\in B'} \langle v,e\rangle e\right\rVert^2 - 2\mathfrak{R}\left(\left\langle v,\sum_{e\in B'}\langle v,e\rangle e\right\rangle\right)\\
&= \lVert v\rVert^2 -\sum_{e\in B'}|\langle v,e\rangle|^2
\end{align*}
$$

이제 집합열 $B_0\subset B_1\subset \cdots\subset B_n\subset \cdots\subset B$를 생각한다. 이 때 $B_i$는 유한 집합이고, $B=\bigcup_i B_i$이다. 위의 부등식이 모든 $B_i$에 대해 성립하므로 $B$에 대하여 성립한다. $\square$

</details>

> **파세발 항등식<sup>Parseval's equality</sup>.** 힐베르트 공간 상에서 가산 정규 직교 집합 $B\subset V$가 정규 직교 기저임과 베셀 부등식의 등식이 성립함은 동치이다.

<details><summary>**증명.**
</summary>

정규 직교 기저의 정의에 의해 자명하다. $\square$

</details>

> 힐베르트 공간의 가산 정규 직교 집합 $\{\phi_n\}$이 정규 직교 기저임과, 모든 $i$에 대해 $\langle v,\phi_i\rangle=0$인 $0\neq v\in V$가 존재하지 않음은 동치이다.

<details><summary>**증명.**
</summary>

다음을 정의하자.

$$
v_n=\sum_{i=1}^n \langle v,\phi_i\rangle \phi_i
$$

$j>k$일 때 다음을 얻는다.

$$
\lVert v_j-v_k\rVert^2 = \sum_{i=k+1}^j \langle v,\phi_i\rangle^2\leq \sum_{i=k+1}^\infty \langle v,\phi_i\rangle^2
$$

$\sum_{i=1}^k \langle v,\phi_k\rangle^2$는 베셀 부등식에 의해 수렴하므로, 위의 우변은 $k\rightarrow \infty$에 대하여 $0$으로 수렴한다. 따라서 $v_n$은 코시 순열이고, 따라서 수렴하는 $w\in V$를 얻는다. $h=v-w$라 두자. 모든 $i\geq k$에 대하여 $\langle v-v_i,\phi_k\rangle=0$이므로, $i\rightarrow \infty$를 취하면 모든 $k$에 대하여 $\langle h,\phi_k\rangle=0$임을 얻는다. 파세발 항등식에 의하여 $h=0$임과 $\{\phi_n\}$이 정규 직교 기저임이 동치이다. $\square$

</details>

> 힐베르트 공간의 가산 정규 직교 기저 $\{\phi_i\}$와 가산 정규 직교 집합 $\{\psi_i\}$이 다음을 만족시킨다고 하자.
>
>$$
> \sum_{i=1}^\infty \lVert \psi_i-\phi_i\rVert^2<1
>$$
>
> 그러면 $\{\psi_i\}$ 또한 가산 정규 직교 기저이다.

<details><summary>**증명.**
</summary>

$\{\psi_i\}$가 기저가 아니라고 가정하자. 그러면 우리는 벡터 모든 $\psi_i$에 대하여 $\langle v,\psi_i\rangle=0$인 $0\neq v\in V$를 얻는다. 이제 다음이 성립한다.

$$
\langle v, \phi_i\rangle = \langle v,\phi_i-\psi_i\rangle
$$

양변을 제곱하고 코시-슈바르츠 부등식을 사용하면 다음을 얻는다.

$$
\langle v,\phi_i\rangle^2 \leq \lVert v\rVert^2 \lVert \phi_i-\psi_i\rVert^2
$$

이를 모든 $i$에 대해 더하면 다음을 얻는다.

$$
\sum_{i=1}^\infty \langle v,\phi_i\rangle^2\leq \lVert v\rVert^2
$$

그러나 이것은 파세발 항등식에 위배된다. $\square$

</details>

> 위의 조건을 어떤 정수 $N$에 대해 다음과 같이 약화시키자.
>
> $$
> \sum_{i=N+1}^\infty \lVert \psi_k-\phi_k\rVert^2<1
> $$
>
> 그러면 집합 $\{\phi_1,\cdots,\phi_N,\psi_{N+1},\cdots\}$의 모든 원소와 직교하는 벡터 $v\in V$는 $0$뿐이다.

<details><summary>**증명.**
</summary>

위의 증명에서, 그러한 벡터 $v$는 $i>N$에 대하여 다음 부등식을 만족함을 알 수 있다.

$$
\langle v,\phi_i\rangle^2 \leq \lVert v\rVert^2 \lVert \phi_i-\psi_i\rVert^2
$$

따라서,

$$
\lVert v\rVert^2=\sum_{i=1}^\infty \langle v,\phi_i\rangle^2 = \sum_{i=N+1}^\infty \langle v,\phi_i\rangle^2 \leq \lVert h\rVert^2 \sum_{i=N+1}^\infty \lVert\phi_i-\psi_i\rVert^2<\lVert v\rVert^2
$$

이나, 이는 파세발 항등식에 위배된다. $\square$

</details>

> 위의 조건을 만족시키는 $\{\phi_i\}$와 $\{\psi_i\}$에 대하여, 다음을 정의하자.
>
>$$
> \eta_i=\phi_i-\sum_{k=n+1}^\infty \langle \phi_i \psi_k\rangle \psi_k
>$$
>
> 그러면 $\{\eta_1,\cdots,\eta_N,\psi_{N+1},\cdots\}$의 모든 원소와 직교하는 벡터 $v\in V$는 $0$뿐이다.

<details><summary>**증명.**
</summary>

그러한 $v$에 대해 다음이 성립한다.

$$
\langle v,\phi_i\rangle = \langle v,\eta_i\rangle+\sum_{k=N+1}^\infty \langle \phi_i,\psi_k \rangle\langle v,\psi_k\rangle = 0
$$

따라서 이는 위의 조건과 같아진다. $\square$

</details>

> 힐베르트 공간 $V$의 가산 정규 직교 기저 $\{\phi_i\}$와 가산 정규 직교 집합 $\{\psi_i\}$이 다음을 만족한다고 하자.
>
>$$
>\sum_{i=1}^\infty \lVert \psi_i-\phi_i\rVert^2<\infty
>$$
>
> 그러면 $\{\psi_i\}$는 가산 정규 직교 기저이다.

<details><summary>**증명.**
</summary>

다음을 만족하는 정수 $N$을 항상 잡을 수 있다.

$$
\sum_{i=N+1}^\infty \lVert \psi_i-\phi_i\rVert^2 < 1
$$

따라서 $\psi_{N+1},\psi_{N+2},\cdots$와 위에서 정의한 $\eta_{1},\cdots,\eta_{N}$ 모두와 직교하는 벡터는 $0$뿐이다. $S$가 $\psi_{N+1},\psi_{N+2},\cdots$와 모두 직교하는 벡터들의 집합이라 하자. $\eta_i$의 정의에 의해 모든 $i$에서 $\eta_i\in S$이다. 따라서 $S$는 최대 $N$차원의 유한차원 벡터 공간이다.

또한, $\psi_{1},\cdots,\psi_{N}\in S$이다. 따라서 $\psi_1,\cdots,\psi_N$의 선형결합이 $\eta_1,\cdots,\eta_N$을 주고, 이는 곧 $\{\eta_1,\cdots,\eta_N,\psi_{N+1},\cdots\}$의 원소와 모두 직교인 벡터는 $\{\psi_i\}$의 원소와 모두 직교임을 말한다. 그러한 벡터는 $0$뿐이므로, $\{\psi_i\}$는 정규 직교 기저이다. $\square$

</details>

<details><summary>**스튀름-리우빌 정리 3.의 증명.**
</summary>

$y_n$이 정규화된 스튀름-리우빌 방정식의 $n$번째 정규화된 고유 함수라 하자. 다음을 정의한다.

$$
\phi_n(x)=\sqrt{\frac{2}{b-a}}\cos \left[ \frac{n\pi(x-a)}{b-a}\right]
$$

$n$이 커질수록 $\lambda_n$은 무한히 커지고, 따라서 스튀름-리우빌 방정식은 다음과 같이 변형된다.

$$
u''+\lambda_n u=0
$$
이를 풀고, $y_n$의 해가 $n$개 분포함을 고려하면, 다음을 얻는다.

$$
|y_n-\phi_n|\sim \mathcal{O}\left(\frac{1}{n}\right)
$$

따라서,

$$
\lVert y_n-\phi_n\rVert^2 \sim \mathcal{O}\left(\frac{1}{n^2}\right)
$$

[바젤 문제](/basel-problem)에 따르면 $\sum_n 1/n^2$는 수렴하고, 따라서

$$
\sum_{i=1}^\infty \lVert y_n-\phi_n\rVert^2<\infty
$$

를 얻는다. 코사인 함수가 정규 직교 기저이므로, $y_n$ 또한 정규 직교 기저이다. $\square$

</details>