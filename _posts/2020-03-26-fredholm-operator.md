---
layout: post
title: "프레드홀름 연산자"
author: "YGLENA"
comments: true
tags: [Functional analysis]
---
* 
{:toc}
## 콤팩트 연산자
바나흐 공간<sup>Banach space</sup> $E,F$와 유계 연산자 $T\in \mathcal{L}(E,F)$에 대하여, $\overline{T(B_E)}$가 $F$의 강한 위상<sup>strong topology</sup> 하에서 콤팩트<sup>compact</sup>할 때, $T$를 **콤팩트 연산자<sup>compact operator</sup>**라 한다. $B_E$는 $E$의 단위 공<sup>unit ball</sup>이다. $E$에서 $F$로 가는 콤팩트 연산자들의 집합을 $\mathcal{K}(E,F)$라 쓴다.

### 성질
>바나흐 공간 $E,F$와 $T\in \mathcal{L}(E,F)$에 대하여, 다음이 동치이다.
>1. $T$는 콤팩트 연산자이다.
>2. 모든 유계 부분 집합 $B\subset E$에 대하여, $\overline{T(B)}$는 $F$의 강한 위상 하에서 콤팩트하다.
>3. 열린 $0\in U\subset E$와 콤팩트한 $V\subset Y$가 존재하여 $T(U)\subset V$를 만족시킨다.
>4. $E$ 위의 모든 유계 수열 $\\{x_n \\}$에 대하여, 수열 $\\{Tx_n\\}$은 수렴하는 부분수열을 가진다.
>5. $B\subset E$가 유계 부분집합일 때, $T(E)$는 완전히 유계<sup>totally bounded</sup>이다.

>$\mathcal{L}(E,F)$ 위에서의 거리 위상에 대하여, $\mathcal{K}(E,F)$는 $\mathcal{L}(E,F)$의 닫힌 선형 부분공간이다.

$T\in \mathcal{L}(E,F)$에 대하여, $T$의 상이 유한 차원 공간일 때 $T$는 **유한 계수<sup>finite rank</sup>**를 가진다고 한다.

> 모든 유한 계수 연산자는 콤팩트 연산자이다.

<details><summary>**증명.**
</summary>

$T$가 유계이므로, 유계 집합을 유계 집합으로 보내고, 따라서 하이네-보렐 정리<sup>Heine-Borel theorem</sup>에 의하여 이의 폐포<sup>closure</sup>는 콤팩트하다. $\square$
</details>

> 바나흐 공간 $E,F,G$에 대하여, $T\in \mathcal{L}(E,F)$, $S\in \mathcal{K}(F,G)$이거나 $T\in \mathcal{K}(E,F)$, $S\in \mathcal{L}(F,G)$일 때, $S\circ T\in \mathcal{K}(E,G)$이다.
>>따라서 $\mathcal{K}(E)$는 $\mathcal{L}(E)$의 양쪽 아이디얼<sup>two-sided ideal</sup>이고, 따라서 $\mathcal{K}(E)/\mathcal{L}(E)$는 단순대수<sup>simple algebra</sup>이다. 이를 **칼킨 대수<sup>Calkin algebra</sup>**라 한다.

<details><summary>**증명.**
</summary>

첫 번째 경우, $T$가 유계이므로 $T(B_E)$가 유계이고, 따라서 $\overline{S\circ T(B_E)}$가 콤팩트하다. 두 번째 경우, $\overline{T(B_E)}$가 콤팩트하므로, $\overline{S(\overline{T(B_E)})}=\overline{S\circ T(B_E)}$가 콤팩트하다. $\square$
</details>

>**프레드홀름 대체<sup>Fredholm alternative</sup>.**[^1] $T\in \mathcal{K}(E)$라 하면, 다음이 성립한다.
>1. $\mathrm{Ker}(I-T)$는 유한 차원을 가진다.
>2. $\mathrm{Im}(I-T)$는 닫혀 있고, $\mathrm{Im}(I-T)=\mathrm{Ker}(I-T^*)^{\perp}$이다.
>3. $\mathrm{Ker}(I-T)=\\{0\\}$임과 $\mathrm{Im}(I-T)=E$임이 동치이다.[^2]
>4. $\mathrm{dim}\mathrm{Ker}(I-T)=\mathrm{dim}\mathrm{Ker}(I-T^*)$이다.

[^1]: '대체'라는 이름이 붙은 이유는, 위에서 다음을 유도할 수 있기 때문이다. 다음 둘 중 하나만이 참이다(즉, 하나가 다른 하나를 대체한다): $u-Tu=0$이 $0$이 아닌 $n$개의 선형독립 해를 가지고 $u-Tu=f$가 풀 수 있음이 $f\in N(I-T^*)^{\perp}$임과 동치이거나, $u-Tu=f$가 모든 $f$에 대하여 유일한 해를 가진다.

[^2]: 유한 차원 공간에서 선형 연산자가 전사임과 단사임은 동치이므로, 이는 자명하다. 무한 차원의 경우, $l^2$ 공간에서 왼쪽 및 오른쪽으로 밀어 주는 연산자를 생각하라.

## 프레드홀름 연산자
$A\in \mathcal{L}(E,F)$에 대하여 $\mathrm{Ker}(A)$가 유한 차원을 가지고 $\mathrm{Im}(A)$가 닫혀 있으며 유한 여차원을 가지면, $A$를 **프레드홀름 연산자<sup>Fredholm operator</sup>**라 한다. 프레드홀름 연산자의 지표<sup>index</sup>는 $\mathrm{ind}(A)=\mathrm{dim}\mathrm{Ker}(A)-\mathrm{co}\mathrm{dim}\mathrm{Im}(A)$로 정의된다.

### 성질
> $E$, $F$가 유한하면, 모든 $T\in \mathcal{L}(E,F)$가 프레드홀름 연산자이다.

> $T$가 콤팩트 연산자이면, $I-T$는 프레드홀름 연산자이다.

>프레드홀름 연산자의 집합은 $\mathcal{L}(E,F)$의 열린 부분 집합이고, 지표 함수 $\mathrm{ind}:A\rightarrow \mathrm{ind}A$는 연속함수이다.

>$A\in \mathcal{L}(E,F)$가 프레드홀름 연산자임과, 어떤 $T\in \mathcal{L}(F,E)$에 대하여 $I-T\circ A$와 $I-A\circ T$가 유한 계수를 가짐이 동치이다.

>$A:E\rightarrow F$가 프레드홀름 연산자이고 $T:E\rightarrow F$가 콤팩트 연산자이면, $A+T$는 프레드홀름 연산자이고 $\mathrm{ind}(A+T)=\mathrm{ind} A$이다.
>>따라서, $A\in \mathcal{L}(X)$가 프레드홀름임과 $[A ]$가 칼킨 대수에서 역원을 가짐이 동치이다.

>$A:E\rightarrow F$와 $T:F\rightarrow G$가 프레드홀름 연산자일 때, $T\circ A$는 프레드홀름 연산자이고 $\mathrm{ind}(T\circ A)=\mathrm{ind}(T)+\mathrm{ind}(A)$이다.

---