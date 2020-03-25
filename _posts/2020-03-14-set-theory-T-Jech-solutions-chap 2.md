---
layout: post
title: "집합론 풀이 2장"
author: "YGLENA"
comments: true
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

$1\Rightarrow 2$. 귀납 집합이 존재하면, 귀납 집합들의 교집합이 공집합이 아니다. $n$은 귀납 집합이 아니기 때문에 이 교집합은 어떤 $n$과 동치가 아니고, 따라서 
$\square$

---
