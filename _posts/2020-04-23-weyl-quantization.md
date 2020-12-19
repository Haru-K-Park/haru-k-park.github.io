---
layout: post
title: "바일 양자화"
author: "YGLENA"
comments: true
---
* 
{:toc}
## 양자화
양자화란 고전역학적 성질을 따르는 계를 양자역학의 이론으로 옮겨오는 과정을 말한다. 따라서, 고전 역학의 위상 공간<sup>phase space</sup>에서의 함수 $f$를 양자 역학의 힐베르트 공간<sup>Hilbert space</sup>에서의 자기수반 연산자<sup>self-adjoint operator</sup>로 바꾸는 과정을 양자화라 할 수 있다.

### 연산자 순서의 문제
함수 $f(x,p)=xp$를 생각하자. 함수 $x$를 연산자 $X$로 바꾸고 $p$를 $P$로 바꾸었다면, 자연스럽게 $xp$는 $XP$로 바꾸고자 할 것이다. 그러나 $f(x,p)=px$로 쓴다면 우리는 $PX$를 얻고, $[ X,P ]\neq 0$이므로 두 결과는 다르다. 보다 일반적으로 다음과 같은 함수를 생각해 보자.

$$
Q(x^j p^k)= X^j P^k
$$

이 함수의 결과는 자기수반 연산자가 아니기 때문에, 적절한 양자화로 볼 수 없다. 대신, 존재 가능한 모든 $X,P$의 순열들의 합으로 표현한다면 이는 자기수반 연산자를 줄 것이다.

## 다항함수에서의 바일 양자화

다음과 같이 정의된 $\mathbb{R}^2$ 위에서의 다항함수에서 $C_c^{\infty}(\mathbb{R})$ 위의 연산자로 향하는 선형함수를 생각하자.

$$
Q(x^j p^k) = \frac{1}{(j+k)!}\sum_{\sigma\in S_{j+k}}\sigma(X,\cdots,X,P,\cdots,P)
$$

이러한 형태의 양자화를 다항함수에서의 **바일 양자화<sup>Weyl quantization</sup>**라 한다. 예를 들어,

$$
Q(xp^2)=\frac{1}{3}(XP^2+PXP+P^2X)
$$

### 성질

>$\mathbb{R}^2$ 위에서의 다항함수에서 $C_c^{\infty}(\mathbb{R})$ 위의 연산자로 향하는 선형함수 $Q$에 대하여, $Q$가 다항식에서의 바일 양자화임과 모든 $a,b\in \mathbb{C}$ 및 $j\in \mathbb{Z}_{\geq 0}$에 대하여 다음 성질을 만족함이 동치이다.
>
>$$
Q((ax+bp)^j)=(aX+bP)^j
>$$

>다항식에서의 바일 양자화에 있어, 다항함수 $f$에 대하여 다음이 성립한다.
>
>$$
\begin{align}
Q(xf)&=Q(x)Q(f)-\frac{i\hbar}{2}Q\left(\frac{\partial f}{\partial p}\right) \\\
&=Q(f)Q(x)+\frac{i\hbar}{2}Q\left(\frac{\partial f}{\partial p}\right)
\end{align}
>$$
>
>$$
\begin{align}
Q(pf)&=Q(p)Q(f)+\frac{i\hbar}{2}Q\left(\frac{\partial f}{\partial x}\right) \\\
&=Q(f)Q(p)-\frac{i\hbar}{2}Q\left(\frac{\partial f}{\partial x}\right)
\end{align}
>$$

## 바일 양자화

$f\in L^2(\mathbb{R}^{2n})$에 대하여, $\kappa_f:\mathbb{R}^{2n}\rightarrow \mathbb{C}$를 다음과 같이 정의한다.

$$
\kappa_f(x,y)=(2\pi\hbar)^{-n}\int_{\mathbb{R}^n} f\left(\frac{x+y}{2},p\right)e^{-i(y-x)\cdot p/\hbar}dp
$$

그러면 $f$의 **바일 양자화**는 다음과 같이 정의된다.

$$
\newcommand{\coloneqqb}{\mathrel{\mathop:}\mathrel{\mkern-1.2mu}=}
\require{mathtools}
Q(f)(\psi)(x)\coloneqqb \int_{\mathbb{R}^n}\kappa(x,y)\psi(y) dy
$$