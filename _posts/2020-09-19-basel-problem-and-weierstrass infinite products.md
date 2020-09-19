---
layout: post
title: "바젤 문제와 바이어슈트라스 무한곱"
author: "YGLENA"
comments: true
tags: [Calculus, Complex analysis]
---
* 
{:toc}

## 바젤 문제
> **바젤 문제<sup>Basel problem</sup>.** 다음이 성립한다.
>
>$$
\sum_{n=1}^\infty \frac{1}{n^2} = \frac{\pi^2}{6}
>$$
>

바젤 문제는 1650년 피에트로 멩골리<sup>Pietro Mengoli</sup>에 의해 제시되었고, 1734년 레온하르트 오일러<sup>Leonhard Euler</sup>에 의해 해결된 문제이다. 이 문제는 모든 자연수의 제곱의 역수의 합을 닫힌 형식<sup>closed form</sup>으로 적는 것을 제시한다. 오일러는 28살의 나이에 이 문제를 푼 것 뿐만이 아니라, 모든 자연수의 $2n$-제곱의 역수의 합을 닫힌 형식으로 적어 유명세를 얻었다. 그러나 모든 자연수의 $2n+1$-제곱의 역수의 합, 가장 간단하게는 세제곱의 역수의 합이 닫힌 형식으로 적힐 수 있는지는 아직 알려지지 않았다.

바젤<sup>Basel</sup>은 오일러의 고향으로, 스위스 북서부에 위치해 있다.

## 역사적 접근
1655년, 존 왈리스<sup>John Wallis</sup>가 바젤 급수의 합을 소수점 세 자리까지(1.645) 계산하였으나 이것이 $\pi^2/6$과 가까움은 눈치채지 못했다. 1673년, 고트프리트 빌헬름 라이프니츠<sup>Gottfried Willhelm Leibniz</sup>는 존 베르누이<sup>John Bernoulli</sup>에게 보낸 편지에서 다음을 발견하였다. 식

$$
\sum_{n=1}^{\infty} \frac{x^n}{n}=-\frac{\log (1-x)}{x}
$$

의 양변을 적분하면

$$
\sum_{n=1}^{\infty} \frac{x^n}{n^2}=-\int_0^x \frac{\log (1-t)}{t} dt
$$

가 되나, 이는 $x=1$일 때 발산한다. 따라서 $x$  대신 $-x$를 집어넣어

$$
\sum_{n=1}^{\infty} (-1)^n \frac{x^n}{n}=-\int_0^x \frac{\log (1+t)}{t} dt
$$

를 얻는다. 이를 부분적분하면 다음과 같은 적분 항이 남고,

$$
\int_0^x \frac{\log t}{1+t} dt
$$

다음 전개를 생각하자.

$$
\ln t = -\sum_{n=1}^{\infty}\frac{1}{n} (1-t)^n,\quad \frac{1}{1+t}=\sum_{n=0}^{\infty} (-t)^n
$$

그러면 위의 적분 항은 다음 적분들의 합으로 표현됨을 알 수 있다.

$$
\int_0^x x^n (1-x)^m dx
$$

라이프니츠는 이러한 형태의 적분을 모두 고려할 수 있다면 바젤 문제의 단서가 보이리라 추측하였다.

바젤 문제의 느린 수렴성은 당대에도 큰 골칫거리였다.[^1] 1728년, 다니엘 베르누이<sup>Daniel Bernoulli</sup>는 크리스티안 골드바흐<sup>Christian Goldbach</sup>에게 보낸 편지에서 바젤 급수의 근사값을 빠르게 구할 수 있는 방법을 알아냈다고 주장하였고, 근사값 $8/5$을 제시하였다. 골드바흐는 답장에서 바젤 급수의 값을 $41/25$와 $5/3$ 사이로 줄일 수 있다고 주장하였다. 이들이 어떻게 이러한 값을 얻었는지는 알려져 있지 않다.

[^1]: 바젤 급수의 소수점 밑 한 자리까지 정확하게 계산하기 위해서는 $n=10^2$까지 계산해야 한다. $n=10^3$에서 두 자리, $10^6$에서 다섯 자리까지 정확한 결과를 준다.

1731년 오일러는 다음과 같은 방법으로 빠르게 수렴하는 식을 제시하였다. 식

