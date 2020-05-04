---
layout: post
title: "오일러-매클로린 급수"
author: "YGLENA"
comments: true
tags: [Calculus]
---
* 
{:toc}
## 베르누이 다항식과 베르누이 수
**베르누이 다항식<sup>Bernoulli polynomials</sup>** $B_n(x)$이란 다음 생성함수를 통해 정의되는 다항식이다.

$$
\frac{te^{xt}}{e^{t}-1}=\sum_{n=0}^{\infty} B_n(x)\frac{t^n}{n!}
$$

베르누이 다항식의 첫 다섯 항은 다음과 같다.

$$
\begin{align*}
B_0 (x) &= 1\\\
B_1(x) &= x-\frac{1}{2}\\\
B_2(x) &= x^2-x+\frac{1}{6}\\\
B_3(x) &= x^3-\frac{3}{2}x^2+\frac{1}{2}x\\\
B_4(x) &= x^4-2x^3+x^2-\frac{1}{30}
\end{align*}
$$


베르누이 다항식을 이용하여 **주기화된 베르누이 함수<sup>periodized Bernoulli function</sup>** $\psi_k(x)=B_k(x-\lfloor x \rfloor )$를 정의할 수 있다. 

**베르누이 수<sup>Bernoulli number</sup>** $B_n$이란 다음 생성함수를 통해 정의되는 수열이다.

$$
\frac{t}{e^t -1}=\sum_{n=0}^{\infty} B_n \frac{ t^n}{n!}
$$

베르누이 수의 첫 0이 아닌 다섯 항은 다음과 같다.

$$
B_0=1,\quad B_1=-\frac{1}{2},\quad B_2=\frac{1}{6},\quad B_4=-\frac{1}{30},\quad B_6=\frac{1}{42}
$$

### 성질
> $B_n=B_n(0)$이다. 또한, 이 값은 $n$이 1이 아닌 홀수일 때 항상 $0$이다.
<details><summary>**증명.**
</summary>

베르누이 다항식의 생성함수에 $x=0$을 대입하면 베르누이 수의 생성함수를 얻는다. 베르누이 수의 생성함수에 대하여,

$$
\begin{align*}
\frac{x}{e^x -1}-\frac{-x}{e^{-x}-1}&=\frac{x(e^x+e^{-x}-2)}{(e^x-1)(e^{-x}-1)}\\\
&=-x
\end{align*}
$$

이므로, $n\neq 1$인 홀수일 때 $B_n$은 $0$이다. $\square$
</details>

> $B_n(0)=(-1)^n B_n(1)$이다.
<details><summary>**증명.**
</summary>

$B_n(1)$의 생성함수는 $\frac{te^t}{e^t-1}$이고, 따라서 $(-1)^n B_n(1)$의 생성함수는 $\frac{-te^{-t}}{e^{-t}-1}=\frac{-t}{1-e^t}$로 $B_n(0)$의 생성함수와 같다. $\square$
</details>

> $B_n'(x)=nB_{n-1}(x)$이다.
>> 따라서 $\psi_n'(x)=n\psi_{n-1}(x)$이다.
<details><summary>**증명.**
</summary>

$B_n'(x)$의 생성함수는 $\frac{t^2 e^{xt}}{e^t-1}$이고, 이는 다음과 같이 전개된다.

$$
\frac{t^2 e^{xt}}{e^t-1}=\sum_{n=0}^{\infty}B_n(x)\frac{t^{n+1}}{n!}=\sum_{n=1}^\infty nB_{n-1}(x)\frac{t^n}{n!}
$$

따라서 $B_n'(x)=nB_{n-1}(x)$이고, $B_0'(x)=0$이다. $\square$
</details>


>후르비츠 제타 함수
>
>$$
\zeta(s,x)=\sum_{n=0}^{\infty}\frac{1}{(x+n)^s}
>$$
>
>를 이용하여 베르누이 다항식을 다음과 같이 쓸 수 있다.
>
>$$
B_n(x)=-n\zeta (1-n, x)
>$$
>
>>따라서, 베르누이 수는 리만 제타 함수<sup>Riemann zeta function</sup> $\zeta(s)=\zeta(s,1)$ 를 이용하여 다음과 같이 쓸 수 있다.
>>
>>$$
B_{n}=(-1)^{1-n} n\zeta(1-n)
>>$$

>$1$차 이상의 주기화된 베르누이 함수는 다음과 같은 급수 표현을 가진다.
>
>$$
\begin{align*}
\frac{\psi_{2k}(x)}{(2k)!}&=(-1)^{k-1}\sum_{n=1}^{\infty} \frac{2\cos(2n\pi x)}{(2n\pi)^{2k}}\\\
\frac{\psi_{2k+1}(x)}{(2k+1)!}&=(-1)^{k-1}\sum_{n=1}^{\infty} \frac{2\sin(2n\pi x)}{(2n\pi)^{2k+1}}\\\
\end{align*}
>$$

## 오일러-매클로린 급수
>정수 $a,b\in \mathbb{Z}$와 함수 $f:[ a,b ]\rightarrow \mathbb{R}$에 대하여,  $f\in C^k([a, b])$일 때 다음이 성립한다.
>
>$$
\sum_{a < i \leq b}f(i) - \int_a^b f(x) dx=\left[\sum_{i=1}^k \frac{(-1)^i}{i!}\left( f^{(i-1)}(b)-f^{(i-1)}(a)\right)B_i \right]+ R_k
>$$
>
>이 때, 나머지 항 $R_k$는 다음과 같이 쓰여진다.
>
>$$
R_k=-\int_a^b \frac{(-1)^k}{k!}\psi_k(x) f^{(k)} (x)dx
>$$
>

