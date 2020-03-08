---
layout: post
title: "호몰로지 긴 완전열"
author: "YGLENA"
comment: true
---
# 정리
**호몰로지 긴 완전열<sup>Homology long exact sequence</sup>.** 아벨 범주<sup>Abelian category</sup> $\mathcal{C}$와 그 위의 사슬 복합체 범주 $\mathrm{Ch}_\bullet(\mathcal{C})$를 생각하자. 사슬 복합체 사이의 짧은 완전열

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
[뱀 보조정리<sup>snake Lemma</sup>](https://yglena.github.io/2020-03-08/snake-lemma)와 프레이드-미첼 매장 정리<sup>Freyd-Mitchell embedding theorem</sup>를 이용한다. $R-\mathrm{mod}$ 위의 사슬 복합체 사이의 짧은 완전열에서 다음 그림을 그릴 수 있다.

$$
\require{AMScd}\begin{CD}
0  @> > >  A_{n+1}  @> > >  B_{n+1}  @> > > C_{n+1} @> > > 0\\
@.      @VdVV       @VdVV      @VdVV       @.\\
0  @> > >  A_n  @> > >  B_n  @> > > C_n @> > > 0\\
@.      @VdVV       @VdVV      @VdVV       @.\\
0 @> > >  A_{n-1}   @> > >  B_{n-1}   @> > > C_{n-1}  @> > > 0 
\end{CD}
$$

여기에 뱀 보조정리를 두 번 적용하면, 다음 그림에서 가로열이 모두 완전열임을 알 수 있다.

$$
\require{AMScd}\begin{CD}
  @.  A_n/d(A_{n+1})  @> > >  B_n/d(B_{n+1})  @> > > C_n/d(C_{n+1}) @> > > 0\\
@.      @VdVV       @VdVV      @VdVV       @.\\
0 @> > >  d(A_{n})   @> > >  d(B_{n})   @> > > d(C_{n})  @.
\end{CD}
$$

$d:A_n/d(A_{n+1})\rightarrow Z_{n-1}(A)$의 핵<sup>kernel</sup>이 $Z_n/B_n=H_n(A)$이고 여핵<sup>cokernel</sup>이 $Z_{n-1}/B_{n-1}=H_{n-1}(A)$이므로, 뱀 보조정리를 다시 적용하면 명시된 긴 완전열을 얻는다. \square

# 코호몰로지
주어진 증명에 쌍대를 취하면, 주어진 공사슬 복합체<sup>cochain complex</sup> 사이의 짧은 완전열

$$
\require{AMScd}\begin{CD}
0 @> > > A_\bullet @>f> > B_\bullet @>g> > C_\bullet @> > > 0
\end{CD}
$$

에 대하여, 다음이 긴 완전열임을 알 수 있다.

$$
\require{AMScd}\begin{CD}
\cdots @> > > H^{n-1}(C) @>\partial> > H^n(A) @>f_{*}> > H^n(B) @>g_{*}> > H^n(C) @>\partial> > H^{n+1}(A)@> > > \cdots
\end{CD}
$$

# 마이어-비토리스 열
호몰로지 긴 완전열을 이용하면 공간 $X$의 호몰로지 군을 더 작은 공간 $A,B$와 그 교집합 $A\cap B$의 호몰로지 군으로 나타낼 수 있다. 즉, $A,B$가 $X$의 부분 공간이고, $A,B$의 내부<sup>interior</sup>가 $X$를 덮을 때, 다음이 긴 완전열이다.

$$
\require{AMScd}\begin{CD}
\cdots @> > > H_{n+1}(X) @>\partial> > H_n(A\cap B) @>(i_{*},j_*)> > H_n(A)\oplus H_n(B) @>k_*-l_*> > H_n(X) @>\partial> >\cdots
\end{CD}
$$

여기서 $i:A\cap B\hookrightarrow A$, $j:A\cap B\hookrightarrow B$, $k:A\hookrightarrow X$, $l:B\hookrightarrow X$이다. 이 긴 완전열을 마이어-비토리스 열<sup>Mayer-Vietoris sequence</sup>라 한다.
 
$A\cap B$가 경로 연결 공간일 때, 마이어-비토리스 열에서 $H_1(X)\simeq H_1(A)\oplus H_1(B)/\mathrm{Im}(i,j)_*$를 얻는다. 이는 자이페르트-반 캄펀 정리<sup>Seifert-van Kampen theorem</sup>의 아벨화로 볼 수 있다.
