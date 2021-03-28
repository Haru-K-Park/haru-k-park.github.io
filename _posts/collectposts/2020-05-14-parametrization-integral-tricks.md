---
layout: post
title: "매개화 적분법:<br> 파인만/슈윙거 매개화"
author: "YGLENA"
comments: true
tags: [Calculus]
---
<details><summary>
<span style="font-size:2em;">**목차**</span>
</summary>
* 목차
{:toc}
</details>
## 개요
파인만 도형을 계산할 때, 전파자<sup>propagator</sup>가 관여하는 항이 $\frac{i}{p^2-m^2}$으로 쓰여지기 때문에 다음과 같은 적분이 빈번하게 등장한다.

$$
\int \frac{d^D p}{(2\pi)^D}\frac{1}{(p^2-m^2)^a[(p-k)^2 -m^2]^b}
$$

이 적분은 $D>1$차원 상에서의 적분으로써 그 값을 구하기 대단히 까다로우며, 결과값을 구하지 않고 각 변수 $m,k,D$에 따라 적분값이 어떻게 변화하는지 근사하기조차도 어렵다.

파인만 매개화<sup>Feynman parametrization</sup>는 두 개의 값의 곱의 역수를 적분으로 풀어 쓰는 것을 말한다. 이 매개화로 인하여 변수가 늘어나지만, 많은 경우 적분의 순서를 바꾸는 과정을 통해 기존에 있던 적분을 없애고, 이를 통해 $D$차원 상에서의 적분을 $1$차원 상에서의 적분으로 변형할 수 있다. 위의 식에 파인만 매개화를 적용한 결과는 다음과 같다.

$$
\frac{\Gamma{(a+b)}}{\Gamma(a)\Gamma(b)}\int_0^1 dx \int\frac{d^D p}{(2\pi)^D}\frac{(1-x)^{a-1}x^{b-1}}{[p^2 -m^2-2pk x+k^2x]^{a+b}}
$$

$p$에 대한 적분은 이제 정확하게 계산 가능하고, 다음을 얻는다.

$$
\frac{1}{(4\pi)^{D/2}}\frac{\Gamma(a+b)}{\Gamma(a)\Gamma(b)}\int_0^1 dx \frac{(1-x)^{a-1}x^{b-1}}{[k^2 x(1-x) -m^2 ]^{a+b-D/2}}
$$

슈윙거 매개화<sup>Schwinger parametrization</sup>는 어떤 값의 $n$제곱의 역수를 적분으로 풀어 쓰는 것을 말한다. 마찬가지로 파인만 도형을 계산하는데 사용되고, 파인만 매개화를 증명하는 데에도 유용하게 사용된다.

## 슈윙거 매개화
>다음이 성립한다.
>
>$$
\frac{1}{A^n}=\frac{1}{\Gamma(n)}\int_0^\infty du\, u^{n-1}e^{-uA}
>$$

<details><summary>**증명.**
</summary>

감마 함수 $\Gamma(n)$은 $n$의 실수부가 $0$보다 클 때 항상 잘 정의되며, 다음과 같이 쓰여진다.

$$
\Gamma(n)=\int_0^\infty dx\, x^{n-1}e^{-x}
$$

이제 $x$를 $uA$로 치환한다. $\square$
</details>

## 파인만 매개화
>다음이 성립한다.
>
>$$
\frac{1}{A_1^{\alpha_1}\cdots A_n^{\alpha_n}}=\frac{\Gamma(\alpha_1+\cdots+\alpha_n)}{\Gamma(\alpha_1)\cdots\Gamma(\alpha_n)}\int_0^1 du_1\,\cdots\int_0^1 du_n\,\frac{\delta\left(1-\sum_{k=1}^n u_k\right)u_1^{\alpha_1-1}\cdots u_n^{\alpha_n -1}}{\left(\sum_{k=1}^n u_k A_k\right)}
>$$
>> 따라서, 아주 단순한 경우로, 다음이 성립한다.
>>
>>$$
\frac{1}{AB}=\int_0^1 \frac{du}{\left[ uA+(1-u)B\right]^2}
>>$$