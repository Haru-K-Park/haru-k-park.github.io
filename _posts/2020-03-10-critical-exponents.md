---
layout: post
title: "임계 지수"
author: "YGLENA"
comments: true
---
# 정의
**임계 지수<sup>critical exponent</sup>**란 물리적인 값들이 이차 상전이<sup>second order phase transition</sup>의 임계점<sup>critical point</sup> 근방에서 보이는 추세를 나타내는 값이다.

임계 온도<sup>critical temperature</sup> $T_c$를 가지는 계에서 환산온도<sup>reduced temperature</sup>를 다음과 같이 쓰자.

$$
\tau\colon = \frac{T-T_c}{T_c}
$$

이 때 환산온도에 의존하는 물리량 $f(\tau)$의 임계 지수 $k$는 다음과 같이 정의된다.

$$
k\colon = \lim_{\tau\rightarrow 0}\frac{\log |f(\tau)|}{\log|\tau|}
$$

곧, $\tau=0$, 즉 $T=T_c$ 근방에서 $f\sim \tau^k$로 표현된다.

임계 온도 이전과 이후에서, 즉 $\tau>0$과 $\tau<0$에서의 임계 지수가 다를 수 있다. 이 경우 임계 지수는 $\tau\rightarrow 0^{\pm}$으로 향하는 극한으로 정의된다.

임계 지수는 반드시 온도에 관련하여 정의되는 것은 아니고, 임계 온도 $T=T_c$ 상에서 물리량의 추세를 나타내는 임계 지수 또한 존재한다.

## 주로 사용되는 임계 지수
일반적으로 다음과 같은 임계 지수가 주로 정의된다.

$$
\begin{align*}
C & \sim |T-T_c|^{-\alpha}\\
|M| & \sim |T-T_c|^\beta\\
\chi & \sim |T-T_c|^{-\gamma}\\
|M| & \sim |B|^{1/\delta}\\
G(x) & \sim |x|^{2-D-\eta}\\
\xi & \sim |T-T_c|^{-\nu}\\
\end{align*}
$$

여기서 $C$는 열용량<sup>heat capacity</sup>, $M$은 자화량<sup>magnetization</sup>, $\chi$는 감수율<sup>susceptibility</sup>, $G(x)$는 상관 함수<sup>correlation function</sup>이다. $D$는 계의 차원이다.

재규격화 이론<sup>renormalization theory</sup>을 통해 임계 지수들 사이에 다음과 같은 관계가 성립함을 알 수 있다.

$$
\begin{align*}
\alpha &= 2-\nu D\\
\beta & =\frac{\nu}{2}(D-2+\eta)\\
\gamma & =\nu(2-\eta)\\
\delta & =\frac{D+2-\eta}{D-e+\eta}
\end{align*}
$$

즉, 모든 임계 지수는 두 개의 임계 지수 $\eta,\nu$와 차원 $D$로부터 유도할 수 있다.
