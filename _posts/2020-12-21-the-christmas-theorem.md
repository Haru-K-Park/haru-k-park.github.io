---
layout: post
title: "크리스마스 정리"
author: "YGLENA"
comments: true
tags: [Number theory]
---
* 
{:toc}

## 크리스마스 정리
> **크리스마스 정리<sup>The Christmas Theorem</sup>.** 홀수 소수 $p$에 대해, $p$가 두 개의 제곱수의 합으로 나타내짐과, $p\equiv 1 \mod 4$임이 동치이다.

크리스마스 정리는 1625년 프랑스의 알버트 지라드<sup>Albert Girard</sup>에 의해서, 두 제곱수의 합으로 표현 가능한 모든 수를 제시함으로써 알려졌다. 이후 1640년 12월 25일, 피에르 드 페르마<sup>Pierre de Fermat</sup>는 마랭 메르센<sup>Marin Mersenne</sup>에게 보낸 편지에서 이를 더욱 정교하게 발전시켰다. 이것이 크리스마스의 일이었기 때문에 이 정리는 종종 **페르마의 크리스마스 정리**로 불린다.

페르마는 다른 정리들처럼 크리스마스의 정리에 대해 자신의 증명을 제시하지 않았다. 첫 증명은 레온하르트 오일러<sup>Leonhard Euler</sup>가 무한강하법<sup>infinite descent</sup>을 이용해 제시하였고, 이후 조제프루이 라그랑주<sup>Joseph-Louis Lagrange</sup>는 이차 형식<sup>quadratic form</sup>을 이용한 증명을 제시하였다. 리하르트 데데킨드<sup>Richard Dedekind</sup>는 가우스 정수<sup>Gaussian integer</sup>를 이용한 증명을 제시한 바가 있고, 데이비드 크리스토퍼<sup>David Christopher</sup>는 분할 이론<sup>partition theory</sup>을 이용한 증명을 제시하였다.

여기에서는, 로저 히스 브라운<sup>Roger Heath-Brown</sup>에 의해 제시된 짧은 증명을 더욱 간략화한 돈 재기어<sup>Don Zagier</sup>의 한 줄 증명과, 크리스마스 정리의 일반화인 야코비의 두 제곱수 정리<sup>Jacobi's two-square theorem</sup>의 증명을 살펴본다. 특히, $p\equiv 3 \mod 4$인 홀수들의 경우, 모든 제곱수는 $4$로 나눈 나머지가 $0$이거나 $1$이기 때문에 두 제곱수의 합으로 나타내는 것이 불가능함을 알 수 있으므로, $p\equiv 1 \mod 4$인 소수들 하에서 그것이 가능함만을 보일 것이다.

## 재기어의 한 줄 증명

<details><summary>**재기어의 한 줄 증명.**
</summary>

유한집합 $S=\\{ (x,y,z)\in \mathbb{N}^3:x^2+4yz=p\\}$의 다음 대합<sup>involution</sup>

$$
(x,y,z)\mapsto \begin{cases}
&(x+2z,z,y-x-z),& x < y-z \\\
&(2y-x, y, x-y+z),& y-z < x < 2y \\\
&(x-2y, x-y+z, y),& x > 2y
\end{cases}
$$

