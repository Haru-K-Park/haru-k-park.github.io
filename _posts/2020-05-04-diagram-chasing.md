---
layout: post
title: "그림 따라가기"
author: "YGLENA"
comments: true
tags: [Homological algebra]
---
* 
{:toc}
## 개요
임의의 작은 아벨 범주<sup>small abelian category</sup> $\mathsf{A}$에 대하여, 프레이드-미첼 매장 정리<sup>Freyd-Mitchell embedding theorem</sup>는 어떤 환<sup>ring</sup> $R$이 존재하여 충실충만<sup>fully faithful</sup>하고 완전<sup>exact</sup>한 함자<sup>functor</sup> $F:\mathsf{A}\rightarrow R-\mathsf{Mod}$가 존재함을 보여 준다. 따라서 많은 경우 아벨 범주를 $R$-모듈이라고 가정하여 그 사상<sup>morphism</sup>이 대상<sup>object</sup>의 원소<sup>element</sup>들에 대하여 정의된다고 생각할 수 있다.

예를 들어, 사상 $f:M\rightarrow N$가 단사 사상<sup>monomorphism</sup>이라면, $R-\mathsf{Mod}$에서 $f$는 단사 함수<sup>surjective</sup>이므로, 어떤 원소 $m\in M$에 대하여 $m=0$이다. 또 $f$가 전사 사상<sup>epimorphism</sup>이라면 모든 $n\in N$에 대하여 $f(m)=n$인 $m$이 존재한다. 이와 같이 일반적인 아벨 범주에서 허용되지 않는 원소의 존재성을 가정하면 가환 그림<sup>commutative diagram</sup>을 따라가며 주어진 원소가 어떻게 변화하는지만 관찰함으로써 다양한 논의를 생략할 수 있다.

그러나 이러한 논의의 생략은 프레이드-미첼 매장 정리를 이용하지 않고 전단사 사상의 정의에 따른 성질만으로도 가능하고, 이러한 성질들을 기본으로 마찬가지로 가환 그림을 따라가며 논리를 전개할 수 있다. 이 과정에서 모듈의 원소 개념과 사상의 동일성 개념이 임의의 아벨 범주에서 성립하도록 조금 바뀌어 등장하게 된다.

## 기본 규칙
아벨 범주 $\mathsf{A}$에서, 대상 $a$를 공역<sup>codomain</sup>으로 하는 사상 $f:x\rightarrow a$를 $a$의 **구성원<sup>member</sup>**이라 하고, $f\in a$라 쓴다. $a$의 구성원 $x,y$에 대하여, 어떤 단사 사상 $u,v$가 존재하여 $x\circ u=y\circ v$일 때, $x\equiv y$라 한다.

> $\equiv$는 동치 관계이다.
<details><summary>**증명.**
</summary>

$x\equiv x$임과 $x\equiv y\Leftrightarrow y\equiv x$임은 자명하다. $x\equiv y\equiv z$이라 하자. 곧, 단사 사상 $u,v,w,r$이 존재하여 $x\circ u=y\circ v$이고 $y\circ w=z\circ r$임을 만족한다 하자. 그러면 다음 그림을 생각할 수 있다.

$$
\require{AMScd}\begin{CD}
  \bullet  @> w'> >  \bullet  @>u> > \bullet\\
    @Vv'VV       @VvVV      @VxVV       \\
\bullet @>w> >  \bullet   @>y> >  a\\
@VrVV   @VyVV @.\\
 \bullet @>z>> a @.
\end{CD}
$$

여기서 $v',w'$는 $v,w$의 당김<sup>pullback</sup>이다. 단사 사상의 당김은 단사 사상이고, 두 단사 사상의 합성은 단사 사상이므로, $x\equiv z$이다. $\square$
</details>

> 아벨 범주 $\mathsf{A}$에서, **그림을 따라갈 때<sup>chasing diagram</sup>** 다음 성질들이 성립한다.
>1. $f:a\rightarrow b$가 전사 사상임과 $f\circ x\equiv 0$인 모든 $x\in a$에 대하여 $x\equiv 0$임이 동치이다.
>2. $f:a\rightarrow b$가 전사 사상임과 $f\circ x\equiv f\circ x'$인 모든 $x,x'\in a$에 대하여 $x\equiv x'$임이 동치이다.
>3. $g:b\rightarrow c$가 단사 사상임과 모든 $z\in c$에 대하여 $y\in b$가 존재하여 $g\circ y\equiv z$임이 동치이다.
>4. $h:r\rightarrow s$가 영사상<sup>zero morphism</sup>임과 모든 $x\in r$에 대하여 $h\circ x\equiv 0$임이 동치이다.
>5. $a\xrightarrow{f} b\xrightarrow{g} c$가 완전<sup>exact</sup>함과 $g\circ f=0$이고 $g\circ y\equiv 0$인 모든 $y\in b$에 대하여 $x\in a$가 존재하여 $f\circ x\equiv y$임이 동치이다.
>6. 주어진 $g:b\rightarrow c$와 $g\circ x\equiv g\circ y$를 만족하는 $x,y\in b$에 대하여, $z\in b$가 존재하여 $g\circ z\equiv 0$이다. 또한, $f:b\rightarrow d$에 대해서 $f\circ x\equiv 0$이면 $f\circ y\equiv f\circ z$이고, $h:b\rightarrow a$에 대해서 $h\circ y\equiv 0$이면 $h\circ x\equiv -h\circ z$이다.
<details><summary>**증명.**
</summary>