<details><summary>**증명.**
</summary>

$k=1$이라 하자. 아벨의 부분합 공식<sup>Abel partial summation formula</sup>

$$
\sum_{i=m}^n (a_{k+1}-a_k)b_k = a_{n+1}b_{n+1}-a_m b_m -\sum_{k=m}^n a_{k+1}(b_{k+1}-b_k)
$$

를 이용하여 다음과 같이 쓸 수 있다.

$$
\begin{align*}
\sum_{a< n \leq b} f(n)&=(b-a-1) f(b)+f(a)-\sum_{a\leq n\leq b-1} (n-a-1)(f(n+1)-f(n))\\\
&=(b-a-1) f(b)+f(a)-\sum_{a\leq n\leq b-1} (n-a-1)\int_n^{n+1} f'(t)dt\\\
&=(b-a-1) f(b)+f(a)-\sum_{a\leq n\leq b-1} \int_n^{n+1} (\lfloor t\rfloor - a-1)f'(t)dt\\\
&= bf(b)-af(a)-\int_a^b (t-(t-\lfloor t\rfloor))f'(t)dt\\\
\end{align*}
$$

부분적분을 이용하여,

$$
\begin{align*}
\sum_{a< n \leq b} f(n)&= \int_a^b f(t) dt + \int_a^b(t-\lfloor t\rfloor )f'(t)dt\\\
&=\int_a^b f(t)dt + \int_a^b \psi(t) f'(t) dt +\frac{1}{2}(f(b)-f(a))\\\
&=\int_a^b f(t)dt + \frac{1}{2}(f(b)-f(a))+R_1
\end{align*}
$$

$k>1$의 경우, 귀납법을 사용한다. 귀납 가정에 의하여 다음을 알고 있다.

$$
R_{k-1}=-\int_a^b \frac{(-1)^{k-1}}{(k-1)!}\psi_{k-1}(x)f^{(k-1)}(x)dx
$$

이를 부분적분하면 다음을 얻는다.

$$
R_{k-1}=\frac{(-1)^{k}}{k!}\left.\psi_{k}(x) f^{(k-1)}(x)\right\rvert_a^b-\int_a^b \frac{(-1)^{k}}{k!}\psi_{k}(x) f^{(k)}(x)dx
$$

뒤의 항은 $R_k$이고, 앞의 항은

$$
\frac{(-1)^k}{k!}B_k \left(f^{(k-1)}(b)-f^{(k-1)}(a)\right)
$$

이며, 이는 $k$차 오일러-매클로린 급수 항이다. $\square$
</details>

### 응용
#### 스털링 근사
>다음이 성립한다.
>
>$$
\log n!=n\log n-n+\frac{1}{2}\log 2\pi n+\mathcal{O}(n^{-1})
>$$
>
>이를 스털링 근사<sup>Stirling approximation</sup>이라 한다.

<details><summary>**증명.**
</summary>

$f(x)=\log x$로 두고, $k=1, a=1, b=n\in \mathbb{N}$이라 두면,

$$
\log n!=\sum_{i=1}^n \log i = n\log n - n + 1 + \frac{\log n}{2}+\int_1^n \frac{\psi_1(t)}{t} dt
$$

여기서, 부분적분을 이용해

$$
\int_1^n \frac{\psi_1(t)}{t}dt=\left.\frac{\psi_2(t)}{2t}\right\rvert_1^n+\int_1^n \frac{\psi_2(t)}{2t^2}dt
$$

를 얻는다. $\psi_2(t)$의 급수 표현으로부터 $\lvert\psi_2(t)\rvert<\infty$임을 알 수 있고, 따라서 위의 적분값 또한 모든 $n$에 대하여 유한함을 알 수 있다. 그러므로 $\log n$차수까지 다음을 얻는다.

$$
\log n!=n\log n-n+\frac{1}{2}\log n+\mathcal{O}(1)
$$

조금 더 정확하게, 다음이 성립한다.

$$
\lim_{n\rightarrow \infty}\int_1^n \frac{\psi_1(t)}{t} dt + 1 = \log \sqrt{2\pi}
$$

따라서 다음을 얻는다.

$$
\log n!=n\log n-n+\frac{1}{2}\log 2\pi n+\mathcal{O}(n^{-1})
$$

$\square$

</details>

#### 파울하버의 공식
>모든 $p>1$에 대하여, 다음이 성립한다.
>
>$$
\sum_{k=1}^n k^p = \frac{n^{p+1}}{p+1}+\sum_{k=1}^p (-1)^k\frac{B_k}{k!}\frac{p!}{(p-k+1)!}n^{p-k+1}
>$$
>
>이를 파울하버의 공식<sup>Faulhaber formula</sup>이라 한다.

<details><summary>**증명.**
</summary> 

$f(x)=x^p$로 두고, $k=p$, $a=0$, $b=n\in \mathbb{N}$으로 두면,

$$
\sum_{k=1}^n k^p=\int_0^n x^p dx+\left[\sum_{i=1}^k \frac{(-1)^i}{i!}\frac{p!}{(p-i+1)!}n^{p-i+1} B_i\right]+R_k
$$

여기서,

$$
R_k=-\int_a^b \frac{(-1)^k}{k!}\psi_p(x)dx=0
$$

이고, 첫 항은 $\frac{n^{p+1}}{p+1}$이므로 준식이 성립한다. $\square$

</details>