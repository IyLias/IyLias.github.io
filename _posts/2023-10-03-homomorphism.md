---
layout: post
comments: true
use_math: true
title:  "Homomorphism and Isomorphism"
date:   2023-10-03
categories: [math]
---


What is homomorphism? I don't know also.


## Definition : Homomorphism

A map $\phi$ of a group $G$ into a group $G'$ is a $homomorphism$ if

$\phi(a*b) = \phi(a) *' \phi(b)$

for all $a,b \in G$ where $<G,*>$ and $<G',*'>$


<br>

## Note

For any groups $G$ and $G'$, there is always at least one homomorphism $\phi: G -> G'$,
namely the $trivial$ $homomorphism$ defined by $\phi(g) = e'$ for all $g \in G$, where $e'$ is the identity in $G'$.


<br>

## Examples


$Q1$.  Let $GL(n, \R)$ be the multiplicative group of all invertible $n$ x $n$ matrices. Recall that a matrix $A$ is invertible if and only if its determinant, $det(A)$, is nonzero. Recall also that for matrices $A,B \in GL(n,\R)$ we have 

$det(AB) = det(A)det(B)$

This means that $det$ is a homomorphism mapping $GL(n,\R)$ into the multiplicative group $\R*$ of nonzero real numbers.


<br><br>


Now we turn to properties of Homomorphisms.

## Definition: Image and Inverse Image

Let $\phi$ be a mapping of a set $X$ into a set $Y$, and let $A$ $\sube$ $X$ and $B$ $\sube$ $Y$. The $image$ $\phi[A]$ of $A$ in $Y$ under $\phi$ is $\{ \phi(a)\mid a \in A \}$.
The set $\phi[X]$ is the $range$ of $\phi$. The $inverse$ $image$ $\phi^{-1}[B]$ of $B$ in $X$ is $ \{ x \in X \mid \phi(x) \in B \}$


<br>


### Theorem.

Let $\phi$ be a homomorphism of a group $G$ into a group $G'$

1. If $e$ is the identity in $G$, then $\phi(e)$ is the identity $e'$ in $G'$.

2. If $a \in G$, then $\phi(a^{-1}) = \phi(a)^{-1}$

3. If $H$ is a subgroup of $G$, then $\phi[H]$ is a subgroup of $G'$.

4. If $K'$ is a subgroup of $G'$, then $\phi^{-1}[K']$ is a subgroup of $G$.



<br><br>


## Definition: Kernel 

Let $\phi : G -> G'$ be a homomorphism of groups. The subgroup $\phi^{-1}[{e'}] = 
\{ x \in G \mid \phi(x)=e' \}$ is the $kernel$ of $\phi$, denoted by $Ker(\phi)$




<br>


## Relation between Homomorphism and Isomorphism

To show $\phi$ is an Isomorphism, 

* Show $\phi$ is a homomorphism

* Show $Ker(\phi)$ = $\{ e \}$.

* Show $\phi$ maps $G$ onto $G'$

