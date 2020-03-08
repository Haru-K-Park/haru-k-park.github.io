---
layout: post
title: "뱀 보조정리"
author: "YGLENA"
---
# 정리
**뱀 보조정리<sup>snake Lemma</sup>.** 아벨 범주<sup>Abelian category</sup> $\mathcal{C}$에 대하여 다음 그림이 가환<sup>commutative</sup>이라고 하자.

$$
\require{AMScd}\begin{CD}
  @.  A'  @> > >  B'  @>p> > C' @> > > 0\\
@.      @VfVV       @VgVV      @VhVV       @.\\
0 @> > >  A   @>i> >  B   @> > > C  @. 
\end{CD}
$$

그렇다면 다음이 완전열<sup>exact sequence</sup>이다.

$$
\require{AMScd}\begin{CD}
\textrm{Ker}(f) @> > > \textrm{Ker}(g) @> > > \textrm{Ker}(h) @>\partial> > \textrm{coKer}(f) @> > > \textrm{coKer}(g) @> > > \textrm{coKer}(h)
\end{CD}
$$

# 증명
프레이드-미첼 매장 정리<sup>Freyd-Mitchell embedding theorem</sup>에 의하여, $\mathcal{C}$가 $R-\textrm{mod}$인 경우만을 증명하면 된다. $R-\textrm{mod}$의 경우 그림을 따라가며 증명할 수 있다.

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

1980년 미국 영화 [It's My Turn](https://www.imdb.com/title/tt0080936/)의 도입부에서  [뱀 보조정리의 정확한 증명이 소개되어 있다.](https://www.youtube.com/watch?v=etbcKWEKnvg) 이 영화에서 교수는 뱀 보조정리를 그림을 따라가며 정확하게 증명하고, 학생은 교수의 증명에서 착각하기 쉬운, 그러나 수학적으로 잘못되지 않은 부분을 지적한다. 이 사실은 C. A. Weibel의 [An introduction to homological algebra](https://doi.org/10.1017/CBO9781139644136)에서도 언급된다.
