---
title: "Set Theory Chpater5: Relations, Functions, Formula, Assignment and Lambda Notations"
categories:
  - Mathematics
tags:
  - Set-Theory

---

One of the key ways in which set theory is an excellent mathematical modeling language is precisely by how easily and naturally relations and functions can be represented as *sets*. Furthermore, set theory makes clear how relations and functions can be *composed*, giving rise to new relations and functions.

---

## Relations and Functions

A ***relation*** is exactly a set of ordered pairs in some cartesian product. That is, a relation is exactly a *subset* of a certain product $A \times B$ , that is an element of the powerset $\mathcal{P}(A\times B)$ for some sets $A$ and $B$.

By convention we write $R : A \Rightarrow B$ as a useful, shorthand notation for $R \in \mathcal{P}(A\times B)$, and say "$R$ is a relation from $A$ to $B$", or "$R$ is a relation whose *domain* is $A$ and whose *codomain* (or range) is $B$." Sometimes, instead of writing $(a, b) \in R$ to indicate that a pair $(a, b)$ is in the relation $R$, we can use the more intuitive infix notation *a R b*.

Note that given a relation $R \subseteq A \times B$ we can devine its *inverse* relation $R^{-1} \subseteq B \times A$ as the set $R^{-1} = \\{ (y, x) \in B\times A \| (x, y) \in R\\}$.

A ***function*** is a *special kind of relation*. a function $f$ is a relation that must be *defined* for every element $x\in A$, and must relate each element $x$ of $A$ to a *unique* element $f(x)$ of $B$.

What is the *set of all functions* from $A$ to $B$ ? Obviously a *subset* of $\mathcal{P}(A \times B)$, which we denote $[A\rightarrow B]$ and call the *function set from* $A$ to $B$.

$[A\rightarrow B] = \\{ f\in \mathcal{P}(A\times B) \| (\forall a \in A)(\exists! b\in B)(a, b) \in f\\}$

By convention, we write $f : A\rightarrow B$ as a shorthand notation for $f \in [A\rightarrow B]$. We then read it as "$f$ is a function from $A$ to $B$, or "$f$ is a function whose *domain* is $A$, and whose *codomain* (also called *range*) is $B$"  

---

## Formula, Assignment, and Lambda Notations

The fact that we know that the set of all relations from $A$ to $B$ is the powerset $\mathcal{P}(A\times B)$, and that the set of all functions from $A$ to $B$ is the set $[A\rightarrow B]$ is well and good; but that does not tell us anything about how to specify any concrete relatoin $R \in \mathcal{P}(A\times B)$, or any concrete function $f\in [A\rightarrow B]$.

In hard way, we can just *list* the elements making up the relation $R$, say, $R = \\{(a_1, b_1), …, (a_n, b_n)\\}$. Of course, for finite functions $f$ we can do just the same: we can specify $f$ as teh set of its pairs $f = \\{(a_1, b_1), …, (a_n, b_n)\\}$.

The easy way is to represent relations and functions *symbolically*, or as philosophers like to say, *intensionally*.

 So we can just *agree* that a precise linguistic description of a relation *R* is just a *formula* $\phi$ in set theory with exactly two free variables, $x$ and $y$. Then given domain and codomain sets $A$ and $B$, this formula $\phi$ unambiguously defines a relation $R\subseteq A\times B$, namely, the relation

$R = \\{(x, y) \in A\times B \| \phi\\}$

For example, the greater than relation, >, on the von Neumann natural numbers can be specified by the set theory formula $y\in x$, since we have,

$>= \\{(x, y)\in \mathbb{N}\times \mathbb{N} \| y \in x\\}$

Let us call this syntactic way of defining relations the ***formula notation***.

Using formula notation to specify function is not always a good idea. Because just from looking at a formula $\phi(x, y)$ we may not have an obvious way to know that for each $x$ there will always be a *unique* $y$ such that $\phi(x, y)$ holds, and we need this to be the case if $\phi (x, y)$ is going to define a function.

A better way is to use a set-theoretic *term* or *expression* to define a function. We can do this using two different notation, called, respectively, the ***assignment*** notation and ***lambda*** notation.

In the assignment notation we write, for example, $s : \mathbb{N} \times \mathbb{N} : x \mapsto x \cup \\{x\\}$ to unambiguously define the successor function. More generally, if $t(x)$ is a set-theoretic term or expression having a single variable $x$, then we can write $f : A\rightarrow B : x \mapsto t(x)$ to define the function $f$. Of course it is specified as the set

$f = \\{(x, y) \in A\times B \| y = t(x)\\}$.

Ok, but how do we *know* that such a set is a function? Well, we do not quite know. There is a possibility that the whole thing is nonsense and we have *not* defined a function. In order for this notation to really define a function from $A$ to $B$, we must furthermore check that for each $a\in A$ the element $t(a)$ belongs to the set $B$. An alternative, quite compact variant of the assignment notation is the notation $A\ni x \mapsto t(x) \in B$.

What about *lambda notation*?  To make explicit the domain $A$ and codomain $B$ of the function  so defined we should write $\lambda x \in A. t(x) \in B.$ Again this could fail to define a function if for some $a\in A$ we have $t(a)\notin B$

Perhaps a nagging doubt that should be assuaged is what terms, say, $t(x)$ or $t(x_1, …, x_n)$, are we allowed to use in our set theory language. The answer to this question is that we are free to use any terms or expressions avilable to us in any *definitional extension of the set theory language*. The idea of a *definitional extension* of a first-order language is very simple: we can always add new, auxiliary notation, provided this new notation is precisely defined in *terms of the previous notation*.

For example, we defined the containment relation $\subseteq$ in terms of the basic notation of set theory — which only uses the $\in$ binary relation symbol and the built-in equality symbol — by means of the defining equivalence $x\subseteq y \Leftrightarrow  (\forall z)(z\in x \Rightarrow z \in y)$.

More precisely, given any formula $\phi$ in our language whose free variables are exactly $x_1, …, x_n $, we can introduce a new predicate symbol, say $P$, of $n$ arguments as an abbreviation for it, provided we add the axiom $P(x_1, …, x_n) \Leftrightarrow \phi$, which uniquely defines the meaning of $P$ in terms of $\phi$.

If we have a formula $\phi$ in our language whose free variables are exactly $x_1, …, x_n, y$ and we can *prove* tha the formula $(\forall x_1, …, x_n) \Leftrightarrow \phi$ is a theorem of set theory, then we can introduce in our language a new function symbol $f$ of $n$ arguments, and we can define the meaning of $f$ by adding the axiom $f(x_1, …, x_n) = y \Leftrightarrow \phi$.

---

 Reference.

* José Meseguer. (2013). Set Theory and Algebra in Computer Science A Gentle Introduction to Mathematical Modeling.
