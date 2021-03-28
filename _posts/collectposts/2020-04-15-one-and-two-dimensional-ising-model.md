---
layout: post
title: "1차원과 2차원 정사각 이징 모형"
author: "YGLENA"
comments: true
---
* 
{:toc}
이 글은 재학 중인 학교의 학술 동아리회에 투고한 글을, 가독성을 높이고 그림을 집어 넣은 뒤 난해하고 재미 없는 유머를 삭제한 것이다.
## 에른스트 이징과 이징 모형
Ernst Ising을 어떻게 읽을 것이냐는 문제는 많은 물리학도의 이징 모형에 대한 깊은 이해를 방해했다. 수학의 James Munkres처럼 발음을 어떻게 해야 할지 원어민도 감을 못 잡는 경우는 아니고, 단순히 Ising이 독일어로는 이징으로 발음되지만 영어로는 아이싱으로 발음된다는 것에서 비롯된 혼동이다. 아무도 스위스인 Euler를 율러라고 읽지 않고, 아무도 오스트리아인 Schrodinger를 스크로딩어로 읽지 않으므로, 독일인 Ising은 이징으로 읽는 것이 옳겠다.[^1]

[^1]:한국물리학회 또한 물리학용어집에서 Ising model을 이징 모형으로 번역하도록 권고하고 있다.

이징 모형은 이징의 박사 논문에서 제시된 모형이다. 이징의 지도 교수였던 빌헬름 렌츠는 1922년 이징에게 '위와 아래 두 가지 상태만을 가지고 가장 가까운 이웃과 상호작용하는 자기 모멘트의 체인'을 모형으로써 제시하였고, 이징은 1924년 이 모형을 풀어낸 결과를 박사논문에서 제시하였다. 이징은 이 논문에서 유한한 온도에서 1차원 이징 모형은 상전이가 발생하지 않음을 보였고, 이를 통해 임의의 차원의 이징 모형에서는 상전이가 발생하지 않을 것이라고 추측했다.

그러나 귀납 추론은 증명 앞에서 무너지기 마련이다. 1944년 온사거[^2]는 2차원 이징 모형의 정확한 해를 제시하며 상전이가 발생함을 보였다. 3차원 이상의 경우에는 아직 해가 제시되지 않았고, 평면이 아닌 유한한 이징 모형에서 각 상호작용 항의 계수가 $\{-J,0,J\}$ 중에서 무작위로 정해질 때, 이 계의 바닥 상태를 구하는 문제는 NP-완전하다는 것이 알려져 있다.[^3] 이 명제가 3차원 이상의 경우에 해를 제시할 수 없음을 의미하지는 않지만, 3차원 이징 모형을 풀기는 아직 요원하다는 사실을 알려주고 있다.

[^2]:Lars Onsager, 노르웨이의 물리학자. 노르웨이어 발음은 '온사게르'에 가까우나 한국물리학회의 물리학용어집에서는 '온사거'를 권장하고 있다.

