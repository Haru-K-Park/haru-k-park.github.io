---
layout: post
title: "집합론 풀이 1장"
author: "YGLENA"
comments: true
tags: [Set theory, Problems and solutions]
---
<details><summary>
<span style="font-size:2em;font-family: Helvetica;">**목차**</span>
</summary>
* 목차
{:toc}
</details>
[T. Jech의 Set Theory](https://doi.org/10.1007/3-540-44761-X){:target="_blank"}
## 1.1.
>$(a,b)=(c,d)$임과 $a=c,b=d$임이 동치이다.

### 풀이
정의에 따라 $(a,b)=\\{\\{a\\},\\{a,b\\}\\}$이다. $a=c, b=d$이면 $(a,b)=\\{\\{a\\},\\{a,b\\}\\}=\\{\\{c\\},\\{c,d\\}\\}=(c,d)$이다. $(a,b)=(c,d)$라 하자. $\\{a\\}=\\{c\\}$이고 $\\{a,b\\}=\\{c,d\\}$이면, $a=c$이고 따라서 $b=d$이다.[^1] $\\{a\\}=\\{c,d\\}$이고 $\\{a,b\\}=\\{c\\}$이면, $c=d=a=b$이다. $\square$

[^1]: $a=b$이면 $\\{a\\}=\\{b\\}=\\{c\\}=\\{d\\}$이다. $a\neq b$이면 $a=c$이므로 $b=d$이다.

## 1.2.
>$P(X)\subset X$인 집합 $X$는 존재하지 않는다.

### 풀이
분류 공리꼴<sup>axiom schema of specification</sup>[^2]에 의하여, 다음과 같은 집합이 존재한다.

$$
Y=\{x\in X:x\notin x\}
$$

$Y\subset X$이므로 $Y\in P(X)\subset X$이다. $Y\in Y$이면 $Y\notin Y$이고, $Y\notin Y$이면 $Y\in Y$이므로 모순이다. $\square$

[^2]: 또는 분리 공리꼴<sup>axiom schema of separation</sup>

## 1.3.
>$X$가 귀납적<sup>inductive</sup>이면, $\\{ x \in X : x \subset X \\}$ 또한 귀납적이다. 따라서 $\mathbb{N}$이 추이적<sup>transitive</sup>이고, $n=\\{m\in \mathbb{N}:m<n\\}$이다.

### 풀이
$Y=\\{ x \in X : x \subset X \\}$이라 하자. $X$가 귀납적이므로 $\emptyset\in X$이고, 따라서 $\emptyset\in Y$이다. $x\in Y$라 하자. $x\in X$이고 $X$가 귀납적이므로 $x\cup \\{ x \\}\in X$이고, 또한 $x\subset X$이므로 $x\cup \\{ x \\} \subset X$이다. 따라서 $x \cup \\{ x \\} \in Y$이고 $Y$는 귀납적이다.

$\mathbb{N}$이 모든 귀납적 집합의 교집합이므로, $\\{ n \in \mathbb{N} : n \subset \mathbb{N} \\}=\mathbb{N}$이고, 따라서 $\mathbb{N}$은 추이적이다. 이로 인해 $n\subset \mathbb{N}$이다. 즉, $n= \\{ m \in \mathbb{N} : m \in n \\}$이다. $\square$

## 1.4.
>$X$가 귀납적이면, $\\{x \in X : x \textrm{는 추이적} \\}$ 또한 귀납적이다. 따라서 모든 $n\in \mathbb{N}$은 추이적이다.

### 풀이
$Y=\\{x \in X : x \textrm{는 추이적} \\}$이라 하자. $X$가 귀납적이므로 $\emptyset\in X$이고, $\emptyset$이 추이적임은 공진리<sup>vacuous truth</sup>이므로 $\emptyset\in Y$이다. $x\in Y$라 하자. $x\in X$이고 $X$가 귀납적이므로 $x\cup \\{ x \\} \in X$이다. $y\in x\cup \\{ x \\}$이라 하자. $y\in x$이면, $x$가 추이적이므로, $y\subset x$이고 따라서 $y\subset x\cup \\{ x \\}$이다. $y\in \\{ x \\}$이면 $x=y$이고 따라서 $y\subset x\cup \\{x\\}$이다. 따라서 $Y$는 귀납적이다.

$\mathbb{N}$이 모든 귀납적 집합의 교집합이므로, $\\{n \in \mathbb{N} : n \textrm{은 추이적} \\}=\mathbb{N}$이고, 따라서 $\mathbb{N}$은 추이적이다. $\square$

## 1.5.
>$X$가 귀납적이면, $\\{x \in X : x \textrm{는 추이적이고 } x\notin x\\}$는 귀납적이다. 따라서 모든 $n\in \mathbb{N}$에 대해 $n\notin n$이고 $n\neq n+1$이다.

### 풀이
$Y=\\{x \in X : x \textrm{는 추이적이고 } x\notin x\\}$이라 하자. $X$가 귀납적이므로 $\emptyset\in X$이고, $\emptyset$이 추이적임은 공진리이고 $\emptyset\notin \emptyset$이므로 $\emptyset\in Y$이다. $x\in Y$라 하자. $x\in X$이고 $X$가 귀납적이므로 $x\cup \\{ x \\} \in X$이다. $y\in x\cup \\{ x \\}$이라 하자. $y\in x$이면, $x$가 추이적이므로, $y\subset x$이고 따라서 $y\subset x\cup \\{ x \\}$이다. $y\in \\{ x \\}$이면 $x=y$이고 따라서 $y\subset x\cup \\{x\\}$이다. $x\cup \\{ x \\}\in x\cup \\{ x \\}$이면 $x\cup \\{x\\}=x$이거나 $x\cup \\{x\\} \in x$이고, $x$가 추이적이므로 $x\cup \\{x\\}\subset x$이다. 따라서 $\\{x\\} \subset x$이고 따라서 $x\in x$이다. 이는 $x\notin x$라는 가정에 모순이므로 $Y$는 귀납적이다.

$\mathbb{N}$이 모든 귀납적 집합의 교집합이므로 위를 적용하면 $n\notin n$이다. $n=n+1$이라 하면 $n\cup \\{ n \\} =n$이므로 $\\{ n \\}\subset n$이 되고, 따라서 $n\in n$을 얻어 모순이다. $\square$

## 1.6.
>$X$가 귀납적이라면, $X$의 추이적인 원소들 $x$ 중 모든 비어 있지 않은 $z\subset x$가 $\in$-최소 원소를 가지는 원소들로 이루어진 부분집합은 귀납적이다.

### 풀이
$Y$가 주어진 집합이라 하자. $\emptyset\in Y$임과 $x\in Y$일 때 $x\cap \\{ x \\}$이 추이적임은 위와 같은 논의로 보일 수 있다. 비어 있지 않은 부분집합 $z\subset x\cup \\{ x \\}$에 대하여, $z\cap x\neq \emptyset$이거나 $z\cap x = \emptyset$이다. 첫 번째 경우, $z\cap x$가 $x$의 비어 있지 않은 부분집합이므로 $\in$-최소 원소 $t$를 가진다. $x\notin z$라면 $t$가 $z$의 최소 원소이다. $x\in z$일 때 $x\in t$라 하자. $t\in x$이고 $x$가 추이적이므로 $t\subset x$이고, 따라서 $x\in x$이다. 두 번째 경우에는 $z=\\{x\\}$이어야 하고, $z$가 최소 원소를 가지지 않는다면 마찬가지로 $x\in x$이다. 그러나 이 경우 $\{x\}\subset x$에서 최소 원소가 존재하지 않으므로 모순이다. $\square$

## 1.7.
>모든 비어있지 않은 $X\subset \mathbb{N}$은 $\in$-최소 원소를 가진다.

### 풀이
$\mathbb{N}$이 모든 귀납적 집합의 교집합이므로, [문제 1.6](#16)에 의하여 모든 $n\in \mathbb{N}$에 대하여, 비어 있지 않은 부분집합 $z\subset n$이 $\in$-최소 원소를 가진다. $X\subset \mathbb{N}$에 대해 $n\in X$를 잡는다. $X\cap n=\emptyset$이면, $s\in n$이고 $s\in X$일 수 없으므로 $n$이 $X$의 최소 원소이다. $X\cap n\neq \emptyset$이면 $X\cap n$이 $n$의 비어 있지 않은 부분집합이므로 $\in$-최소 $m\in X\cap n$을 가진다. $n\in m$이면 [문제 1.4](#14)에 의하여 $n\subset m$이고, $m\in n$이므로 $m\in m$이다. 이는 [문제 1.5](#15)에 의해 모순이다. $\square$

## 1.8.
>$X$가 귀납적이라면, $\\{ x\in X:(x=\emptyset)\vee(\exists y(x=y\cup \{y\})) \\}$ 또한 귀납적이다. 따라서 $0$이 아닌 $n$ 은 어떤 $m$에 대해서 $m+1$과 같다.

### 풀이
$Y$를 그러한 집합이라 하자. $x\in Y$라 할 때, $x\neq \emptyset$이라 하자. 그러면 $x\cap \{x\}\in X$이고 조건을 만족시키므로 $x\cap \{x\}\in Y$이다.

$\mathbb{N}$이 모든 귀납적 집합의 교집합이므로, $\mathbb{N}$에 대한 위의 집합은 $\mathbb{N}$이다. 따라서 $n\neq 0$이면 어떤 $m$에 대해서 $n=m+1$이다. $\square$

## 1.9.
> $A\subset \mathbb{N}$이 $0\in A$이고, $n\in A$일 때 $n+1\in A$를 만족시키면, $A=\mathbb{N}$이다.

### 풀이
$A$는 $\mathbb{N}$의 부분집합이면서 귀납적이므로, $A=\mathbb{N}$이다. $\square$

## 1.10.
> $n\in \mathbb{N}$일 때 $n$은 T-유한<sup>T-finite</sup>하다.

### 풀이
T-유한한 $n\in \mathbb{N}$들의 부분집합을 $A$라 하자. $P(0)=\{\emptyset\}$이고, 따라서 $\emptyset$은 $\subset$-극대 원소이므로 $0\in A$이다. $n\in A$라 하자. $X\subset P(n+1)$일 때, 분류 공리에 의하여 집합 $Y=\{x\in X:n\in x\}$이 존재한다. 이것이 공집합이라면 $X\subset P(n)$이고, 따라서 $X$는 $\subset$-극대 원소를 가진다. $Y$가 공집합이 아니라고 하자. 분류 공리에 의하여 공집합이 아닌 집합 $Z=\\{ z\in P(n):z\cup \\{n\\} \in Y \\}$가 존재하고, $Z\subset P(n)$이다. 따라서 $Z$는 $\subset$-극대 원소 $M$을 가진다. $B\in X$에 대하여 $M\cup \\{n\\}\subset B$이라 하면, $n\in B$이므로 $B\in Y$이다. 그러면 $M\subset B-\\{n\\}$이므로 $M\cup \\{n\\}=B$이고, 따라서 $M\cup \\{n\\}$은 $X$의 $\subset$-극대 원소이다. [문제 1.9](#19)에 의하여 $A=\mathbb{N}$이다. $\square$

## 1.11.
> $\mathbb{N}$은 T-무한하다.

### 풀이
$\mathbb{N}\subset P(N)$을 생각하고, $n\in \mathbb{N}$이 $\subset$-극대 원소라고 하자. $n\in n+1$이고 [문제 1.4](#14)에 의하여 $n\subset n+1$이다. [문제 1.5](#15)에 의하여 $n\neq n+1$이고, 이는 모순이다. $\square$

## 1.12.
> 모든 유한집합은 T-유한하다.

### 풀이
집합 $X$가 유한집합이면 n에서 $X$ 위로의 일대일함수 $f$가 존재한다. 이 때 $f^{-1}$ 또한 함수이고, 따라서 치환 공리꼴<sup>axiom of replacement schema</sup>에 의하여 집합의 $f$와 $f^{-1}$에 대한 상<sup>image</sup>은 집합이다. 공집합이 아닌 부분집합 $A\subset P(X)$에 대하여, [문제 1.10](#110)에 의해 $f^{-1}(A)$의 $\subset$-극대 원소 $m$이 존재한다. 어떤 $u\in A$에 대하여 $f(m)\subset u$라 하자. 그러면 $m\subset f^{-1}(u)$이므로 $m=f^{-1}(u)$이고, 따라서 $f(m)=u$이고 $f(m)$은 $A$의 $\subset$-극대 원소이다. $\square$

## 1.13.
> 모든 무한집합은 T-무한<sup>T-infinite</sup>하다.

### 풀이
집합 $S$가 무한집합일 때, 집합 $X=\\{u\subset S:|u|<\infty\\}$을 생각하자. $X$가 $\subset$-극대 원소 $u$를 가진다고 가정하자. $u$가 유한집합이고 $S$가 무한집합이므로, $S-u$는 공집합이 아니다. 따라서 $x\in S-u$를 잡을 수 있고, $u\cup \\{x\\}$는 $X$의 원소이다. $x\notin u$이므로 $u\subset u\cup \\{x\\}$이고 $u\neq u\cup \\{x\\}$이고, 이는 모순이다. $\square$

## 1.14.
> 분리 공리꼴은 치환 공리꼴로부터 유도된다.

### 풀이
논리식 $\phi(u,p)$에 대하여, $p$를 고정하고 다음 함수를 정의하자.

$$
F=\{(x,x):\phi(x,p)\}
$$

$(x,y)\in F$이고 $(x,z)\in F$이면, $x=y$이고 $x=z$이므로 $y=z$이다. 따라서 이는 함수이다. 치환 공리꼴에서 $F(X)$는 집합이다. $F(X)$의 정의상

$$
F(X)=\{x\in X: \phi(x,p)\}
$$
이므로 분리 공리꼴이 성립한다. $\square$

## 1.15.
> 합집합 공리, 멱집합 공리, 치환 공리꼴 대신 다음 약화된 공리들을 생각하자.
>- $\forall X \, \exists Y \, \bigcup X\subset Y$
>- $\forall X \, \exists Y \, P(X) \subset Y$
>- 모임 $F$가 함수일 때, $\forall X\, \exists Y\, F(X)\subset Y$
>
>그러면 이들과 분리 공리꼴을 이용하여 합집합 공리, 멱집합 공리, 치환 공리꼴을 각각 증명할 수 있다.

### 풀이
각각의 공리들이 부분 집합으로서의 존재성을 보증하고 있기 때문에, 분리 공리꼴을 이용하여 이들을 분리해내면 된다. 즉, 각각의 공리들에 대하여,
- $\phi(y)$를 $\exists x\in X. y\in x$로 두고, $\cup X=\\{y\in Y: \phi(y)\\}$로 둔다.
- $\phi(y)$를 $y\subset X$로 두고, $P(X)=\\{y\in Y: \phi(y)\\}$로 둔다.
- $\phi(y)$를 $\exists x\in X. y=F(x)$로 두고, $F(X)=\\{y\in Y: \phi(y)\\}$로 둔다.
$\square$

---
