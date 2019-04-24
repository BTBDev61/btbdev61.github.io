---
title: "The Empty Set, Extensionality, and Seperation"
categories:
  - Mathematics
tags:
  - Set-Theory
last_modified_at: 2018-07-01T13:00:00+09:00

---

## The Empty Set

The simplest, most basic axiom, the *empty set axiom* can be captured by the following set theory formula, which we will refer to as the $\empty$ axiom:

$\empty$              ($\exists x$ )($\forall y$) $y \notin x$.

In plain english, we could say 

>  "There is a set that has no elements."

-------

## Extensionality

The *axiom of extensionality* allows us to determine when two sets are equal. In plain English the extensionality axiom can be stated as follows:

>  *Two sets are equal if and only if they have the same elemnts*

Again, this can be captured by the following formula in our langauge

$(\forall x, y)((\forall z)(z\in x \Leftrightarrow  z\in y)\Rightarrow x=y)$

where it is enough to have the implication $\Rightarrow$ in the formula, instead of the equivalence $\Leftrightarrow$, because if two sets are equal, then logical reasoning alone ensures that they must have the same elements, that is, we get the other implication $\Leftarrow$ for free, so that it needs not be explicitly stated in the axiom.

Note that extentsionality makes sure that our $\empty$ notation for the empty set is unambiguous, since there is only one such set. Indeed, suppose that we were to have two empty sets, say $\empty_1$ and $\empty_2$. We have the equivalence $(\forall z)(z \in \empty_1 \Leftrightarrow z\in \empty_2)$. But then forces the equality $\empty_1=\empty_2$.

The axiom of extensionality is intimately connected with the notion of a subset. Given two sets, $A$ and $B$, we say that $A$ is subset of $B$, denoted $A\subseteq B$, if and only if every element of A is an element of B.

$ x\subseteq y \Leftrightarrow (\forall z)(z\in x \Rightarrow z\in y)$

The above notation allows us to rephrase the Ext axiom as the implication 

$(\forall x, y)((x\subseteq y \wedge y\subseteq x)\Rightarrow x=y)$

We say that a subset inclusion $A\subseteq B$ is *strict* if, in addition $A\neq B$. We then use the notation $A\subset B$.

$x\subset y \Leftrightarrow (x\neq y\wedge(\forall z)(z\in x \Rightarrow z\in y))$.

-------

## Separation

The restriction imposed by separation axiom consists in requiring the quantification to range, not over all sets, but over the elements of some existing set.

If *A* is a set and $\phi$ is a set theory formula having *x* as its only free variable, then we can use $\phi$ to define the subset *B* of *A* whose elements are all the elements of *A* that satisfy the formula $\phi$ .

$\{{x\in A | \phi}\}$

In particular, formulas $\phi$ ans $\phi'$ that are *logically equivalent* (for example, $\phi \rightarrow \phi'$ and $\neg \phi \vee \phi'$ are logically equivalent formulas) always define by separation the same subset of the given set *A*, that is, if $\phi$ and $\phi'$ are logically equivalent, we always have the equality of sets {$x\in A | \phi$} = {$x\in A | \phi'$}.

The precise formalization of seperation axiom is as an *axiom sheme* parameterized by all set theory formulas $\phi$ whose only free variable is *x*. For any such $\phi$ the separation axiom scheme adds the formula

$(\forall y)(\exists !z)(\forall x)(x\in z \Leftrightarrow (x \in y \wedge \phi))$

> *Given any set A and any set theory formula $\phi (x)$ having x as its only free variable, we can define a subset of A consisting of all elements x of A such that $\phi (x)$ is true.

The separation axiom is sometimes called the *subset axiom*.

-------

Reference.

* José Meseguer. (2013). Set Theory and Algebra in Computer Science A Gentle Introduction to Mathematical Modeling.