[^3]: [Istrail, S. (2000, May). Statistical mechanics, three-dimensionality and NP-completeness: I. Universality of intracatability for the partition function of the Ising model across non-planar surfaces. In Proceedings of the thirty-second annual ACM symposium on Theory of computing (pp. 87-96).](https://dl.acm.org/doi/pdf/10.1145/335305.335316)

박사 학위를 얻은 뒤 이징은 특허청에서 근무하였지만, 곧 자신이 학생을 가르치는 것을 더 좋아한다는 사실을 깨달았다. 1927년부터 이징은 기숙학교에서 근무하였고, 1930년에는 경제학자 요한나 에머와 결혼하였다. 그리고 1933년, 바이마르 공화국에서 수권법이 가결되었다. 유대인이었던 이징은 직업을 잃었고, 1934년 유대인 학교의 교사직을 다시 얻었지만, 1938년 나치에 의해 학교가 파괴되었다. 1939년 1월 27일 게슈타포가 그를 네 시간동안 심문하였고, 이징이 독일을 떠난다는 약속을 한 뒤에 풀려났다. 이징은 룩셈부르크를 통하여 미국으로 망명하고자 했으나 이징의 40번째 생일 독일군이 룩셈부르크를 점령하여 미 영사관의 문을 닫았다. 독일은 유대인의 강제퇴거를 준비하였으나 이는 독일인과 결혼한 유대인에는 해당하지 않았고, 이에 따라 이징과 36쌍의 유대인-독일인 남-녀 커플은 독일군을 위해 일하는 대신 룩셈부르크에 머물렀고, 전쟁이 끝날 때까지 살아남을 수 있었다. 이징은 1947년 4월 미국으로 가족과 함께 이민하였고, 보스턴에서 열린 물리학 컨벤션에 참가한 뒤, "당신이 이징 모형의 그 '이징'이냐"는 질문을 처음 듣게 되었다.[^4] [^5]

[^4]: [Kobe, S. (2000). Ernst Ising 1900-1998. Brazilian Journal of Physics, 30(4), 649-654.](http://www.scielo.br/scielo.php?pid=S0103-97332000000400003&script=sci_arttext)
[^5]: [Ising, T., Folk, R., Kenna, R., Berche, B., & Holovatch, Y. (2017). The fate of ernst ising and the fate of his model. arXiv preprint arXiv:1706.01764.](https://arxiv.org/abs/1706.01764)

에른스트 이징은 이후 여러 대학의 교수로 재직했지만 어떤 논문도 작성하지 않고, 1998년, 98세의 생일 하루 뒤 숨을 거두었다.

## 1차원 이징 모형
1차원 이징 모형의 해밀토니안은 다음과 같이 쓰여진다.

$$
H=-J\sum_{i=1}^N \sigma_i \sigma_{i+1} - h\sum_{i=1}^N \sigma_i
$$

여기서 $\sigma_i$는 쌍극자의 방향을 나타내는 변수로 그 값으로 $\pm 1$을 가진다. 또한, 우리는 주기성 $\sigma_i = \sigma_{i+N}$을 가정한다. 온도 $T$에서 우리는 다음과 같은 분배 함수를 얻는다.

$$
\begin{split}
Z(N,h,T)&=\sum_{\sigma_1}\cdots\sum_{\sigma_N} e^{\beta (J\sum_{i=1}^N \sigma_i \sigma_{i+1} + h\sum_{i=1}^N \sigma_i)}\\
&=\sum_{\sigma_1}\cdots\sum_{\sigma_N} \prod_{i}e^{\beta (J \sigma_i \sigma_{i+1} + h \sigma_i)}
\end{split}
$$

그런데 우리는 해밀토니안을 다음과 같이 적절히 변형할 수 있다.

$$
H=-J\sum_{i=1}^N \sigma_i \sigma_{i+1} - \frac{h}{2}\sum_{i=1}^N (\sigma_i+\sigma_{i+1})
$$

따라서,

$$
Z(N,h,T)=\sum_{\sigma_1}\cdots\sum_{\sigma_N} \prod_{i}e^{\beta (J \sigma_i \sigma_{i+1} + \frac{h}{2} (\sigma_i+\sigma_{i+1}))}
$$

눈여겨볼 점은, 분배 함수의 뒷부분을 다음과 같이 나타낼 수 있다는 점이다.

$$
e^{\beta (J \sigma_i \sigma_{i+1} + \frac{h}{2} (\sigma_i+\sigma_{i+1}))}=\langle \sigma_i|P|\sigma_{i+1}\rangle
$$

여기서, $P$는 $1,-1$값을 기저로 했을 때,

$$
P=
  \begin{bmatrix}
    e^{\beta (J+h)} & e^{-\beta J} \\
    e^{-\beta J} & e^{\beta(J-h)}
  \end{bmatrix}
$$

로 나타내지는 행렬이다. 따라서,

$$
Z(N,h,T)=\sum_{\sigma_1}\cdots\sum_{\sigma_N} \prod_{i}\langle \sigma_i|P|\sigma_{i+1}\rangle
$$

풀어서 쓰면,

$$
Z(N,h,T)=\sum_{\sigma_1}\cdots\sum_{\sigma_N} \langle \sigma_1|P|\sigma_{2}\rangle\langle \sigma_2|P|\sigma_{3}\rangle\cdots\langle \sigma_N|P|\sigma_{1}\rangle=\sum_{\sigma_1}\langle \sigma_1|P^N|\sigma_1\rangle=\textrm{Tr}{P^N}
$$

그런데 $P$는 대각화가 가능하고, 그 대각값은 

$$
\lambda_{\pm}=e^{\beta J}\cosh(\beta h)\pm \sqrt{e^{2\beta J}\sinh^2(\beta h)+e^{-2\beta J}}
$$

이다. 따라서,

$$
Z(N,h,T)=\lambda_+^N+\lambda_-^N
$$

을 얻는다. 항상 $\lambda_+>\lambda_-$이므로, $N$이 매우 클 때

$$
Z(N,h,T)=\lambda_+^N
$$

을 얻는다. 따라서, 각 쌍극자마다의 자유 에너지는

$$
f(h,T)=-kT\ln \lambda_+=-J-kT\ln\left[\cosh(\beta h)+\sqrt{\sinh^2(\beta h)+e^{-4\beta J}}\right]
$$

이 된다. 자유 에너지가 각 변수에 대하여 해석적이므로 유한한 온도의 1차원 이징 모형에서는 상전이가 발생하지 않는다.

## 2차원 이징 모형
2차원 이징 모형 또한 똑같은 방법으로 쓸 수 있다. $L\times L=N$개의 스핀이 있다고 가정할 때, 1차원 이징 모형을 응용하되 자기장 항을 지우고 $J=1$로 잡아 다음과 같이 쓰자.

$$
H(\sigma)=-\sum_{\langle i,j\rangle}\sigma_i \sigma_j
$$

이 때 $\sigma=(\sigma_1,\cdots,\sigma_N)$는 각 스핀의 방향이며, $\langle i,j\rangle$은 가장 가까운 이웃(nearest neighbor, NN)를 뜻한다. 그러면 분배 함수는 1차원의 경우와 같이

$$
Z(N,T)=\sum_{\sigma_1}\cdots \sum_{\sigma_N} e^{-\beta H}=\sum_{\sigma_1}\cdots \sum{\sigma_N}\prod_{\langle i,j\rangle}e^{\beta\sigma_i \sigma_j}
$$

가 된다. 또한, $\sigma_i,\sigma_j$는 항상 $\pm 1$의 값을 가지므로, $e^{\pm\beta}=\cosh(\beta)\pm\sinh(\beta)$임을 이용해서

$$
\prod_{\langle i,j\rangle}e^{\beta \sigma_i \sigma_j}=\prod_{\langle i,j\rangle}\cosh(\beta)+\sigma_i \sigma_j \sinh(\beta)=\prod_{\langle i,j\rangle}\cosh(\beta)(1+\sigma_i \sigma_j \tanh(\beta))
$$

를 얻는다. $\tanh(\beta)$를 $u$로 두고, $1/\sqrt{1-u^2}=\cosh(\beta)$를 이용해서,

$$
Z=(1-u^2)^{-B/2}\sum_{\sigma_1}\cdots\sum_{\sigma_N}\prod_{\langle i,j\rangle}(1+\sigma_i \sigma_j u)
$$

가 된다. $B$는 NN쌍의 수다. 곱셈을 풀어서 써 보면

$$
Z=(1-u^2)^{-B/2}\sum_{\sigma_1}\cdots\sum_{\sigma_N}\sum_{m=0}^{2N}u^m\sum_{\mathscr{N}\in \mathscr{N}^m}\prod_{(i,j)\in \mathscr{N}}\sigma_i\sigma_j
$$

이 된다. $\mathscr{N}^m$은 $m$개의 서로 다른 NN쌍들의 모임을 뜻한다.

이제 합기호를 계산해 보자. $\mathscr{N}$에 $i$가 홀수 개 들어 있다면 어떻게 될까? 이 경우, $\sigma_i=1$일 때와 $\sigma_i=-1$일 때의 계산 결과는 모든 것이 같고 부호만 다를 것이다. 이 둘을 더하면 0이 된다! 따라서 $i$는 홀수 개 들어갈 수 없고, 이는 모든 스핀 위치에 대해 성립한다. 다시 말해 덧셈을 모든 $\mathscr{N}$에 대해서 할 필요 없이, 각각의 스핀 위치가 짝수 번 등장하는 $\mathscr{N}$에 대해서만 하면 된다. 그리고 이 경우는 모든 스핀의 곱이 항상 1이 되므로, 다음과 같이 쓸 수 있다.


$$
Z=2^{N}(1-u^2)^{-B/2}\left(1+\sum_{G\in \mathscr{A}}u^{m(G)}\right)
\label{eqn:multtosum}
$$

여기서 $\mathscr{A}$는 격자 그래프 상에서 모든 꼭지점의 차수가 짝수인 부분그래프들의 집합이고, $m(G)$는 그래프 $G$의 변의 개수이다. 앞의 1은 $m=0$인 경우를 의미한다.

참고할 만한 사항은, 여기까지 우리는 격자의 종류에 대해 어떤 제한도 두지 않았다는 것이다. 1차원 체인의 경우 $\mathscr{A}=\emptyset$이고 $B=N-1\simeq N$이므로,

$$
Z=2^N(1-u^2)^{-N/2}=(2\cosh(\beta))^N
$$

가 된다. 1차원의 $h=0$인 경우와 비교해 보라.

---