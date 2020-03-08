---
layout: post
title: "호몰로지 긴 완전열"
author: "YGLENA"
comment: true
---
# 정리
**호몰로지 긴 완전열<sup>Homology long exact sequence</sup>.** 아벨 범주<sup>Abelian category</sup> $\mathcal{C}$와 그 위의 사슬 복합체 범주 $\mathrm{Ch}_\bullet(\mathcal{C})$를 생각하자ㅣ. 사슬 복합체 사이의 짧은 완전열

$$
\require{AMScd}\begin{CD}
0 @> > > A_\bullet @>f> > B_\bullet @>g> > C_\bullet @> > > 0
\end{CD}
$$

에 대하여, 다음이 긴 완전열이다.

$$
\require{AMScd}\begin{CD}
\cdots @> > > H_{n+1}(C) @>\partial> > H_n(A) @>f_{*}> > H_n(B) @>g_{*}> > H_n(C) @>\partial> > H_{n-1}(A)@> > > \cdots
\end{CD}
$$

# 증명
[뱀 보조정리](https://yglena.github.io/2020-03-08/snake-lemma)를 이용한다. 사슬 복합체 사이의 짧은 완전열에서 다음 그림을 그릴 수 있다.

$$
\require{AMScd}\begin{CD}
0  @> > >  A_{n+1}  @> > >  B_{n+1}  @> > > C_{n+1} @> > > 0\\
@.      @Vd^A_{n+1}VV       @Vd^B_{n+1}VV      @Vd^C_{n+1}VV       @.\\
0  @> > >  A_n  @> > >  B_n  @> > > C_n @> > > 0\\
@.      @Vd^A_{n}VV       @Vd^B_nVV      @Vd^C_nVV       @.\\
0 @> > >  A_{n-1}   @> > >  B_{n-1}   @> > > C_{n-1}  @> > > 0 
\end{CD}
$$

여기에 뱀 보조정리를 두 번 적용하면, 다음 그림에서 가로열이 모두 완전열임을 알 수 있다.


$$
\require{AMScd}\begin{CD}
  @.  \mathrm{coKer}(d^A_{n+1})  @> > >  \mathrm{coKer}(d^B_{n+1})  @> > > \mathrm{coKer}(d^C_{n+1}) @> > > 0\\
@.      @Vd_AVV       @Vd_BVV      @Vd_CVV       @.\\
0 @> > >  \mathrm{Ima}(d^A_{n})   @> > >  \mathrm{Ima}(d^B_{n})   @> > > \mathrm{Ima}(d^C_{n})  @.
\end{CD}
$$