$$
-\sum_{n=1}^{\infty} \frac{1}{n^2} = \int_0 ^1 \frac{\log t}{1-t} dt
$$

의 적분구간을 둘로 쪼개어 다음과 같이 쓴다.

$$
\int_0 ^1 \frac{\log t}{1-t} dt=\int_0 ^x \frac{\log t}{1-t} dt+\int_x ^1 \frac{\log t}{1-t} dt
$$

두 번째 적분의 경우, $u=1-t$로 치환하고 $u$에 대해 급수전개하면 다음을 얻는다.

$$
\int_x ^1 \frac{\log t}{1-t} dt = -\sum_{n=1}^{\infty} \frac{(1-x)^n}{n^2}
$$

첫 번째 적분의 경우, $t$에 대해 적분한 뒤 부분적분을 해 주면 다음을 얻는다.

$$
\int_0 ^x \frac{\log t}{1-t} dt = -\log x \log (1-x) -\sum_{n=1}^{\infty} \frac{x^n}{n^2}
$$

이제 $x=1/2$를 대입해 주면 다음을 얻는다.

$$
\sum_{n=1}^{\infty} \frac{1}{n^2} = (\log 2)^2 + \sum_{n=1}^\infty \frac{1}{2^n n^2}
$$

이 식은 바젤 급수에 비해 빠른 수렴 속도를 가진다.

