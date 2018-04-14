---
layout: post
title: 모든 원소의 위수가 유한인 무한군의 예시
description:
categories:
 - Group theory
tags:
 - example
---

$\mathbb{Q}/\mathbb{Z}$는 무한군이지만, 각 원소의 위수(order)는 유한입니다.

$\mathbb{Q}/\mathbb{Z}$의 임의의 원소를 $\frac{p}{q}+\mathbb{Z}$ (단, $p$는 정수, $q$는 양의 정수이고 $\gcd(|p|,q)=1$)로 나타낼 수 있는데, 그러면 $1\le i < q$인 정수 $i$에 대해 $q\nmid ip$이므로
$$
i\left(\frac{p}{q}+\mathbb{Z}\right)\ne\mathbb{Z}
$$
이고
$$
q\left(\frac{p}{q}+\mathbb{Z}\right)=p+\mathbb{Z}=\mathbb{Z}
$$
입니다. 따라서 $\operatorname{ord}\left(\frac{p}{q}+\mathbb{Z}\right)=q$를 얻습니다.

## 문제
> Prove or disprove: $\mathbb{Q}/\mathbb{Z}\cong \mathbb{Q}$

Every element of $\mathbb{Q}/\mathbb{Z}$ has finite order, but the order of each nonzero element of $\mathbb{Q}$ is $\infty$.  Thus $\mathbb{Q}/\mathbb{Z}\not\cong \mathbb{Q}$.