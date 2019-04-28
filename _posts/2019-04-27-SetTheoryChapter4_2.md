---
title: "Set Theory Chpater4: Powersets, Infinity"
categories:
  - Mathematics
tags:
  - Set-Theory

---

## Powersets

Yet another, quite reasonable idea to build new sets out of previously constructed ones is to form the set of all subsets of a given set *A*, called its ***powerset***, and denoted $\mathcal{P}(A)$.

> Given any set, the collection of all its subsets is also a set.

$(\forall x)(\exists !y)(\forall z)(z\in y \Leftrightarrow z \subseteq x)$

It is trivial to show that if $U, V \in \mathcal{P}(X), then U\cup V, U\cap V, U-V, U\boxplus V \in \mathcal{P}(X)$, that is, $\mathcal{P}(X)$ is *closed under all bolean operations*. Furthermore, there is one more boolean operation not defined for sets in general, but defined for sets in $\mathcal{P}(X)$, namely, *complementation*. Given $U \in \mathcal{P}(X)$, its *complement, denoted $\bar{U}$ , is, by definition, the set $\bar{U} = X - U$.

Note that this clousre under boolean operations *can be extended to arbitrary unions and arbitrary intersection*. We need to consider set of sets $\mathcal{U}$ whose elements are subset of a given set $X$.

Given $\mathcal{U} \in \mathcal{P}(\mathcal{P}(X))$, its union is always a subset of $X$, that is, $\bigcup \mathcal{U} \subseteq X$, or, equivalently, $\bigcup \mathcal{U} \in \mathcal{P}(X)$. If $\mathcal{U} \in \mathcal{P}(\mathcal{P}(X))$ is a *nonempty* set of subsets of $X$, then we likewise have $\bigcap \mathcal{U} \subseteq X$, or, equivalently, $\bigcap \mathcal{U} \in \mathcal{P}(X)$. (when $\mathcal{U} = \emptyset$ , the intersection $\bigcap \mathcal{U}$ is not defined.)

However, we can in the context of $\mathcal{P}(X)$ extend the intersection operation also to the empty family by *flat*, defining it as: $\bigcap \emptyset = X$. Intuitively, the more sets we intersect, the smaller the intersection:

$\bigcap \\{U\\} \supseteq \bigcap\\{U, V\\} \supseteq \\{U, V, W\\} \supseteq ...$

Following this reasoning, since for any $U \subseteq X$ we have $\emptyset \subseteq \\{U\\}$, we should always have $\bigcap \emptyset \supseteq \\{U\\} = U$. Since we know that the biggest set in $\mathcal{P}$ is $X$ itself, it is then entirely natural to define $\bigcap \emptyset = X$, as we have done.

Once we have powersets, we can define many other interesting sets. For example, given sets A and B, we can define the set $A\otimes B$ of all unordered pairs {a, b} with $a\in A$ and $b \in B$ as the set

$A\otimes B = \\{\\{x, y\\}\in \mathcal{P}(A\cup B) \| (x\in A \wedge y \in B)\\}$

Similary, we can define the set $A\times B$ of all ordered pairs (a, b) with $a\in A$ and $b \in B$, called the ***cartesian product*** of A and B, as the set

$A \times B = \\{\\{\\{x\\}, \\{x, y\\}\\} \in \mathcal{P}(\mathcal{P}(A\cup B)) \| (x\in A \wedge y \in B)\\}$  

Using cartesian products, we can also construct the *disjoint union* of two sets $A$ and $B$. The idea of the disjoint union is to avoid any overlaps between A and B, that is, to *force* them to be disjoint before building their union.

$A\oplus B = (A \times \\{0\\})\cup(B \times \\{1\\})$

These sets $A \times \\{0\\}$ and $B \times \\{1\\}$ are respectively just like $A$ or $B$, except that each element $a \in A$ has now an extra marker "0" and is represented as the ordered pair (a, 0); and each $b\in B$ has now an extra marker "1" and is represented as the ordered pair (b, 1).

## Infinity

It is of course very compelling to think that, if we have all the natural numbers 1, 2, 3, …, $n$, …, as finite sets, there should exist an *infinite* set containing exactly those numbers, that is, the set of all natural numbers.

Note that this set, if it exists, satisfies two interesting properties:

1. 0 = $\emptyset$ belongs to it
2. if $x$ belongs to it, then $s(x) = x\cup\\{x\\}$ also belongs to it.

We call any set satisfying conditions (1) and (2) a ***successor set***.

Even though in a naive, unreflective way of doing mathematics the existence of the natural numbers would be taken for granted, in our axiomatic theory of sets it must be explicitly postulated as a new axiom, called the *axiom of infinity*, which can be informally stated in English as follows:

> There is a successor set

$(\exists y)(\emptyset \in y \wedge (\forall x \in y)((x\cup \\{x\\})\in y))$

Note that the successor set *y* asserted to exist by this axiom is not unique: there can be many successor sets.

* If $S$ and $S'$ are successor sets, then $S\cup S'$ and $S\cap S'$ are also successor sets.

* If $S$ is a successor set, then the set of all successor sets $S'$ such that $S' \subseteq S$ can be precisely defined as the following subset of $\mathcal{P}(S)$

  $\\{S'\in \mathcal{P}(S) \| (\emptyset \in S' \wedge (\forall x \in S')((x\cup\\{x\\})\in S'))\\}$

* This set is of course nonempty (S belongs to it) and its intersection

  $\bigcap \\{S'\in \mathcal{P}(S) \| (\emptyset \in S' \wedge (\forall x \in S')((x\cup \\{x\\})\in S'))\\}$

  is a successor set.

* If $X$ is  a set having an element $z\in X$ such that for all $x\in X $ we have $z\subseteq x$, then $\bigcap X = z$

We can then use these easy facts to define the set $\mathbb{N}$ of the natural numbers. Let $S$ be a successor set, which we know it exists because of the axiom. We define $\mathbb{N}$ as the intersection:

$\mathbb{N} = \bigcap \\{S'\in \mathcal{P}(S) \| \emptyset \in S' \wedge (\forall x \in S')((x\cup \\{x\\})\in S')\\}$

which we know is a successor set

The key question, of course is the *uniqueness* of this definition.

Suppose we had chosen a different successor set $T$ and had used the same construction to find its smallest successor subset. $S\cap T$ is also a successor set. And, since $S\cap T \subseteq S$,this implies that $\mathbb{N} \subseteq (S\cap T) \subseteq T$. That is, any successor set contains $\mathbb{N}$ as a subset. Then using last bullet above, we get that for any successor set $T$

 $\mathbb{N} = \bigcap \\{T'\in \mathcal{P}(T) \| \emptyset \in T' \wedge (\forall x \in T')((x\cup \\{x\\})\in T')\\}$

as claimed. The fact that any successor set contains $\mathbb{N}$ as a subset has the following well-known induction principle as an immediate consequence:

> Theorem 2 (Peano Induction) if $T\subseteq \mathbb{N}$ is a successor set, then $T = \mathbb{N}$.

It is an indispensable reasoning principle used routinely in many mathematical proofs: to prove that a property $P$ holds for all natural numbers, we consider the subset $T\subseteq \mathbb{N}$ for which $P$ holds; then, if we can show that P(0) (that is, that $0\in T$)and that for each $n\in \mathbb{N}$ we have the implication $P(n) \Rightarrow P(s(n))$ (that is, that $n\in T \Rightarrow s(n)\in T$), then we have shown that $P$ holds for all $n\in \mathbb{N}$. Because this means that we have proved that $T$ is a successor set, and then by Peano Induction we must have $T = \mathbb{N}$.
