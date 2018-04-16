---
layout: post
title: $\pi+e$와 $\pi e$ 중 적어도 하나는 초월수
description:
categories:
 - field theory
tags:
 - algebraic number
---

$\pi$와 $e$가 무리수, 더 나아가 초월수라는 점은 잘 알려져 있습니다.[^1] 그러나 $\pi+e$와 $\pi e$가 초월수이거나 무리수인지는 아직 밝혀지지 않았습니다. 그럼에도 불구하고, $\pi+e$와 $\pi e$ 중 하나가 초월수(transcendental number)임을 보일 수 있습니다.

> **Theorem**. A field of algebraic numbers is algebraically closed.

**Proof.** Let $K$ be the field of algebraic numbers over $F$. Let $\alpha$ be a root of some polynomial in $K[x]$, then $K(\alpha)$ is algebraic over $K$. Since $K$ is algebraic over $F$, $K(\alpha)$ is algebraic over $F$. Thus $\alpha$ is algebraic over $F$. Since $K$ contains all roots of each polynomial in $F[x]$, $\alpha\in K$.

> **Proposition.** If $\alpha$ and $\beta$ are transcendental over $\mathbb{Q}$, then $\alpha+\beta$ or $\alpha\beta$ is transcendental over $\mathbb{Q}$.

**Proof.** Suppose that both $\alpha+\beta$ and $\alpha\beta$ are algebraic over $\mathbb{Q}$. Let $f(x)=x^2-(\alpha+\beta)x+\alpha\beta\in K[x]$, where $K$ is the field of algebraic numbers over $\mathbb{Q}$. Then coefficients of $f(x)$ are algebraic, and $\alpha$ and $\beta$ are roots of $f(x)$. Since $K$ is algebraically closed, $\alpha$ and $\beta$ are algebraic, which is a contradiction.

$\pi$와 $e$가 초월수임은 알려져 있으므로, $\pi+e$와 $\pi e$ 중 적어도 하나는 초월수임을 알 수 있습니다.

## 각주
[^1]: $\pi$와 $e$의 초월성에 대해선 [이 문서](http://people.math.sc.edu/filaseta/gradcourses/Math785/Math785Notes6.pdf)를 참고하시기 바랍니다.