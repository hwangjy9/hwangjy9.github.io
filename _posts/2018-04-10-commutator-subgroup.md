---
layout: post
title: 교환자부분군
description:
categories:
 - Group theory
tags:
 - commutator subgroup
---

교환자부분군(commutator subgroup)에 대한 문제 하나를 풀어보았습니다.

## 문제
> Let $G$ be a group and let $G'=\langle aba^{-1}b^{-1}\rangle$; that is, $G'$ is the subgroup of all finite products of elements in $G$ of the form $aba^{-1}b^{-1}$. The subgroup $G'$ is called the **commutator subgroup** of $G$.[^1]
> 
> (a) Show that $G'$ is a normal subgroup of $G$.
>
> (b) Let $N$ be a normal subgroup of $G$. Prove that $G/N$ is abelian if and only if $N$ contains the commutator subgroup of $G$.

## 풀이
> (a) Show that $G'$ is a normal subgroup of $G$.

We show that $gG'g^{-1} \subset G'$ for any $g\in G$. Let $x\in G'$, then $gxg^{-1}=x(x^{-1}gxg^{-1})$, and $x^{-1}gxg^{-1}$ is an element of $G'$ by the definition of the commutator subgroup. Thus $gxg^{-1}\in G'$ and so $gG'g^{-1}\subset G'$. Therefore, $G'$ is a normal subgroup of $G$.

> (b) Let $N$ be a normal subgroup of $G$. Prove that $G/N$ is abelian if and only if $N$ contains the commutator subgroup of $G$.

$$\begin{align}
G/N\text{ is abelian}&\Longleftrightarrow (aN)(bN)=(bN)(aN)\text{ for all }a,b\in G\\
&\Longleftrightarrow aba^{-1}b^{-1}\in N \text{ for all }a,b\in G\\
&\Longleftrightarrow G' \subset N
\end{align}$$

## 각주
[^1]: Thomas W. Judson, Robert A. Beezer. (2016). [Abstract Algebra: Theory and Applications](http://abstract.pugetsound.edu/), p. 124.