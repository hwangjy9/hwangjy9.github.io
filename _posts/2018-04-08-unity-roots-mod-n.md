---
layout: post
title: 합동식 $x^n \equiv 1\pmod p$의 해의 개수
description:
categories:
 - Number theory
tags:
 - congruence
---

합동식 $x^n\equiv 1\pmod p$의 해의 개수를 구하고 연관된 임용고시 문제를 풀어보았습니다.

## 명제

> **Theorem.** 홀수인 소수 $p$에 대해, 합동식 $x^n\equiv 1\pmod p$의 해의 개수는 $\gcd(p-1,n)$이다.

**Proof.** $p$가 홀수인 소수이므로 법 $p$에 대한 원시근(primitive root) $g$가 존재한다. 즉, $\operatorname{ord}_p g = \varphi(p)=p-1$인 정수 $g$가 존재한다. 이때 $\operatorname{ord}_p g$는 법 $p$에 대한 $g$의 위수(order)이며 $\varphi$는 오일러 피 함수(Euler phi function)이다. 그러면 $g^{p-1}\equiv 1\pmod p$이고 $1\le i < p-1$인 정수 $i$에 대해 $g^i\not\equiv 1\pmod p$이다. 여기서 $g^j\equiv 1\pmod{p}$일 필요충분조건은 $(p-1)\mid j$임을 알 수 있다. 한편 $|\mathbb{Z}_p^\times|=p-1$이고 $g,g^2,\dots,g^{p-1}(=1)$는 서로 다르므로, 임의의 $x\in\mathbb{Z}\setminus p\mathbb{Z}$에 대해 $x\equiv g^k\pmod p$인 $k\in\{1,\dots,p-1\}$가 존재한다. $x$가 $x^n\equiv 1\pmod p$의 해라면 $g^{kn}\equiv 1\pmod p$이고, $p-1\mid kn$에서 $k=\dfrac{p-1}{n}q$꼴임을 알 수 있다. 최대공약수의 정의에 의해 $p-1=k_1\gcd(p-1,n)$, $n=k_2\gcd(p-1,n)$이고 $\gcd(k_1,k_2)=1$인 정수 $k_1,k_2$가 존재한다. 그러면 $k=\dfrac{k_1}{k_2}q$이므로 $q=k_2 t=\dfrac{nt}{\gcd(p-1,n)}$ 꼴이다. 따라서 $k=\dfrac{p-1}{\gcd(p-1,n)}t,\; t=1,\dots, \gcd(p-1,n)$이고, 원하는 결론을 얻는다.
## 문제풀이
다음 문제는 2018년 임용고시 수학 문제 중 하나이다.
>**문제.** 합동식
>
>$$x^{n+5}-x^n-x^5+1\equiv 0\pmod{131}$$
>
>의 법 $131$에 대한 해의 개수가 $5$가 되도록 하는 $130$ 이하의 자연수 $n$의 개수를 풀이 과정과 함께 쓰시오.

**Solution.** 131이 소수인지 판정하기 위해 다음 정리를 활용할 수 있다.
> **Theorem.** 자연수 $n$이 합성수라면, $\sqrt{n}$ 이하인 $n$의 소인수가 존재한다.

$\lfloor 131 \rfloor=11$이고 11 이하의 소수는 2, 3, 5, 7, 11인데, 이들은 131의 소인수가 아니다. 따라서 131이 소수임을 알 수 있다. 한편, 주어진 합동식은

$$
(x^n-1)(x^5-1)\equiv 0\pmod{131}
$$

와 같고 $\mathbb{Z}_{131}$은 체이므로, 주어진 합동식의 해는 $x^n\equiv 1\pmod{131}$의 해이거나 $x^5\equiv 1\pmod{131}$의 해이다. $x^n\equiv 1\pmod{131}$의 해의 개수는 $\gcd(130,n)$이고 $x^5\equiv 1\pmod{131}$의 해의 개수는 $\gcd(130,5)=5$이다. 만약 $\gcd(130,n)>5$이면 주어진 합동식의 해의 개수가 5개를 초과하기 때문에 $\gcd(130,n)\le 5$이어야 한다. $130=2\times 5\times 13$이기 때문에, $\gcd(130,n)$은 $1, 2, 5$가 될 수 있다.

1. $\gcd(130,n)=1$일 경우: $x\equiv 1\pmod{131}$이 $x^n\equiv 1\pmod{131}$의 유일한 해가 되는데, $x\equiv 1\pmod{131}$은 $x^5\equiv 1\pmod{131}$의 해이기도 하다. 따라서 이 경우 주어진 합동식의 법 131에 대한 해의 개수는 5가 되며, 이때 130 이하의 $n$의 개수는 $\varphi(130)=(2-1)(5-1)(13-1)=48$이다.
2. $\gcd(130,n)=2$일 경우: $2\mid n$이므로 $x\equiv \pm 1\pmod{131}$은 $x^n\equiv 1\pmod{131}$의 해이다. 그런데 $x\equiv -1\pmod{131}$은 $x^5\equiv 1\pmod{131}$의 해가 아니므로, 주어진 합동식의 해의 개수가 6이다.
3. $\gcd(130,n)=5$일 경우: $x^5\equiv 1\pmod{131}$의 해는 모두 $x^n\equiv 1\pmod{131}$의 해가 되므로, 주어진 합동식의 해의 개수는 5가 된다. 한편 $5\mid n$이므로 $n=5k$인 정수 $k$가 존재하며, $2\nmid n$, $13\nmid n$이고 $(2,5)=(13,5)=1$이므로 $2\nmid k$, $13\nmid k$이다. 즉 $k$는 26 이하의 자연수이고 26과 서로소이므로, 130 이하의 $n$의 개수는 $\varphi(26)=(2-1)(13-1)=12$이다.

따라서 구하고자 하는 $n$의 개수는 $\varphi(130)+\varphi(26)=60$이다.