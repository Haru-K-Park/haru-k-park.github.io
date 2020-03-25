---
layout: post
title: "가우시안 앙상블"
author: "YGLENA"
comments: true
---

* 
{:toc}

두 개의 멀리 떨어진 스케일을 생각해 보자. 이를테면 에너지 스케일에서 $\Lambda_{UV}\gg \Lambda_{IR}$을 생각할 수 있다. 이는 길이 스케일에서 $l_{UV}\ll l_{IR}$가 된다. 우리는 이 두 개의 스케일 사이에서 이론이 스케일 변환에 대해 거의 불변이라고 생각할 수 있다. 즉, $\beta=E\frac{d\lambda(E)}{dE}\simeq 0$이다.

이론에 등장하는 연산자의 차원을 생각하자. 4차원 시공간에서 차원이 4보다 작은 연산자들을 생각한다. 그러면, 스칼라 장 이론에서 $[ \phi]=1$이므로, $V=\kappa^3\phi+m^2\phi^2+\mu\phi^3$의 각 항의 질량 차원은 모두 0보다 크다. 이들을 관련 연산자<sup>relevant operator</sup>이라 한다.

차원이 4인 연산자의 경우, 즉 $\lambda_4 \phi^4$와 같은 경우, 이를 한계 연산자<sup>marginal operator</sup>이라 한다. 차원이 4 이상인 경우 무관련 연산자<sup>irrelevant operator</sup>이라 한다.

이제 각 커플링 상수를 무차원으로 만들어 주자. 즉 $\overline{\lambda_n}(E)=\frac{\lambda_n}{E^n}$으로 정의한다. $\lambda_n$을 맨값<sup>bare value</sup>라고 하고, 이는 어떤 재규격화 스케일에 대해서도 변하지 않아야 한다. 따라서

$$
0=\frac{d\lambda_n}{dE}=nE^{n-1}\overline{\lambda_n}+E^n\frac{d\overline{\lambda}}{dE}\quad\Rightarrow\quad \frac{d\overline{\lambda}}{dE}=-n\frac{dE}{E}
$$

가 되고, 고에너지에서의 커플링 상수의 값을 $\overline{\lambda}(\Lambda_{UV})$라 할 때 $\overline{\lambda}(E)\sim \overline{\lambda}(\Lambda_{UV})\left(\frac{\Lambda_{UV}}{E}\right)^n$이 된다. 따라서 다음을 얻는다.

$$
\overline{\lambda}(\Lambda_{UV})=\left(\frac{\Lambda_{IR}}{\Lambda_{UV}}\right)^n \overline{\lambda}(\Lambda_{IR})
$$

$n=0$일 때면 $\overline{\lambda}(\Lambda_{UV})$와 $\overline{\lambda}(\Lambda_{IR})$은 모두 $\mathcal{O}(1)$이지만, $n>0$이면 $\overline{\lambda}(\Lambda_{IR})$이 작은 $\Lambda_{IR}$일 때 매우 커지기 때문에 미세조정<sup>fine tuning</sup>이 필요하다.

한계 연산자의 경우 다음 결과를 얻는다.

$$
\overline{\lambda} (E) \sim \frac{1}{\overline{b}\log\left(\frac{E}{\Lambda_{IR}}\right)}
$$

이 경우에는 큰 계층을 만들기 위해서는 단순히 $\overline{\lambda}(\Lambda_{UV})$를 $\mathcal{O}(1)$로 만들고 조정해주면 된다.

즉 $\overline{\lambda}(\Lambda_{IR})\sim \mathcal{O}(1)$이기 위해서, $UV$의 값이 잘 골라져야 한다.

우리는 질량 계층이 다음을 만족하기를 바란다.

$$
\frac{\Lambda_{IR}}{\Lambda_{UV}}\leq 10^{-N}
$$

약력 스케일에서 $\Lambda_{IR}\sim 10^2\textrm{GeV}$이고 플랑크 질량이 $\sim 10^18 \textrm{GeV}$이므로 $N\sim 16$이라고 생각할 수도 있다. 아무튼, 이에 따르면 $\overline{\lambda}(\Lambda_{IR})\sim \mathcal{O}(1)$에서 $\overline{\lambda}(\Lambda_{UV})\sim 10^{-nN}\sim \mathcal{O}(1)$이려면 $n,N$이 서로 상쇄하여야 한다.

질량항 $m^2\phi^2$를 생각하면, $\overline{\lambda}(\Lambda_{UV})\sim 10^{-2N}$이다. 이것이 미세조정 없는 $UV$의 크기 $\mathcal{O}(1)$보다 매우 작기 때문에, 같아지고자 하면 매우 미세조정된 결과여야 한다.

$d=4-\epsilon$이라 하자. 이 때 $\overline{lambda}(\Lambda_{UV})\sim 10^{-\epsilon N}\sim \mathcal{O}(1)$이므로 ($\epsilon\ll 0$), 우리는 미세조정이 필요 없고, 계층은 매우 견고하다. $d=4$인 경우에도 마찬가지이다.

따라서 $\overline{\lambda}\ll 1$이 대칭성에 의해 조정되는 것이 아니라면, 그 이론은 미세조정되어야 한다는 결론을 얻을 수 있다. 이를 엇후프트 자연성 기준<sup>'t Hooft naturalness criteria</sup>이라 한다.
