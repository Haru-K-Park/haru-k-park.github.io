---
layout: post
title: "뱀 보조정리"
author: "YGLENA"
---
아벨 범주 $\mathcal{C}$에 대하여 다음 그림이 가환이라고 하자.

<div class="commdiag">
$$
\require{AMScd}\begin{CD}
  @.  A'  @> > >  B'  @>p> > C' @> > > 0\\
@.      @VfVV       @VgVV      @VhVV       @.\\
0 @> > >  A   @>i> >  B   @> > > C  @. 
\end{CD}
$$
</div>

그렇다면 다음이 완전열이다.
$$
\textrm{Ker}(f) @> > > \textrm{Ker}(g) @> > > \textrm{Ker}(h) @>\partial> > \textrm{coKer}(f) @> > > \textrm{coKer}(g) @> > > \textrm{coKer}(h)
$$
