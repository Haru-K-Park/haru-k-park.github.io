---
layout: post
title: "집합론 풀이 1장"
author: "YGLENA"
comments: true
---
# 문제 출처
[T. Jech의 Set Theory](https://dio.org/10.1007/3-540-44761-X){:target="_blank"}
## 1.1.
$(a,b)=(c,d)$임과 $a=c,b=d$임이 동치임을 보이시오.
### 풀이
정의에 따라 $(a,b)=\\{\\{a\\},\\{a,b\\}\\}$이다. $a=c, b=d$이면 $(a,b)=\\{\\{a\\},\\{a,b\\}\\}=\\{\\{c\\},\\{c,d\\}\\}=(c,d)$이다. $(a,b)=(c,d)$라 하자. $\\{a\\}=\\{c\\}$이고 $\\{a,b\\}=\\{c,d\\}$이면, $a=c$이고 따라서 $b=d$이다.[^1] $\\{a\\}=\\{c,d\\}$이고 $\\{a,b\\}=\\{c\\}$이면, $c=d=a=b$이다. $\square$

[^1]: $a=b$이면 $\\{a\\}=\\{b\\}=\\{c\\}=\\{d\\}$이다. $a\neq b$이면 $a=c$이므로 $b=d$이다.

## 1.2.
$P(X)\subset X$인 집합 $X$는 존재하지 않는다.
### 풀이
분류 공리<sup>separation schema</sup>[^2]에 의하여, 다음과 같은 집합이 존재한다.

$$
Y=\{x\in X:x\notin x\}
$$

$Y\subset X$이므로 $Y\in P(X)\subset X$이다. $Y\in Y$이면 $Y\notin Y$이고, $Y\notin Y$이면 $Y\in Y$이므로 모순이다. \square

[^2]: 또는 분리 공리<sup>separation axiom</sup>

## 1.3.
$X$가 귀납적<sup>inductive</sup>이면, $\{x\in X : x\subset X \}$가 귀납적이다. 따라서 $\mathbb{N}$이 귀납적이고, $n=\\{m\in \mathbb{N}:m<n\\}$이다.