1732-1733년, 오일러는 콜린 매클로린<sup>Colin McLaurin</sup>과 함께 [오일러-매클로린 식](https://yglena.github.io/2020-05-03/euler-maclaurin-forumla)을 이용하여 소수점 밑 스무 자리까지 정확하게 계산하였다. 

1734년, 오일러는 사인 함수의 전개를 이용하여 바젤 문제를 해결함과 동시에, 자연수의 네제곱의 역수의 합 또한 계산하였다. $\pi$의 정수배수가 아닌 수 $\alpha$에 대하여 함수

$$
f(x)=1-\frac{\sin x}{\sin \alpha}
$$

를 생각하자. 라이프니츠는 이를 전개하여

$$
f(x)=1-\sum_{n=0}^{\infty} \frac{(-1)^{n+1}}{(2n+1)!}\frac{x^{2n+1}}{\sin \alpha}
$$

를 얻었다. f(x)의 근은 $2n\pi+\alpha$ 혹은 $2n\pi+\pi-\alpha$들이므로,

$$
f(x)=\prod_{n=-\infty}^{\infty} \left(1-\frac{x}{2n\pi +\alpha}\right)\left(1-\frac{x}{2n\pi +\pi -\alpha}\right)
$$

으로 쓰여진다. 양변의 계수를 비교하면,

$$
\frac{1}{\alpha} + \sum_{n=1}^{\infty}\left(\frac{1}{(2n-1)\pi -\alpha}-\frac{1}{(2n-1)\pi+\alpha}+\frac{1}{2n\pi+\alpha}-\frac{1}{2n\pi-\alpha}\right)=\frac{1}{\sin \alpha}
$$

$$
\frac{1}{\alpha^2} + \sum_{n=1}^{\infty}\left(\frac{1}{((2n-1)\pi -\alpha)^2}-\frac{1}{((2n-1)\pi+\alpha)^2}+\frac{1}{(2n\pi+\alpha)^2}-\frac{1}{(2n\pi-\alpha)^2}\right)=\frac{1}{\sin^2 \alpha}
$$

$$
\frac{1}{\alpha^3} + \sum_{n=1}^{\infty}\left(\frac{1}{((2n-1)\pi -\alpha)^3}-\frac{1}{((2n-1)\pi+\alpha)^3}+\frac{1}{(2n\pi+\alpha)^3}-\frac{1}{(2n\pi-\alpha)^3}\right)=\frac{1}{\sin^3 \alpha}-\frac{1}{2\sin \alpha}
$$

등을 얻는다.

$\alpha$에 다양한 값을 넣음으로써 우리는 다양한 무한급수의 합을 구할 수 있다. $\alpha=\pi/2$를 넣으면, 제임스 그레고리<sup>James Gregory</sup>가 계산하여 이미 알려진 식

$$
\sum_{n=0}^{infty} \frac{(-1)^n}{2n+1} = \frac{\pi}{4}
$$

를 얻는다. 두 번째 식은

$$
\sum_{n=0}^{\infty} \frac{1}{(2n+1)^2} = \frac{\pi^2}{8}
$$

을 주고, 이를 이용하여 바젤 급수의 합 $\pi^2/6$을 얻을 수 있다. 같은 방법으로, 자연수의 네제곱의 역수의 합이 $\pi^4/90$임을 알 수 있다.

$\alpha=\pi/4$를 넣으면 오일러가 뉴턴에게 헌정한 다음 사실을 얻는다.

$$
1+\frac{1}{3}-\frac{1}{5}-\frac{1}{7}+\frac{1}{9}+\cdots = \frac{\pi}{2\sqrt{2}}
$$

이러한 다양한 결과를 주는 식 이전에, 오일러는 이미 베젤 급수를 다음 관계를 통해 계산하였다.

$$
\frac{\sin x}{x} = \prod_{n=1}^{\infty} \left(1-\frac{x^2}{(n\pi)^2}\right)
$$

그러나 그는 이것이 정확하게 일치하는 관계임은 보이지 못했다.

## 바이어슈트라스 무한곱
> **바이어슈트라스 무한곱<sup>Weierstrass infinite product</sup>.** 복소수의 수열 $\\\{a_n\\\}$에 대하여 $\lim_{n\rightarrow \infty} \lvert a_n\rvert=\infty$일 때, 어떤 전해석 함수<sup>entire function</sup> $f$ 가 존재하여 $z=a_n$에서, 그리고 그곳에서만 $0$이 된다. 이를 만족하는 모든 전해석 함수는 전해석 함수 $g$에 대하여 $f(z)e^{g(z)}$로 적어진다. $f$는 다음과 같이 적을 수 있고, 이를 **바이어슈트라스 곱**이라 한다.
>
> $$
f(z)=z^m\prod_{n=1}^\infty E_n(z/a_n),\quad E_k=(1-z)e^{\sum_{n=1}^k z^k/k},\quad E_0=1-z
> $$

바이어슈트라스 무한곱 정리는 어떤 전해석 함수에 대해서도 오일러 급수와 같은 논증을 할 수 있음을 알려 준다. 그러나 필연적으로 붙게 되는 전해석 함수의 지수함수는 제거할 수 없다. 사인 함수의 절대값이 $e^{\lvert z\rvert} $의 꼴로 증가함을 이용하면 지수 위의 함수가 반드시 차수 1 이하의 다항식임을 추측할 수 있다. 실제로 다음이 성립한다.

> **아다마르 분해 정리<sup>Hadamard factorization theorem</sup>.** $f$가 전해석 함수이고, 어떤 $A, B, \rho_0$에 대하여 다음이 항상 성립한다 하자.
>
>$$
\lvert f(z)\rvert \leq Ae^{B\lvert z\rvert^{\rho_0}}
>$$
>
> $k=\[\rho_0\]$이라 하고, $\\\{a_n\\\}$이 $f$의 0이 아닌 해의 수열이라 할 때, 다음이 성립한다.
>
>$$
f(z)=e^{P(z)}z^m\prod_{n=1}^{\infty} E_k(z/a_n)
>$$
>
>이 때 $P$는 차수 $k$ 이하의 다항식이고, $m$은 $f$의 $z=0$에서의 해의 차수이다.

아다마르 분해 정리에 의하여 $\sin z/z$는 오일러가 제시한 식에 $e^{Az+B}$를 곱한 꼴로 나타내짐을 알 수 있고, 따라서 $z=0$을 대입하면 $B=0$을 얻는다. $z=-z$로 치환하여 $A=0$을 얻으면 오일러가 얻은 식이 옳음을 증명할 수 있다.

아다마르 분해 정리를 이용하여 다양한 함수를 무한곱의 형태로 쓸 수 있다. 이를테면 다음이 성립한다.

$$
e^z -1= e^{z/2}z\prod_{n=1}^\infty \frac{1+z^2}{4n^2\pi^2}
$$

$$
\cos \pi z = \prod_{n=0}^\infty \frac{1-4z^2}{(2n+1)^2}
$$

## 사인 함수의 곱전개
오일러가 계산해낸 사인 함수의 곱전개를 증명하기 위해 아다마르 분해 정리를 사용할 수 있지만, 여기서는 좀더 직접적인 방법을 사용해 보자. 우선 다음 보조 정리를 증명한다.

> **보조정리.** $z$가 정수가 아닌 복소수일 때, 다음이 성립한다.
>
>$$ 
\pi \cot \pi z=\lim_{N\rightarrow\infty} \sum_{\lvert n\rvert \leq N} \frac{1}{z+n} = \frac{1}{z}+\sum_{n=1}^{\infty}\frac{2z}{z^2-n^2}
>$$

<details><summary>**증명.**
</summary>

복소함수 $F(z)=\pi \cot \pi z$에 대하여, 다음이 성립함을 쉽게 확인할 수 있다.

1. $z$가 $F(z+1)-F(z)$이다.
2. $0$ 근방에서 해석적인 함수 $F_0$가 존재하여, $F(z)=\frac{1}{z}+F_0(z)$이다.
3. $F(z)$는 정수점 위에서 단순 극점<sup>simple pole</sup>을 가지고, 다른 특이점<sup>singularity</sup>은 가지지 않는다.

또한 우변도 이러한 성질이 성립함을 알 수 있다. 따라서 다음과 같이 정의된 함수 $\Delta$는 $\Delta(z+1)=\Delta(z)$이고 전해석 함수이다.

$$
\Delta(z)=F(z)-\sum_{n=-\infty}^{\infty}\frac{1}{z+n}
$$

이제 $z=x+iy$라 쓸 때 $\lvert x\rvert \leq 1/2$이고 $\lvert y\rvert > 1$인 영역을 생각하자. $y>1$일 때,

$$
\cot \pi z = i\frac{e^{-2\pi y}+e^{-2\pi i x}}{e^{-2\pi y-e^{-2\pi i x}}}
$$
이므로 이의 절대값은 유계<sup>bounded</sup>이다. 또한,

$$
\frac{1}{z}+\sum_{n=1}^{\infty}\frac{2z}{z^2-n^2}=\frac{1}{x+iy}+\sum_{n=1}^{\infty}\frac{2(x+iy)}{x^2-y^2-n^2+2ixy}
$$

이고 $y>1$이므로,

$$
\left\lvert\frac{1}{z}+\sum_{n=1}^{\infty}\frac{2z}{z^2-n^2}\right\rvert\leq C+C\sum_{n=1}^{\infty}\frac{y}{y^2+n^2}\leq C+C\int_{0}^{\infty} \frac{y}{y^2+x^2} dx
$$

이다. 적분에서 $x$를 $yx$로 치환하면 이 적분값은 $y$과 관계 없으며 유한함을 알 수 있다. 따라서 $\lvert x \rvert \leq 1/2$이고 $y>1$인 영역에서 $\Delta$는 유계이다.

비슷한 방법으로 $\lvert x \rvert \leq 1/2$이고 $y<-1$일 때 $\Delta$는 유계이다. $\lvert x\rvert \leq 1/2$, $\lvert y\rvert \leq 1$의 범위가 컴팩트<sup>compact</sup>하므로 $\Delta$는 $\lvert x\rvert \leq 1/2$에서 유계이다. $\Delta(z+1)=\Delta(z)$임으로부터 $\Delta$는 복소평면 전체에서 유계이고, 따라서 리우빌의 정리<sup>Liouville's theorem</sup>에 의하여 $\Delta(z)$는 상수이다. $\Delta$가 우함수이므로 $\Delta\equiv 0$이다. $\square$

</details>

또한, 함수 곱전개의 수렴성을 증명하기 위해 다음의 보조정리 둘을 증명하자.

> **복소수 무한곱의 수렴성.**  복소수 순열 $\\{a_n\\}$에 대하여 $\sum_{n=1}^{\infty} \lvert a_n \rvert < \infty$일 때, $\prod_{n=1}^{\infty}(1+a_n)$은 수렴한다. 또한, 이 곱이 $0$임과 $1+a_n=0$인 $n$이 존재함이 동치이다.

<details><summary>**증명.**
</summary>

합의 수렴성에 의하여, 모든 $n$에 대해 $\lvert a_n \rvert < 1/2$임을 가정할 수 있다. 또한 $\lvert z\rvert < 1$에서 $1+z=e^{\log (1+z)}$이므로, $B_N=\sum_{n=1}^N b_n$, $b_n=\log (1+a_n)$으로 쓰면 무한곱의 부분곱을 다음과 같이 쓸 수 있다.

$$
\prod_{n=1}^N (1+a_n) = e^{B_N}
$$

$\log$ 함수의 급전개를 이용하면 $\lvert z\rvert < 1/2$일 때 $\lvert \log(1+z)\rvert \leq 2\lvert z\rvert$이고, 따라서 $\lvert b_n\rvert \leq 2\lvert a_n\rvert$이다. 따라서 $\lim_{N\rightarrow \infty} B_N = B < \infty$이다. 지수함수의 연속성에 의해 이 무한곱은 $e^B$로 수렴한다.

$1+a_n=0$이면 무한곱은 자명하게 $0$이다. 모든 $1+a_n$이 $0$이 아니면 무한곱이 유한한 $B$에 대해 $e^B$의 꼴로 수렴하고, 이는 $0$이 아니다. $\square$

</details>

> **해석함수의 무한곱의 수렴성.** $\\{F_n\\}$이 열린 집합 $\Omega$ 위에서의 해석함수의 순열일 때, 복소수 순열 $\\{c_n>0\\}$이 존재하여 $\sum c_n < \infty$이고, 모든 $z\in \Omega$에 대해 $\lvert F_n(z)-1 \rvert \leq c_n$이라 하자. 그러면 $\prod_{n=1}^\infty F_n(z)$는 $\Omega$ 위에서 해석함수로 균등수렴<sup>uniform convergence</sup>하고, 어떤 $z$에 대하여, 모든 $n$이 $F_n(z)\neq 0$를 만족시킨다면, 다음을 만족한다.
>
>$$
\frac{F^{\prime}(z)}{F(z)}=\sum_{n=1}^{\infty}\frac{F_n^{\prime}(z)}{F_n(z)}
>$$

<details><summary>**증명.**
</summary>

균등수렴성은 $\prod_{n=1}^{\infty} (1+c_n)$의 수렴성에 의하여 성립한다. $K$가 $\Omega$ 안의 컴팩트 집합이라 할 때, $G_N(z)=\prod_{n=1}^N F_n(z)$라 하자. $\Omega$에서 $G_N$이 $F$로 균등수렴하므로, $K$에서 $G_N^{\prime}$이 $F^{\prime}$으로 균등수렴한다. 또한 $G_N$이 $K$에서 균등하게 밑에서 유계이므로, $K$에서 $G_N^{\prime}/G_N$는 $F^{\prime}/F$로 균등수렴한다. 따라서 모든 점에서 위와 같이 수렴한다. $G^{\prime}_N / G_N = \sum\_{n=1}^{N} F_n^{\prime} / F_n$이므로 주어진 식이 참이다. $\square$

</details>

이제 다음을 증명할 수 있다.

> **사인 함수의 곱전개.** 다음이 성립한다.
>
>$$
\frac{\sin \pi z}{\pi z} = \prod_{n=1}^{\infty} \left(1-\frac{z^2}{n^2}\right)
>$$

<details><summary>**증명.**
</summary>

다음과 같이 쓰자.

$$
G(z)=\frac{\sin \pi z}{\pi},\quad P(z)= z\prod_{n=1}^{\infty} \left(1-\frac{z^2}{n^2}\right)
$$

$\sum_{n=1}^\infty 1/n^2 < \infty$이므로, $P(z)$는 수렴한다. 또한 $z$가 정수가 아닐 때 다음을 얻는다.

$$
\frac{P'(z)}{P(z)}=\frac{1}{z}+\sum_{n=1}^{\infty}\frac{2z}{z^2-n^2}
$$

또한 $G'(z)/G(z)=\pi \cot \pi z$이므로, 다음을 얻는다.

$$
\left( \frac{P(z)}{G(z)}\right)^{\prime} = \frac{P(z)}{G(z)} \left[ \frac{P^{\prime} (z)}{P(z)} - \frac{G^{\prime} (z)}{G(z)}\right] = 0
$$

따라서 어떤 상수 $c$에 대해 $P(z)=cG(z)$이고, 양변을 $z$로 나누고 $z\rightarrow 0$으로 보내면 $c=1$임을 얻는다. $\square$

</details>


## 출처
- [*Euler and the Zeta Function*](https://www.jstor.org/stable/2319041), Raymond Ayoub
- E. M. Stein and R. Shakarchi, Complex Analysis (Princeton University Press, 2003)