---
layout: post
title: "집합론 풀이 2장"
author: "YGLENA"
comments: true
tags: [Set theory, Problems and solutions]
---
* 
{:toc}

[T. Jech의 Set Theory](https://dio.org/10.1007/3-540-44761-X){:target="_blank"}
## 2.1.
>모든 부분순서집합<sup>partially ordered set</sup>의 모음<sup>class</sup>에서, 동형관계<sup>isomorphism</sup>는 동치관계<sup>equivalence relation</sup>이다.

### 풀이
1. \[반사 관계<sup>reflexivity</sup>.\] 부분순서집합 $(P,<)$에 대하여 $1_P:(P,<)\rightarrow (P,<)$로 둔다. 
2. \[대칭 관계<sup>symmetry</sup>.\] $f:(P,<)\rightarrow (Q,<)$가 동형사상일 때, $f^{-1}:(Q,<)\rightarrow(P,<)$ 또한 동형사상이다.
3. \[추이 관계<sup>transitivity</sup>.\] $f:(P,<)\rightarrow (Q,<)$와 $g:(Q,<)\rightarrow (R,<)$가 동형사상일 때, $g\circ f:(P,<)\rightarrow (R,<)$가 동형사상이다.

$\square$

## 2.2.
>$\alpha$가 극한서수<sup>limit ordinal</sup>임과, 모든 $\beta$에 대하여, $\beta<\alpha$이면 $\beta+1<\alpha$임이 동치이다.

### 풀이
$\alpha$가 극한서수라 하자. $\beta<\alpha$이고 $\beta+1\nless\alpha$인 $\beta$가 존재한다면, $\alpha$가 극한서수이므로 $\beta+1>\alpha$이다. 따라서 $\alpha=\beta$이거나 $\alpha<\beta$이고, 이는 모순이다.

모든 $\beta$에 대하여, $\beta<\alpha$이면 $\beta+1<\alpha$라고 하자. 어떤 $\gamma$에 대하여 $\gamma+1=\alpha$라 할 때, $\gamma<\alpha$이고 $\gamma+1\nless \alpha$이므로 모순이다. $\square$

## 2.3.
>집합 $X$가 귀납적<sup>inductive</sup>이면, $X\cap Ord$ 또한 귀납적이다. 집합 $\mathbb{N}=\cap \\{X:X\textrm{는 귀납적}\\}$는  0이 아닌 최소 극한서수<sup>least limit ordinal</sup>이다.

### 풀이
$\emptyset\in X\cap Ord$이고, $\alpha\in X\cap Ord$이면 $\alpha\cup \\{\alpha\\}=\alpha+1\in X\cap Ord$이다.

무한 공리<sup>axiom of infinity</sup>에 의하여 $\mathbb{N}$은 공집합이 아니다. $\mathbb{N}\cap Ord\subset \mathbb{N}$이 귀납적이므로 이는 $\mathbb{N}$이고, 따라서 $0\neq \mathbb{N}\in Ord$이다.

[문제 2.2](#22)에 의해 $\alpha$가 $0$이 아닌 극한서수임과 귀납적임은 동치이다. $\mathbb{N}$이 최소 귀납 집합이고 서수<sup>ordinal</sup>이므로 $0$이 아닌 최소 귀납 집합이다. $\square$

## 2.4.
>본 문제에서는 무한 공리를 가정하지 않는다.<br>
>$0$이 아닌 최소 극한이 존재한다면 이는 $\omega$이고, 존재하지 않는다면 $\omega=Ord$이다. 다음 명제들이 서로 동치임을 보여라.
>1. 귀납 집합이 존재한다.
>2. 무한 집합이 존재한다.
>3. $\omega$는 집합이다.

### 풀이

$1\Rightarrow 2$. 귀납 집합이 존재하므로 귀납 집합들의 교집합은 공집합이 아니다. 또한 이는 귀납 집합이다. [문제 1.11](https://yglena.github.io/2020-03-10/set-theory-T-Jech-solutions-chap1#111)에 따르면, 최소 귀납 집합은 $T$-무한하고, [문제 1.12](https://yglena.github.io/2020-03-10/set-theory-T-Jech-solutions-chap1#112)의 대우에 따르면 $T$-무한한 집합은 무한 집합이므로 무한 집합이 존재한다.

$2\Rightarrow 3$. 무한 집합 $X$에 대하여, $Y=\\{Z \in P(X) : \lvert Z\rvert < \infty \\}$를 생각하자. $X$가 집합이므로 멱집합 공리<sup>axiom of power set</sup>에 의하여 $P(X)$는 집합이고, 분리 공리꼴<sup>axiom schema of separation</sup>에 의하여 $Y$는 집합이다.

최소 극한이 존재한다면 [문제 1.9](https://yglena.github.io/2020-03-10/set-theory-T-Jech-solutions-chap1#19)의 귀납법을 이용할 수 있고, 최소 극한이 존재하지 않는다면 초한귀납법<sup>transfinite induction</sup>을 사용할 수 있다. 최소 극한이 존재하지 않는 경우 초한귀납법의 극한 서수에 관한 서술은 필요 없으므로, 두 경우 모두 같은 가정 하에 있다.

이제 함수 $f:Y\rightarrow Ord$를 $f(y)=\lvert y\rvert$가 되도록 정의한다. $\emptyset \in Y$이므로 $0\in \mathrm{ran} f$이고, $y\in Y$에 대하여 $y\subset X$이고, $X$가 무한집합이므로 $x\in X-y$를 고를 수 있다. 그러면 $y\cup \{x\}\in Y$이고 따라서 $\alpha\in \mathrm{ran} f$이면 $\alpha+1\in \mathrm{ran} f$이다. 따라서 $\mathrm{ran} f=\omega$이고, 치환 공리꼴<sup>axiom schema of replacement</sup>에 의하여 $\omega$는 집합이다.

$3\Rightarrow 1$. $\omega=Ord$인 경우, $Ord$가 귀납적이므로 $\omega$는 귀납 집합이다. $\omega$가 최소 극한인 경우, $\omega=\mathbb{N}$이므로 $\omega$는 귀납 집합이다.

$\square$

## 2.5.
> W가 정렬 집합<sup>well-ordered set</sup>일 때, $W$에서 $a_0>a_1>a_2>\cdots$를 만족시키는 순열 $\langle a_n:n\in \mathbb{N}\rangle$은 존재하지 않는다.

### 풀이
집합 $\\{a_n:n\in \mathbb{N}\\}$은 $W$의 부분집합이고, 따라서 최소 원소 $a_m$을 가진다. 그러나 이는 $a_m>a_{m+1}$임에 모순이다. $\square$

## 2.6.
> 임의의 큰 서수가 존재한다. 다시 말해, 모든 서수 $\alpha$에 대하여 $\beta>\alpha$인 극한서수 $\beta$가 존재한다.

### 풀이
$\alpha_0=\alpha$로 두고 $\alpha_n=\alpha+n$으로 두어, 극한 $\beta=\lim_{n\rightarrow \omega}\alpha_n$을 생각하자. 정의에 의해 $\alpha_n\leq \beta$이다. 만약 어떤 $m\in \omega$에 대해 $\alpha_m=\beta$라면, $\beta<\alpha_{m+1}$이므로 모순이다. 따라서 $\alpha_n\leq \beta$이다. 곧, $\gamma<\beta$에 대하여, $\gamma<\alpha$면 $\gamma+1\leq \alpha<\beta$이고, $\gamma\geq \alpha$이면 $\gamma=\alpha_n$이므로 $\gamma+1<\beta$이고, 따라서 $\beta$는 극한서수이다. $\square$

## 2.7.
> 모든 정규 순열<sup>normal sequence</sup>은 임의의 큰 고정점<sup>fixed point</sup>을 가진다. 다시 말해, 충분히 큰 어떤 서수 $\alpha$가 존재하여 $\gamma_\alpha=\alpha$이다.

### 풀이
어떤 $\alpha$에 대하여 $\alpha_0=\alpha$로 두고 $\alpha_{n+1}=\gamma_{\alpha_n}$으로 두어, 극한 $\beta=\lim_{n\rightarrow \omega} \alpha_n$을 생각하자. $\beta$가 극한서수이므로 $\gamma_\beta=\lim_{\xi\rightarrow \beta}\gamma_\xi$이다. 정의에 의하여 $\beta\leq \gamma_\beta$이다. $\beta<\gamma_\beta$라 하자. 그렇다면 어떤 서수 $\delta$가 존재하여 $\delta<\beta<\gamma_\delta$를 만족한다. 그러나 우리는 항상 $\delta<\alpha_m$을 만족하는 $m$을 찾을 수 있고, 따라서 $\gamma_\delta<\gamma_{\alpha_m}=\alpha_m<\beta$이므로 모순이다. 따라서 $\beta=\gamma_\beta$이다. $\square$

## 2.8.
> 모든 $\alpha, \beta, \gamma$에 대하여, 다음을 만족한다.
>1. $\alpha\cdot(\beta+\gamma)=\alpha\cdot\beta+\alpha\cdot\gamma$
>2. $\alpha^{\beta+\gamma}=\alpha^\beta\cdot\alpha^\gamma$
>3. $(\alpha^\beta)^\gamma=\alpha^{\beta\cdot\gamma}$

### 풀이
$\gamma$에 대한 초한귀납을 생각한다.
1. 주어진 $\alpha,\beta$에 대하여 해당 식을 만족시키는 $\gamma$의 모음을 생각하자. $\gamma=0$이면, $\alpha\cdot (\beta+0)=\alpha\cdot \beta$이고, $\alpha\cdot \beta+\alpha\cdot 0=\alpha\cdot \beta+0=\alpha\cdot \beta$이다.<br>$\delta$가 해당 식을 만족시킨다 할 때, $\alpha\cdot(\beta+(\delta+1))=\alpha\cdot ((\beta+\delta)+1)=\alpha\cdot(\beta+\delta)+\alpha=\alpha\cdot \beta+\alpha\cdot \delta+\alpha$이고, $\alpha\cdot \beta+\alpha\cdot(\delta+1)=\alpha\cdot \beta+\alpha\cdot \delta+\alpha$이므로, $\delta+1$ 또한 해당 식을 만족시킨다.<br>극한 $\eta$에 대해 $\delta<\eta$가 모두 해당 식을 만족시킨다면, $\alpha\cdot(\beta+\eta)=\alpha\cdot(\lim_{\delta\rightarrow \eta}(\beta+\delta))=\lim_{\xi\rightarrow \beta+\eta}(\alpha\cdot \xi)=\lim_{\xi\rightarrow \eta}(\alpha\cdot(\beta+\xi))=\lim_{\xi\rightarrow \eta}(\alpha\cdot \beta+\alpha\cdot \xi)$이고, 이는 곧 $\alpha\cdot \beta+\alpha\cdot \eta$와 같으므로 $\eta$ 또한 해당 식을 만족시킨다.

2. 와 3. 도 이와 같다.

$\square$

## 2.9. 
> 1. $(\omega+1)\cdot 2\neq \omega\cdot 2+1\cdot 2$임을 보여라.
> 2. $(\omega\cdot 2)^2\neq \omega^2\cdot 2^2$임을 보여라.

### 풀이
1. 
    &nbsp;

    $$
    \begin{align*}
    (\omega+1)\cdot 2&=(\omega+1)\cdot(1+1)\\\
    &=(\omega+1)+(\omega+1)\\\
    &=(\omega+(1+\omega))+1\\\
    &=(\omega+\omega)+1\\\
    &=\omega\cdot 2+1\\\
    &< \omega\cdot 2+1\cdot 2
    \end{align*}
    $$
    

2. 
    &nbsp;

    $$
    \begin{align*}
    (\omega\cdot 2)^2&=(\omega\cdot 2)^{1+1}\\\
    &=(\omega\cdot 2)\cdot(\omega\cdot 2)\\\
    &=(\omega\cdot(2\cdot \omega))\cdot 2\\\
    &=(\omega\cdot \omega)\cdot 2\\\
    &< \omega^2\cdot 2^2
    \end{align*}
    $$

$\square$

## 2.10.
> $\alpha<\beta$이면, $\alpha+\gamma\leq \beta+\gamma$이고, $\alpha\cdot \gamma\leq \beta\cdot \gamma$이고, $\alpha^\gamma\leq \beta^\gamma$이다.

### 풀이
$\gamma$에 대한 초한귀납법을 사용한다. $\gamma=0$일 때 정의에 의해 자명하다. $\gamma=1$일 때, $\alpha<\beta$라고 하자. $\beta<\alpha+1$이라면, $\alpha\in \beta\in \alpha\cup \\{\alpha\\}$이다. $\beta\neq \alpha$이므로 $\alpha\in \beta\in \alpha$에서 $\alpha<\alpha$를 얻고, 이는 모순이다. 따라서 $\alpha+1\leq \beta\leq \beta+1$이다. 이제 일반적인 $\delta$에 대하여,

$$
\alpha+(\delta+1)=(\alpha+\delta)+1\leq (\beta+\delta)+1=\beta+(\delta+1)
$$

이다. 마지막으로 극한 $\eta$에 대하여 $\delta<\eta$가 모두 해당 식을 만족시킨다면,

$$
\alpha+\eta=\mathrm{sup}\\{\alpha+\delta:\delta<\eta\\}\subset \\{\beta+\delta:\delta<\eta\\}=\beta+\eta
$$

이므로 $\eta$ 또한 해당 식을 만족시킨다.

2. 와 3. 도 이와 같다. $\square$

## 2.11.
> 다음을 만족하는 $\alpha, \beta, \gamma$를 찾으시오.

1. $\alpha<\beta$이고 $\alpha+\gamma=\beta+\gamma$
2. $\alpha<\beta$이고 $\alpha\cdot \gamma=\beta\cdot \gamma$
3. $\alpha<\beta$이고 $\alpha^\gamma=\beta^\gamma$

### 풀이.

1. $0<1$이고 $0+\omega=1+\omega$이다.

2. $1<2$이고 $1\cdot \omega=2\cdot \omega$이다.

3. $2<3$이고 $2^\omega=3^\omega$이다.

$\square$

## 2.12.
> $\alpha_0=\omega$이고 $\alpha_{n+1}=\omega^{\alpha_n}$으로 정의할 때, $\epsilon_0=\lim_{n\rightarrow \omega}\alpha_n$이라 하자. $\epsilon_0$가 $\omega^\epsilon=\epsilon$을 만족하는 가장 작은 서수임을 보이시오.

### 풀이.
먼저,

$$
\epsilon_0=\mathrm{sup} \{\omega, \omega^\omega, \omega^{\omega^\omega},\cdots \} = \omega^{\mathrm{sup}\{\omega, \omega^\omega, \omega^{\omega^\omega},\cdots\}}=\omega^{\epsilon_0}
$$

이다. $\epsilon<\epsilon_0$가 $\omega^\epsilon=\epsilon$을 만족시킨다 하자. $\epsilon<\epsilon_0$이므로 $\alpha_{n}<\epsilon<\alpha_{n+1}$인 $n$이 존재하고, $\alpha_{n+1}=e^{\alpha_{n}} < e^{\epsilon} = \epsilon$이므로 모순이다. $\square$

## 2.13.
> 극한 서수 $\gamma>0$이 분해 불가능<sup>indecomposable</sup>함과, 모든 $\alpha<\gamma$에 대하여 $\alpha+\gamma=\gamma$임과, 어떤 $\alpha$에 대하여 $\gamma=\omega^\alpha$임이 동치이다.

### 풀이
$\gamma$가 분해 불가능하다고 하자. 모든 $\alpha<\gamma$에 대하여 $\delta_\alpha$가 존재하여 $\alpha+\delta_\alpha=\gamma$이다. $\delta_\alpha<\gamma$이면 $\gamma$는 분해 가능하고, $\delta_\alpha>\gamma$이면 $\alpha+\delta_\alpha>\gamma$이므로, $\delta_\alpha=\gamma$이다. 반대로 모든 $\alpha<\gamma$에 대하여 $\alpha+\gamma=\gamma$라면 $\alpha+\delta=\gamma$인 $\delta$의 유일성에 의하여 $\gamma$는 분해 불가능하다.

$\gamma$가 분해 불가능하다고 하자. $\beta$가 $\omega^\beta\leq \gamma$를 만족하는 가장 큰 서수라고 하면, $\gamma=\omega^\beta\cdot \alpha+\delta$인 $\alpha\in \mathbb{N}$와 $\delta<\gamma$가 유일하게 존재한다. 따라서 $\omega^\beta\cdot \alpha=\gamma$이고, 만약 $\alpha>1$이면 $\gamma=\omega^\beta\cdot (\alpha-1)+\omega^\beta\cdot \alpha$이므로, $\alpha=1$이다. 반대로 $\gamma=\omega^{\alpha}$라 하자. $\beta, \delta<\gamma$에 대하여 $\beta+\delta=\gamma$라면, 위와 같은 방법으로 $\beta=e^{\alpha_\beta}\cdot n_\beta+\rho_\beta$이고 $\delta=e^{\alpha_\delta}\cdot n_\delta+\rho_\delta$라고 쓰자. 그러면 $\beta< e^{\alpha_\beta} \cdot (n_\beta+1) $, $\gamma< e^{\alpha_\gamma} \cdot (n_\gamma+1)$이고, 따라서 어떤 $\alpha'<\alpha , n$에 대하여 $\beta,\gamma<\omega^{\alpha '}\cdot n$이다. 따라서 $\beta+\gamma<\omega^{\alpha'}\cdot (n+n)<\omega^\alpha$이므로 모순이다. $\square$


## 2.14. 
> $E$가 $P$ 위에서 잘 받혀진 관계<sup>well-founded relation</sup>[^1]일 때, $a_1\,E\, a_0, a_2 \,E\, a_1, a_3 \,E\, a_2, \cdots$를 만족하는 순열 $\langle a_n:n\in \mathbb{N}\rangle$은 존재하지 않는다.

[^1]: 대한수학회의 [수학용어사전](http://www.kms.or.kr/mathdict/list.html)에서는 well-founded relation의 번역어를 제시하지 않고 있다. 위키백과의 [well-founded relation](https://en.wikipedia.org/wiki/Well-founded_relation) 항목은 한국어로 [정초 관계](https://ko.wikipedia.org/wiki/%EC%A0%95%EC%B4%88_%EA%B4%80%EA%B3%84)로 작성되어 있고, 이는 일본어 항목 [整礎関係](https://ja.wikipedia.org/wiki/%E6%95%B4%E7%A4%8E%E9%96%A2%E4%BF%82)를 직역한 것으로 보인다. 일본에서도 整礎라는 단어는 자주 사용되는 단어가 아니지만, 整과 礎라는 한자는 독립적으로 잘 사용되므로 일본어 화자들에게는 의미를 파악하는 데 무리가 없다. 그러나 한국어 화자가 정초 관계라는 단어를 보았을 때 즉시 그 의미를 파악하기 어렵다고 보았고, 따라서 원래의 의미를 풀어서 사용하는 방향으로 번역하였다.

### 풀이
정의에 따라 집합 $\\{a_n:n\in \mathbb{N}\\}\subset P$의 $E$-최소 원소 $a_m$이 존재한다. 그러나 $a_{m+1} \,E\, a_m$이므로 모순이다. $\square$

## 2.15. 
> $E$가 $P$ 위에서 잘 받혀진 관계라 하고, $G$가 함수라 하자. 그러면 함수 $F$가 존재하여, 모든 $x\in P$에 대하여 $F(x)=G(x,F\upharpoonright \\{ y\in P: y\, E\, x\\})$를 만족한다.

### 풀이
*이 문제는 풀이를 잠시 미루어 둔다.*

---
