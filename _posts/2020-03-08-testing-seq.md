---
layout: post
title: "뱀 보조정리"
author: "YGLENA"
---
# 정리
_뱀 보조정리<sup>snake Lemma</sup>._ 아벨 범주<sup>Abelian category</sup> $\mathcal{C}$에 대하여 다음 그림이 가환<sup>commutative</sup>이라고 하자.<br>
$$
\require{AMScd}\begin{CD}
  @.  A'  @> > >  B'  @>p> > C' @> > > 0\\
@.      @VfVV       @VgVV      @VhVV       @.\\
0 @> > >  A   @>i> >  B   @> > > C  @. 
\end{CD}
$$

그렇다면 다음이 완전열<sup>exact sequence</sup>이다.<br>
$$
\require{AMScd}\begin{CD}
\textrm{Ker}(f) @> > > \textrm{Ker}(g) @> > > \textrm{Ker}(h) @>\partial> > \textrm{coKer}(f) @> > > \textrm{coKer}(g) @> > > \textrm{coKer}(h)
\end{CD}
$$

# 증명
프레이드-미첼 매장 정리<sup>Freyd-Mitchell embedding theorem</sup>에 의하여, $\mathcal{C}$가 $R-\textrm{mod}$인 경우만을 증명하면 된다. $R-\textrm{mod}$의 경우 그림을 따라가며 증명할 수 있다.

# 호몰로지 긴 완전열
뱀 보조정리는 사슬 복합체 사이의 짧은 완전열<br>
$$
\require{AMScd}\begin{CD}
0 @> > > A_\bullet @>\alpha> > B_\bullet @>\beta> > C_\bullet @> > > 0
\end{CD}
$$<br>
에 대한 호몰로지 긴 완전열<sup>homology long exact sequence</sup><br>
$$
\require{AMScd}\begin{CD}
\cdots @> > > H_{n+1}(C) @>\partial> > H_n(A) @>\alpha_{*}> > H_n(B) @>\beta_{*}> > H_n(C) @>\partial> > H_{n-1}(A)@> > > \cdots
\end{CD}
$$<br>
의 존재성을 증명하는 데 사용된다.
