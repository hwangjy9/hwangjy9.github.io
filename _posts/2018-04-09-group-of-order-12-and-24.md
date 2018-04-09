---
layout: post
title: 위수 12인 군과 위수 24인 군의 정규부분군
description: 위수 12인 군과 위수 24인 군은 단순군(simple group)이 아님을 알 수 있습니다.
categories:
 - Group theory
tags:
---

## 문제 1
> Prove that every group of order 12 has a normal subgroup of order 3 or 4.

**Proof.** Let $G$ be a group of order 12. Since $|G|=12=2^2\cdot 3$, Sylow 2-subgroups of $G$ have order $2^2$, and Sylow 3-subgroups of $G$ have order 3. Let $n_2, n_3$ be the number of Sylow $n_2, n_3$-subgroups of $G$. By the Sylow theorem, there are integers $k_2,k_3\ge 0$ such that $n_2=2k_2+1\mid 3$ and $n_3=3k_3+1\mid 4$. Thus $n_2=1\text{ or }3$ and $n_3=1\text{ or }4$. If $n_3=1$, then the Sylow 3-subgroup is normal, so $G$ has a normal subgroup of order 3. Now suppose that $n_3=4$. Sylow 3-subgroups intersect trivially, so $G$ has at least 8 elements of order 3 and at most 3 elements that are not of order 3. Thus there is at most one Sylow 2-subgroups of $G$. Thus $G$ has a normal subgroup of order 4.

## 문제 2
> Prove that every group of order 24 has a normal subgroup of order 4 or 8.

**Proof.** Let $G$ be a group of order 24. Since $|G|=24=2^3\cdot 3$, Sylow 2-subgroups of $G$ have order $2^3$. Let $n_2$ be the number of Sylow 2-subgroups, then $n_2=1$ or $n_2=3$. If $n_2=1$, then the Sylow 2-subgroup is normal, so $G$ has a normal subgroup of order 8. Now suppose $n_2=3$, and let $H$ and $K$ be distinct Sylow 2-subgroups. Let $N=N_G(H\cap K)$ be the normalizer of $H\cap K$. Then
$$
|H\cap K|=\frac{|H||K|}{|HK|}\ge \frac{|H||K|}{|G|}=\frac{8\cdot 8}{24}>2.
$$
Since $H\cap K$ is a subgroup of $H$, $|H\cap K|$ is a divisor of $|H|=8$. Thus $|H\cap K|=4$. Since
$$
[H:H\cap K]=[K:H\cap K]=2,
$$
$H\cap K$ is normal in both $H$ and $K$, so $H,K\subset N$ and so $HK\subset N$. Since $N$ is a subgroup of $G$, $|N|\mid 24$. Also,
$$
|HK|=\frac{|H||K|}{|H\cap K|}=\frac{8\cdot 8}{4}=16\le |N|.
$$
Thus $|N|$ must be 24 and $N=G$. Therefore, $H\cap K$ is normal in $G$, and $G$ has a normal subgroup of order 4.