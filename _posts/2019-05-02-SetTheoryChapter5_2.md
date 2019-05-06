---
title: "Set Theory Chpater5: Images, Composing Relations and Functions"
categories:
  - Mathematics
tags:
  - Set-Theory

---

## Images

Given a relation $R\subseteq A\times B$, we can consider the ***image*** under R of any subset $A'\in \mathcal{P}(A)$, that, is those elements of $B$ related by $R$ to some element in $A'$.

$R[A'] = \\{b \in B \| (\exists a \in A')(a, b) \in R\\}$

Of course, given $B'\subseteq B$ , its *inverse image* under $R$,

$R^{-1}[B'] = \\{a\in A \| (\exists b\in B')(a, b)\in R\\}$,

is exactly the *image* of $B'$ under the inverse relation $R^{-1}$.

Given a relation $R\subseteq A\times B$ , we call the set $R[A] \subseteq B$ the *image* of $R$.

Call a relation $R$ from $A$ to $B$ *total* iff for each $a\in A$ we have $R[\\{a\\}]\neq \emptyset $. And any function from $A$ to $B$ is a total relation.

Given a function $f \in [A\rightarrow B]$ and given a subset $A'\subseteq A$ we can define the restriction $f\upharpoonright _{A'} $ of $f$ to $A'$ as the

$f\upharpoonright _{A'} = \\{(a, b) \in f \| a \in A'\\}$.

Similary, given a relation $R\in \mathcal{P}(A\times B)$ and given a subset $A'\subseteq A$ we can define the restriction $R\upharpoonright _{A'}$ of $R$ to $A'$ as the set

$R\upharpoonright _{A'} = \\{(a, b) \in R \| a \in A'\\}$

## Composing Relations and Functions

Given relations $F : A \Rightarrow B$ and $G : B\Rightarrow C$, their ***composition*** is the relation $F; G : A \Rightarrow C$ defined as the set

$F; G = \\{(x, z) \in A\times C  \| (\exists y\in B)((x, y)\in F \wedge (y, z)\in G)\\}$

Similarly, given functions $f : A \rightarrow B$ and $g : B \rightarrow C$, their ***composition*** is the function $f;g : A \rightarrow C$ which is trivial to check it is a function.

Given any set $A$, the ***identity function*** on $A$ is the function $id_A = \\{(a, a) \| a \in A\\}$, or in assignment notation, $id_A : A \rightarrow A : a \mapsto a.$