1. $f\circ x\equiv 0$이면 어떤 단사 사상 $u$가 존재하여 $f\circ x\circ u=0$이다. $f$가 전사 사상이므로 $x\circ u=0$이고, 따라서 $x\equiv 0$이다.
2. $f\circ x\equiv f\circ x'$이면 어떤 단사 사상 $u,v$가 존재하여 $f\circ x\circ u=f\circ x'\circ v$이다. $f$가 전사 사상이므로 $x\circ u=x'\circ v$이고, 따라서 $x\equiv x'$이다.
3. $g$가 단사 사상이면, $g,z$를 당겨서 $u\in c, y\in b$를 얻을 수 있다. 이 때 $g\circ y=z\circ u$이다. $u$는 단사 사상의 당김이므로 단사 사상이고, 따라서 $g\circ y\equiv z$이다.
4. $h$가 영사상이면 $h\circ x=0$이다. $h\circ x\equiv 0$이면 어떤 단사 사상 $u$가 존재하여 $h\circ x\circ u=0$이고, $u$가 단사 사상이므로 $h\circ x=0$이다. 영사상의 정의에 의하여 $h=0$이다.
5. 주어진 열이 완전열이라 하자. $f$의 상<sup>image</sup>을 통한 분해 $f=m\circ e$를 생각할 때 $m=\ker g$이다. $g\circ y\equiv 0$일 때 $g\circ y=0$이고, 따라서 $y=m\circ y_1$인 $y_1$이 존재한다. $y_1$과 $e$의 공역이 같으므로 이 둘을 당긴 $y_1'$과 $e'$을 생각할 수 있다. 그러면 $y\circ e'=m\circ e\circ y_1'=f\circ y_1'$이고 $e'$가 단사 사상이므로 $y\equiv f y_1$이다.<br>
    거꾸로 모든 $y\in b$에 대하여 주어진 성질을 만족한다고 하자. $k=\ker g\in b$이고 $g\circ k\equiv 0$이므로 $f\circ x\equiv k$인 $x\in a$가 존지한다. 즉, $k\circ u=m\circ e\circ x\circ v$가 되도록 하는 단사 사상 $u,v$가 존재한다. $m\circ e\circ x\circ v\circ \ker (k\circ u)=0$이고 $m$이 전사 사상이므로 $e\circ x\circ v\circ \ker (k\circ u)=0$이고, 따라서 $e\circ x\circ v$는 $t\circ u$로 표현된다. 따라서 $k\circ u=m\circ t\circ u$이고, $u$가 단사 사상이므로 $k=m\circ t$이다. 또한 $g\circ f=0$이므로 $g\circ m=0$이고, 따라서 $m=k\circ s$이다. 즉 $m=m\circ t\circ s$이고 $k=k\circ s\circ t$임을 얻는다. $m,k$가 전사 사상이므로 $t\circ s$와 $s\circ t$는 $1$이고, 따라서 주어진 열은 완전열이다.
6. $g\circ x\equiv g\circ y$임은 $g\circ x\circ u=g\circ y\circ v$인 단사 사상 $u,v$가 존재함을 말한다. $z=y\circ v-x\circ u$로 두면 $g\circ z=0$이다. 또한 $f\circ x\equiv 0$이면 $f\circ z=f\circ y\circ v$이고, $h\circ y\equiv 0$이면 $f\circ z=-f\circ x\circ u$이다.

$\square$
</details>

## 사용
가환 그림 상에서의 많은 정리들을 그림을 따라가며 증명할 수 있다. 대표적인 예시로 [뱀 보조정리<sup>snake Lemma</sup>](https://yglena.github.io/2020-03-08/snake-lemma)와 5-보조정리가 있다.

## 참고문헌
Saunders Mac Lane의 [Categories for the Working Mathematician](https://www.springer.com/gp/book/9780387984032) p.202-205를 참고하였다.