은 단 하나의 고정점을 가지므로 $\vert S \vert $는 홀수이고, 따라서 $ (x,y,z)\mapsto (x,z,y) $는 고정점을 가진다. $\square$

   <details><summary>**네...?**
   </summary>

   이 증명은 한 줄로 구성되어 있지만 많은 세부적인 내용이 생략되어 있다. 하나하나씩 살펴 보자.

   * **$S$는 유한집합이다** : $0 < x,y,z \leq p$이므로, $\vert S \vert < p^3$이다.

   * **주어진 식이 대합이다** : 주어진 식을 $f$라고 하자. $f(x,y,z)\in S$임은 직접 계산으로 확인할 수 있다.
      * $x < y-z$일 때, $f(x,y,z)=(x+2z, z, y-x-z)$이다. $y-x-z>0$이므로 이는 잘 정의된다. $x+2z>2z$이므로 $f^2(x,y,z)=(x,y,z)$이다. 
      * $y-z< x< 2y$일 때, $f(x,y,z)=(2y-x, y, x-y+z)$이다. $2y-x>0$이고 $x+z-y>0$ 이므로 이는 잘 정의된다. $2y-x-z < 2y-x < 2y$이므로 $f^2(x,y,z)=(x,y,z)$이다.
      * $x > 2y$일 때, $f(x,y,z)=(x-2y, x-y, y)$이다. $x-2y>0$이므로 이는 잘 정의된다. $x-2y< x-2y+z$이므로 $f^2(x,y,z)=(x,y,z)$이다.
   
   * **단 하나의 고정점을 가진다** : $x=x+2z$임과 $x=x-2y$임이 불가능하므로, $y-z< x < 2y $ 조건 하에서 $x=2y-x$, $z=x-y+z$ 두 가지 조건을 충족시켜야 고정점이 된다. 이는 $x=y$임을 말하고, 따라서 $x(x+4z)=p$가 된다. $p$가 소수이고 $x< x+4z$이므로 $x=1$이고, 따라서 $p=4z+1$이다. $p\equiv 1 \mod 4$이므로 그러한 $z$는 존재한다.

   이 증명의 특징은 비구성적<sup>non-constructive</sup>이라는 것이다. 우리는 이 증명을 통해 그러한 표현이 존재한다는 것만을 알 수 있을 뿐, 어떤 제곱수 둘이 $p$를 나타내는지는 조금도 알 수 없다.

   해당 대합은 정사각형에 네 개의 직사각형을 둘러 붙인 도형의 두 가지 분할법으로 그림화시켜 나타낼 수 있다. [다음 링크](https://mathoverflow.net/questions/31113/zagiers-one-sentence-proof-of-a-theorem-of-fermat/299696#299696)에서 그림을 확인할 수 있다.

   </details>

</details>

## 야코비의 두 제곱수 정리
> 양의 정수 $n$에 대하여, $d_i(n)$을 $d\equiv i \mod 4$이고 $d\vert n$인 양의 정수 $d$의 수로 정의하자. 그러면, 양의 정수 $n$을 두 제곱수의 합으로 나타내는 방법의 수는 $4(d_1(n)-d_3(n))$이다.

소수 $p$가 $p\equiv 1 \mod 4$일 경우, $d_1(p)=1$이고 $d_3(p)=0$이므로 그러한 방법의 수는 $4>0$가지고, 따라서 존재한다.

이 증명 또한 비구성적이다. 반대로, 크리스마스 정리의 고전적인 증명은 대부분 구성적이다.

<details><summary>**증명.**
</summary>

이 증명에는 다음 세 곱 항등식<sup>triple-product identity</sup>이 사용된다.

$$
\prod_{n\geq 1}(1+ax^{2n-1})(1+a^{-1}x^{2n-1})(1-x^{2n})=\sum_{-\infty}^{\infty} a^n x^{n^2}
$$

이는 $a\neq 0$이면서 $\vert x\vert < 1$인 모든 복소수 $a, x$에서 성립한다.

위의 식에 $a$ 대신 $-a^2 x$를 대입하고, 이후 $x^2$ 대신 $x$를 대입하면 우리는 다음을 얻는다.

$$
(a-a^{-1})\prod_{n\geq 1}(1-a^2 x^n)(1-a^{-2}x^n)(1-x^n) = \sum_{-\infty}^{\infty} (-1)^n a^{2n+1} x^{(n^2+n)/2}
$$

우변의 식에서 $n$이 짝수인 경우와 홀수인 경우를 나누면 다음과 같이 쓸 수 있다.

$$
\sum_{-\infty}^{\infty} a^{4n+1} x^{2n^2 + n}-\sum_{-\infty}^{\infty} a^{4n-1} x^{2n^2 - n}
$$

각 항을 위와 같이 변형하면 다음을 얻는다.

$$
a\prod_{n\geq 1} (1+a^4 x^{4n-1}) (1+a^{-4}x^{4n-3})(1-x^{4n})-a^{-1}\prod_{n\geq 1} (1+a^4 x^{4n-3})(1+ax^{-4}x^{4n-1})(1-x^{4n}) 
$$

양변을 $a=1$에서 $a$로 미분하고 $2$로 나눠주면 다음을 얻는다.

$$
\prod_{n\geq 1}(1-x^n)^3 = \prod_{n\geq 1} (1+x^{4n-3})(1+x^{4n-1})(1-x^{4n}) \left\{ 1-4\sum_{n\geq 1} \left(\frac{x^{4n-3}}{1+x^{4n-3}}-\frac{x^{4n-1}}{1+x^{4n-1}} \right) \right\}
$$

이제,

$$
\prod_{n\geq 1}(1+x^n)^2(1-x^n)=\prod_{n\geq 1}(1+x^{4n-3})(1+x^{4n-1})(1-x^{4n})
$$

으로 양변을 나눠주면 다음을 얻는다.

$$
\prod_{n\geq 1}\left(\frac{1-x^n}{1+x^n}\right)^2= 1-4\sum_{n\geq 1} \left(\frac{x^{4n-3}}{1+x^{4n-3}}-\frac{x^{4n-1}}{1+x^{4n-1}} \right)
$$

또한,

$$
\prod_{n\geq 1}\left(\frac{1-x^n}{1+x^n}\right)=\sum_{-\infty}^{\infty} (-1)^n x^{n^2}
$$

이므로, 이를 넣고 $x\mapsto -x$를 대입하면 다음을 얻는다.

$$
\left(\sum_{-\infty}^{\infty}x^{n^2} \right)^2 = 1+4\sum_{n\geq 1} \left(\frac{x^{4n-3}}{1-x^{4n-3}}-\frac{x^{4n-1}}{1-x^{4n-1}}\right)
$$

이제 좌우변의 계수를 비교한다. 좌변의 $x$의 차수는 모든 두 제곱수의 합이고, 우변의 $x$의 차수는 $4n-3$과 $4n-1$의 배수들이다. 따라서 좌변의 $n$차 항의 차수는 $n$을 두 제곱수의 합으로 나타낼 수 있는 방법의 수이고, 우변의 $n$차 항의 차수는 $4(d_1(n)-d_3(n))$이다.

</details>

야코비의 두 제곱수 정리는 다음과 같은 따름정리 또한 준다.

> $1$보다 큰 양의 정수 $n$이 두 제곱수의 합으로 표현될 수 있음과, 그 소인수분해가 $p\equiv 3 \mod 4$인 소수 $p$와 홀수 $k$에 대해 $p^k$ 꼴의 항을 포함하지 않음이 동치이다.

<details><summary>**증명.**
</summary>

$d_{1,3}(2n)=d_{1,3}(n)$이므로, 홀수인 $n$에 대해서만 증명하면 된다. 소수 $p$로 나눠지지 않는 $d$에 대해서 $n=dp^k$라 하자. $p\equiv 1\mod 4$라면 $d_{1,3}(n)=(k+1)d_{1,3}(d)$이다. $p\equiv 3\mod 4$이고 $k=2i$라면 $d_{1}(n)=(i+1)d_{1}(d)+id_{3}(d)이고 $d_{3}(n)=id_{1}(d)+(i+1)d_{3}(d)$이다. 따라서 $d_1(n)-d_3(n)=d_1(d)=d_3(d)$이고, 이 두 경우에서 $d$와 $n$의 제곱수의 합으로 표현될 수 있음은 동치이다. 마지막으로 $k=2i-1$이라면 $d_{1,3}(n)=i(d_1(d)+d_3(d))$이므로 $d_{1}(n)-d_{3}(n)=0$이다. $\square$

</details>

이 따름정리는 다음 따름정리 또한 증명한다.
> 두 제곱수의 합으로 표현될 수 있는 수들의 집합은 곱에 의해 닫혀 있다.

이는, 위와 같은 비구성적 방법이 아니더라도, 다음 식에 의해서 즉시 증명된다.

$$
(a^2+b^2)(c^2+d^2)=(ac-bd)^2+(ad+bc)^2=(ac+bd)^2+(ad-bc)^2
$$

야코비의 두 제곱수 정리를 증명한 것과 유사한 방법으로, 모든 자연수는 제곱수 네 개의 합으로 표현될 수 있다는 라그랑주의 네제곱수 정리<sup>Lagrange's four square theorem</sup>을 증명할 수도 있다. 증명은 [다음 링크](https://web.maths.unsw.edu.au/~mikeh/webpapers/paper25.pdf)에서 확인할 수 있다.

## 출처
- [*A one-sentence proof that every prime $ p\equiv 1 \mod 4$ is a sum of two squares*](https://people.mpim-bonn.mpg.de/zagier/files/doi/10.2307/2323918/fulltext.pdf), D. Zagier
- [*A simple proof of Jacobi's two-square theorem*](https://web.maths.unsw.edu.au/~mikeh/webpapers/paper21.pdf), M. D. Hirschhorn