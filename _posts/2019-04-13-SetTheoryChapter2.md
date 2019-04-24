---
title: "Set Theory as an Axiomatic Theory"
categories:
  - Mathematics
tags:
  - Set-Theory
last_modified_at: 2018-07-01T13:00:00+09:00
---

In mathematics all entites are studied a very useful method called the *axiomatic method*.

> The entities in question, for example, points, lines and planes are characterized by means of axioms.

One uses *logical deduction* to infer from axioms the properties that the entities in question satisfy. Such properties, inferred from the basic axioms, are called *theorem*s.

The axioms, together with the theorems we can prove as their logical consequences, form a mathematical, axiomatic *theory*.

The way in which set theory is used as a language for mathematics is by expressing or translating other theories in terms of the theory sets. In this way, everything can be *reduced* to sets and relations between sets.

> a line can be precisely understood as a set of points satisfying certain properties.

---

But sets themselves are also *mathematical* entities, which in this particular encoding of everything as sets we happen to take as the most basic entities. This means that we can study sets also axiomatically, just as we study any other mathematical entity.

Mathematical logic, specifically the language of *first-order-logic*, allows us to define axiomatic theories, and then logically deduce theorems about such theories.

(This article is about set-theory, so that an explanation about first-order-logic will be skipped)

In the *formal language of set theory* there are no function symbols and no constants, and only one domain-specific binary predicate symbol, the $\in$ symbol, read *belong to*, or *is a member of*, or *is an element of*, which holds true of an element
$x$ and a set $X$, written $x \in X$ , if and only if $x$ is indeed an element of the set $X$ .

----

Let us now consider the process of *logical deduction*.

Any first-order logic theory is specified by the *language* $L$ of its formulas, and by a set $\Gamma$ of *axioms*, that is a set $\Gamma$ of formulas in the language $L$ .

Given any such theory with axioms $\Gamma$ , first-order logic provides a finite set of *logical inference rules* that allow us to derive all the theorems of the theory $\Gamma$ . Using these inference rules we can construct *proofs*, which show how we can reason logically from the axioms $\Gamma$ to obtain a given theorem $\phi$ by finite application of the rules.

If a formula $\phi$ can be proved from the axioms $\Gamma$ by such a finite number of logical steps, we use the notation $\Gamma \vdash  \phi$ , read, $\Gamma$ *proves* (or entails) $\phi$ , and call $\phi$ a *theorem* of $\Gamma$.

> If GP is the set of axioms of group theory, then the theorems of group thoery are the formulas $\phi$ in GP's language such that $GP \vdash \phi$.

*theorem prover* can prove theorems from $\Gamma$ either totally automatically, or with user guidance about what logical inference rules to apply to a given formula.

-----
Reference.
- José Meseguer. (2013). Set Theory and Algebra in Computer Science A Gentle Introduction to Mathematical Modeling.
