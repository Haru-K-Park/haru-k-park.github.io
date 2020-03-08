---
layout: post
title: "뱀 보조정리"
author: "YGLENA"
comment: true
---
# 정리
**뱀 보조정리<sup>snake Lemma</sup>.** 아벨 범주<sup>Abelian category</sup> $\mathcal{C}$에 대하여 다음 그림이 가환<sup>commutative</sup>이고 각 가로열들이 완전열<sup>exact sequence</sup>이라 하자.

$$
\require{AMScd}\begin{CD}
  @.  A'  @> > >  B'  @>p> > C' @> > > 0\\
@.      @VfVV       @VgVV      @VhVV       @.\\
0 @> > >  A   @>i> >  B   @> > > C  @. 
\end{CD}
$$

그렇다면 다음이 완전열이다.

$$
\require{AMScd}\begin{CD}
\textrm{Ker}(f) @> > > \textrm{Ker}(g) @> > > \textrm{Ker}(h) @>\partial> > \textrm{coKer}(f) @> > > \textrm{coKer}(g) @> > > \textrm{coKer}(h)
\end{CD}
$$

더 나아가서, $A'\rightarrow B'$이 단사<sup>monic<\sup>이면 $\mathrm{Ker}(f)\rightarrow \mathrm{Ker}(g)$도 단사이고, $B\rightarrow C$가 전사<sup>epic<\sup>이면 $\mathrm{coKer}(g)\rightarrow \mathrm{coKer}(h)$도 전사이다.

# 증명
프레이드-미첼 매장 정리<sup>Freyd-Mitchell embedding theorem</sup>에 의하여, $\mathcal{C}$가 $R-\textrm{mod}$인 경우만을 증명하면 된다. $R-\textrm{mod}$의 경우 그림을 따라가며 증명할 수 있다.

$\partial=i^{-1}\circ g\circ p^{-1}$로 두고, $c'\in \mathrm{Ker}(h)$를 잡는다. $h(c')=0$이므로 $g\circ p^{-1}(c')\in \mathrm{Ker}(B\rightarrow C)=\mathrm{Im}(A\rightarrow B)$이다. $i$가 단사 함수<sup>injective</sup>이므로 $i^{-1}\circ g\circ p^{-1}(c')$은 존재한다. $p(b)=p(b')=c$라 하면, $p(b-b')=0$이므로, $A'\rightarrow B'$가 $a$를 $b-b'$로 보내는 $a\in A'$가 존재한다. 그림의 가환성으로 $f(a)=i^{-1}\circ g(b-b')$임을 알 수 있고, 이는 $\mathrm{coKer}(A)$에서 0이므로 $\partial$은 잘 정의된다.

이제 위의 열이 $\mathrm{Ker}(h)$와 $\mathrm{coKer}(f)$에서 완전열이 됨을 보이면 되고, 이 둘은 쌍대 관계에 있으므로 하나만 증명하면 된다. $c\in \mathrm{Ker}(\partial)$이면 $g\circ p^{-1}(c)=0$이고, $b\in p^{-1}(c)$일 때 $b\in \mathrm{Ker}(g)$이고 $p(b)=c$이므로 $c\in \mathrm{Im}(\mathrm{Ker}(g)\rightarrow \mathrm{Ker}(h))$이다. 반대로 $c\in \mathrm{Im}(\mathrm{Ker}(g)\rightarrow \mathrm{Ker}(h))$이고 $b\in \mathrm{Ker}(g)$가 $p(b)=c$를 만족시킬 때, $i^{-1}\circ g\circ p^{-1}(c)=i^{-1}\circ g(b)=i^{-1}(0)=0$이다.

$A'\rightarrow B'$가 단사이면 $a\mapsto 0$일 때 $a=0$이다. 따라서 $a\in \mathrm{Ker}(f)$일 때 $a\mapsto 0$이 $a=0\in \mathrm{Ker}(f)$를 뜻하므로, $\mathrm{Ker}(f)\rightarrow \mathrm{Ker}(g)$는 단사이다. 남은 하나는 쌍대 관계로 증명된다. $\square$

# 호몰로지 긴 완전열
뱀 보조정리는 사슬 복합체 사이의 짧은 완전열

$$
\require{AMScd}\begin{CD}
0 @> > > A_\bullet @>\alpha> > B_\bullet @>\beta> > C_\bullet @> > > 0
\end{CD}
$$

에 대한 호몰로지 긴 완전열<sup>homology long exact sequence</sup>

$$
\require{AMScd}\begin{CD}
\cdots @> > > H_{n+1}(C) @>\partial> > H_n(A) @>\alpha_{*}> > H_n(B) @>\beta_{*}> > H_n(C) @>\partial> > H_{n-1}(A)@> > > \cdots
\end{CD}
$$

의 존재성을 증명하는 데 사용된다.

# 참고
뱀 보조정리라는 이름은, 얻어진 완전열이 뱀과 같은 모양을 가진다는 점에서 착안하여 이름붙여졌다. 트위터에 업로드한 [다음 그림](https://twitter.com/YGLENA/status/1156595340604108800){:target="_blank"}에서도 확인할 수 있다.

1980년 미국 영화 [It's My Turn](https://www.imdb.com/title/tt0080936/){:target="_blank"}의 도입부에서  [뱀 보조정리의 정확한 증명이 소개되어 있다.](https://www.youtube.com/watch?v=etbcKWEKnvg){:target="_blank"} 이 영화에서 교수는 뱀 보조정리를 그림을 따라가며 정확하게 증명하고, 학생은 교수의 증명에서 착각하기 쉬운, 그러나 수학적으로 잘못되지 않은 부분을 지적한다. 이 사실은 C. A. Weibel의 [An introduction to homological algebra](https://doi.org/10.1017/CBO9781139644136){:target="_blank"}에서도 언급된다.