Closely related to the identify function $id_A$on a set $A$ we more generally have inclusion functions. Given a subset inclusion $A'\subseteq A$, the  ***inclusion function*** from $A'$ to $A$ is the function $j^{A}_{A'} = \\{(a', a') \| a'\in A'\\}$, or in assignment notation, $j^{A}_{A'} : A' \rightarrow A : a' \mapsto a$.  To emphasize that an inclusion function identically includes the subset $A'$ into $A$, we will use the notation $j^{A}_{A'}: A' \hookrightarrow A$.  It is trivial to check that we have the equalities: $f\upharpoonright_{A'} = j^{A}_{A'}; f$ and $F\upharpoonright_{A'} = j^{A}_{A'}; F$.

We call a function $f : A \rightarrow B$ ***injective*** iff $(\forall a, a' \in A)(f(a) = f(a') \Rightarrow a = a')$. Obviously inclusion function is injective. We use the notation $f : A \rightarrowtail B$ as a shorthand for "$f$ is an injective function from A to B".

We call a function $f : A \rightarrow B$ ***surjective*** iff $B$ is the image of $f$, that is, iff $f[A] = B$. We use the notation $f : A \twoheadrightarrow B$ as a shorthand for "$f$ is a surjective function from $A$ to $B$"

For any $B$ such that $f[A] \subseteq B$ we always have $f = f;j^{B}_{f[A]}$ according to the composition

$A \twoheadrightarrow^{f} f[A] \hookrightarrow^{j^{B}_{f[A]}} B$.

Since any inclusion function is injective, the above composition $f = f;j^{B}_{f[A]}$ shows that any function can always be expressed as the composition of a surjective function followed by an injective function.

We call a function $f : A \rightarrow B$ ***bijective*** iff it is both injective and surjective. Obviously, the identity function $id_A$ is bijective. We use the notation $f : A \xrightarrow{\cong} B$ as a shorthand for "$f$ is a bijective function from $A$ to $B$." We also use the notation $A\cong B$ as a shorthand for "there exist a bijective function from $A$ to $B$".

Since any function $f : A\rightarrow B$ is a special case of a relation, its inverse relation $f^{-1} : B \Rightarrow A$ is always defined. However, in general $f^{-1}$ is a relation, but not necessarily a function. If we have two sets $A$ and $B$ such that there is a bijective function $f : A \xrightarrow{\cong} B$ between them, then in all relevant aspects these sets are "essentially same", because we can put each element $a$ of $A$ in a "one-to-one" correspondence with a unique element of $b$, and conversely each element $b$ of $B$ is put in one-to-one correspondence with a unique element of $A$, namely $f^{-1}(b)$.  This means that $f$ and $f^{-1}$ act as *faithful encoding functions*, so that the data from $A$ can be faithfully encoded by data from $B$, and data from $B$ can be faithfully decoded as data from $A$. It also means that the set $A$ and $B$ have "the same size".

We can illustrate the way in which a bijection between two sets makes them "essentially the same" by explaining how the powerset construction $\mathcal{P}(A)$ and the function set construction $[A\rightarrow 2]$ are intimately related in a bijective way. Given any set $A$, the set $\mathcal{P}(A)$ and $[A\rightarrow 2]$ are *essentially the same* in this precise, bijective sense. $\mathcal{P}(A)$ and $[A\rightarrow 2]$ give us two alternative ways of dealing with a subset $B\subseteq A$. Viewed as an element $B\in \mathcal{P}(A)$, B is just a subset. But we can alternatively view $B$ as a boolean-valued *predicate*, which is true for the elements of $B$, and false for the elements of $A-B$. That is, we can alternatively represent $B$ as the function

$\chi_B : A \rightarrow 2 : a \mapsto $ if $a\in B$ then 1 else 0 fi

where $\chi_B$is called the *characteristic function* of the subset $B$. The sets $\mathcal{P}(A)$ and $[A\rightarrow 2]$ are essentially the same, because the function $\chi_{\\\_} : \mathcal{P}(A) \rightarrow [A\rightarrow 2] : B \mapsto \chi_B $ is bijective, since its inverse is the function $(\\_)^{-1}[\\{1\\}] : [A\rightarrow 2] \rightarrow \mathcal{P}(A) : f \mapsto f^{-1}[\\{1\\}]$.

 We call a function $f : A \rightarrow B$ a ***left inverse*** iff there is a function $g : B \rightarrow A$ such that $f; g = id_A$. Similarly, we call $g : B \rightarrow A$ a ***right inverse*** iff there is a function $f : A \rightarrow B$ such that $f;g  = id_A$

 For exaple, composing

$N \hookrightarrow^{j^{Z}_{f[N]}} Z \twoheadrightarrow^{\| \\\_ \|} \mathbb{N} $.

the inclusion of the natural numbers in the integer with the absolute value function, we obtain, therfore $j^{Z}_{N}$ is a left inverse and \| \_ \| is a right inverse.

Call  a function $f : A  \rightarrow B$ ***epi*** iff for any set $C$ and any two functions $g,  h : B \rightarrow C$, if $f; g = f; h$ then $g = h$. Dually call a function $f : A \rightarrow B$ ***mono*** iff for any set $C$ and any two functions $g, h : C \rightarrow A$, if $g; f = h; f$ then $g =h$.

In the von Neumann representation of the natural numbers as sets, the number 1 is represented as the singleton set 1 = $\\{\emptyset \\}$. Given any set A, we can then consider the function sets $[1 \rightarrow A]$ and $[A \rightarrow 1]$. the set $[A\rightarrow 1]$ is always a singleton set. Later we will show we always have a bijection $A \cong [1\rightarrow A]$.

Note that, since for any set $A$ we have the set equality $\emptyset \times A = \emptyset $, then we also have set equalities $\mathcal{P}(\emptyset \times A) = \mathcal{P}(\emptyset) = \\{\emptyset \\} = 1$. Furthermore, the unique relation $\emptyset : \emptyset \Rightarrow A$ is obviously a function.  As a consequence, we have the additional set equalities $\mathcal{P}(\emptyset \times A) = [\emptyset \rightarrow A] = \\{\emptyset\\} = 1.$ That is, for any set A there is a unique function from the empty set to it, namely, the function $\emptyset : \emptyset \rightarrow A$, which is precisely the inclusion function $j^{A}_{\emptyset} : \emptyset  \hookrightarrow A$, and therfore always injective.

What about the function set $[A\rightarrow \emptyset]$? We of course have $[A\rightarrow  \emptyset]$? We of course have $[A\rightarrow \emptyset] \subseteq \mathcal{P}(A \times \emptyset) = \mathcal{P}(\emptyset) = \\{\emptyset\\} = 1$. Buf if $A \neq \emptyset$ teh unique relation $\emptyset : A \Rightarrow \emptyset$ is *not* a function. Therefore, if $A \neq \emptyset$ we have $[A\rightarrow \emptyset] = \emptyset$, that is, there are obviously *no* functions from a nonemptyset to the empty set. What about the case $A = \emptyset$? Then we have the set equalities $[\emptyset \rightarrow \emptyset] = \mathcal{P}(\emptyset \times \emptyset) = \mathcal{P}(\emptyset) = \{\emptyset \} = 1.$ Furthermore, the unique function $\emptyset : \emptyset \rightarrow \emptyset$ is precisely the identity function $id_{\emptyset}$.

---

Reference.

* José Meseguer. (2013). Set Theory and Algebra in Computer Science A Gentle Introduction to Mathematical Modeling.
