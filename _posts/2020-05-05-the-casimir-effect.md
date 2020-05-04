---
layout: post
title: "카시미르 효과"
author: "YGLENA"
comments: true
tags: [Quantum field theory]
---
* 
{:toc}
## 개요
1차원 상에서의 자유 스칼라 장<sup>free scalar field</sup>의 해밀토니안은 다음과 같이 쓸 수 있다.

$$
H=\int \frac{dk}{2\pi}\omega_k \left( a_k^\dagger a_k+\frac{1}{2}\right)
$$

즉 진공 상태 $ \| 0 \rangle $의 에너지는 $\int \frac{dk}{2\pi}\frac{\omega_k}{2}$이다. $\omega_k=\lvert k\rvert$이므로 이 값은 무한으로 발산한다.

계의 크기를 $a$로 제한하면 $k$가 가질 수 있는 값 또한 정수 $n\in \mathbb{Z}$에 대하여 $\frac{n\pi}{a}$이므로, 진공 상태의 에너지는 다음과 같다.

$$
E(a)=\frac{\pi}{2a}\sum_{n\in \mathbb{N}} n
$$

이는 마찬가지로 발산한다. 그러나 우리가 계산한 것은 다른 에너지에 대한 상대적 에너지이므로 측정할 수 없는 값이다. 측정할 수 있는 값을 얻어내기 위하여, 계가 크기 $L\gg a$인 계 안에 갇혀 있다고 생각하자. 그러면 총 에너지는 다음과 같다.

$$
E_{\textrm{tot}}(a)=\left(\frac{1}{a}+\frac{1}{L-a}\right)\frac{\pi}{2}\sum_{n\in \mathbb{N}} n
$$

$a$의 미소 변화에 따른 전체 에너지의 변화는 작은 계에 가해지는 힘과 관련이 있다. 이를 이용하면,

$$
F(a)=-\frac{dE_{\textrm{tot}}}{da}=\left(\frac{1}{a^2}-\frac{1}{(L-a)^2)}\right)\frac{\pi}{2}\sum_{n\in \mathbb{N}}n
$$

$L$이 무한대로 가면 $F(a)$ 또한 무한대로 간다. 즉, 작은 계는 무한대의 힘을 받으며 넓어지려 하고, 이는 실험 결과에 전혀 들어맞지 않는다.

## 에너지 조정
실제 물리적 계에서, 두 계를 분리하는 장벽이 버텨낼 수 있는 에너지에는 한계가 존재한다. 장벽은 그 장벽을 이루는 분자 구조의 크기 단위보다 짧은 파장을 가지는 고에너지 파동은 차폐할 수 없고, 따라서 우리의 계산에서 이와 같은 파동은 약간의 영향만을 미쳐야 한다.

이러한 "에너지의 조정"은 장벽의 구조 등으로 인하여 다양한 함수로 표현될 수 있다. 즉, 계의 에너지를 구할 때 각 주파수마다 가중치 $f$를 주어, 전체 에너지를 다음과 같이 표현할 수 있다.

$$
E(a)=\frac{\pi}{2a}\sum_{n\in \mathbb{N}}nf\left(\frac{n}{a\Lambda}\right)
$$

이 때 $\Lambda$는 거리의 역수 단위를 가진 상수이다. 우리는 $f(x)$가 높은 $x$에 대해서는 빠른 속도로 $0$으로 감소하기를, 그리고 낮은 $x$에 대해서는 $1$에 충분히 가깝기를 기대한다. 따라서 다음 조건들을 가정한다.

$$
\lim_{x\rightarrow \infty} x f^{(j)}(x)=0,\quad f(0)=1
$$

이제 계에서 $L-a$ 부분의 에너지는 다음과 같이 쓸 수 있다.

$$
E(L-a)=\frac{\pi}{2(L-a)}\sum_{n\in \mathbb{N}}n f\left(\frac{n}{(L-a)\Lambda}\right)
$$

$L$이 충분히 커지면 $x=\frac{n}{(L-a)\Lambda}$로 두고 합연산을 적분으로 바꾸어 다음과 같이 생각할 수 있다.

$$
E(L-a)=\frac{\pi}{2}(L-a)\Lambda^2\int x f(x)dx 
$$

$L$ 관련 항은 $a$와 관련 없으므로 무시한다. 이제 다시 $x$를 $\frac{n}{a\Lambda}$로 바꾸면 전체 에너지는 다음과 같다.

$$
E_{\textrm{tot}}=\frac{\pi}{2a}\sum_{n\in \mathbb{N}}nf\left(\frac{n}{a\Lambda}\right)-\frac{\pi}{2a}\int  n f\left(\frac{n}{a\Lambda}\right) dn
$$

[오일러-매클로린 식<sup>Euler-Maclaurin formula</sup>](https://yglena.github.io/2020-05-03/euler-maclaurin-forumla)을 $F(n)=nf\left(\frac{n}{a\Lambda}\right)$에 대하여 이용하면 다음을 안다.

$$
\sum_{n\in \mathbb{N}}F(n)-\int_0^\infty F(n)=-\sum_{i=1}^{\infty} \frac{(-1)^i}{i!}B_i F^{(i-1)}(0)
$$

$B_i$는 $i$번째 베르누이 수이고, $F^{(i-1)}(0)=(a\Lambda)^{-(i-2)}f^{(i-2)}\left(\frac{n}{a\Lambda}\right)$이다. 1차항까지만 계산하여 힘을 구하고 $\hbar, c$를 되살리면 다음을 얻는다.

$$
F(a)=-\frac{\pi \hbar c}{24a^2}\simeq \frac{-4\times 10^{-27}[ \textrm{Nm^2}]}{a^2}
$$

이는 $a=1nm$에서 약 $4\times 10^{-9}[ \textrm{N}]$의 힘으로, 도마뱀붙이의 강모 하나가 가지는 점착력과 유사하다.