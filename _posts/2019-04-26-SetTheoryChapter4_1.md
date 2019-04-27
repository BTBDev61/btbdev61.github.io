---
title: "Set Theory Chpater4: Pairing, Unions"
categories:
  - Mathematics
tags:
  - Set-Theory

---

## Pairing

 One very reasonable idea is to consider sets whose only elemenet is another set. Such sets are called ***singleton sets***.

We can also get sets whose only elements are other sets A and B. Such sets are called (unordered) ***pairs***, and are denoted {A, B}. What happens if we try to enclose A *twice* inside the outer box? This set expression still contains only *one* element, namely *A*, so that, by extensionality {A, A} = {A}. That is we get notion of a singleton set as a special case of the notion of a pair.

> Given sets A and B, there is a set whose elements are exactly A and B.

$(\forall x, y)(\exists !z)(\forall u)(u\in z \Leftrightarrow (u = x \vee u = y))$

Of course, by extensionality, the order of the elements does not matter.

What about ***ordered pairs***? Following an idea of Kuratowski, we can *define* an ordered pair (x, y) as a special kind of unordered pair by means of the defining equation.

$(x, y) = \{\{x\}, \{x, y\}\}$.

A key property of ordered pairs is a form of extensionality for such pairs, namely, the following

> Lemma 1 (Extensionlity of Ordered Pairs). For any sets $x, x', y, y'$, the following equivalence holds:
>
> $(x, y) = (x', y') \Leftrightarrow (x = x' \vee y = y')$

One could reasonably wish to distinguish between the *abstract concept* of an ordered pair $(x, y)$, and a *concrete representation* of that concept, such as the set $\{\{x\}, \{x, y\}\}$. Lemma 1 gives strong evidence that this particular choice of representation faithfully models the abstract notion.

---

## Unions

Another reasonable idea is that of *gathering together the elements of various sets into a single set*, called their *union*, that contains exactly all such elements.

In its simplest version, we can just consider two sets, *A* and *B*, and define thier union $A\cup B$ as the set containing all the elements in $A$ or in $B$.

$(\forall x, y)(\exists !z)(\forall u)(u\in z \Leftrightarrow (u\in x \vee u\in y))$

this would be entirely correct and perfectly adequate for *finite* unions of sets.

We can more generally, consider any (finite or infinite) set of sets (and in pure set theory *any* set is always a set of sets), say {$A_1, A_2, A_3, …$}, and then form the union of all those sets.

> Given any collection of sets, there is a set such that an element belongs to it if and only if it belongs to some set in the collection.

$(\forall x)(\exists !y)(\forall z)(z\in y \Leftrightarrow (\exists u)(u\in x \wedge z\in u))$

We introduce the notation $\bigcup x$ to denote the unique set *y* claimed to exist by the above formula, and call it the *union* of the collection of sets *x*.

the $intesection \bigcap x$ of a set $x$ of sets is of course the set of elements that belong to all the elements of $x$, provided $x$ is *not* the empty set. (if $x = \emptyset$ , the intersection is not defined).

$\bigcap x = ${$y\in \bigcup x \| (\forall z \in x) y \in z$}

Given two sets A and B, we say that they are ***disjoint*** if and only if $A\cap B = \emptyset$ .

A set of sets $X$ is called a collection of ***pairwise disjoint*** sets if and only if for any $x, y \in X$, we have the implication $x\neq y \Rightarrow x\cap y = \emptyset$.

> Definition 1
>
> Let X be a collection of pairwise disjoint sets and let $Y = \bigcup X$. Then $X$ is called a ***partition*** of $Y$ iff either (i) X = Y = $\emptyset$; or (ii) $X\neq \emptyset \wedge \emptyset \notin X$. That is, a partition of X of Y = $\bigcup X$ is either the empty collection of sets when Y = $\emptyset$, or a nonempty collection of pairwise disjiont nonempty sets whose union is Y.



So far, we have seen how intersection can be obtained from unions. we can likewise define other *boolean operation* among sets.

The *set difference* $A-B$ of two sets, that is, the set whose elements are exactly those elements of $A$ that do not belong to $B$, is deinfed using union and the *Sep* axiom as the set

$A - B = ${$x\in A\cup B \| x\in A \wedge x\notin B$}

Similarly, the *symmetric difference* of two sets $A \boxplus B$ can be defined by the equation

$A\boxplus B = (A - B) \cup (B - A) $

Of course, with set union, as well as with the other boolean opeartions we can define based on set union by separation. For example, we can associate to any set $A$ another set $s(A)$, called its *successor*, by defining $s(A) = A \cup \{A\}$.

In particular, we can consider the sequences of sets

$\emptyset   $          $    s(\emptyset ) $          $s(s(\emptyset ))$           $     s(s(s(\emptyset ))) … $

 which is the sequence of von Neumann *natural numbers*. Now the number *n* is a set with *exactly* $n$ elements, which precisely the previous numbers; and $n < m$ iff $n\in m$.

---

Reference.

* José Meseguer. (2013). Set Theory and Algebra in Computer Science A Gentle Introduction to Mathematical Modeling.
