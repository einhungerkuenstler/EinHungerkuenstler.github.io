---
title: II. The Morphisms Relations of Groups
layout: simple
---

$$\gdef\def{\blue{\operatorname{def}}}$$
$$\gdef\dfs{\blue{:=}}$$
$$\gdef\ifif{\blue{\iff}}$$
$$\gdef\imp{\blue{\implies}}$$
$$\gdef\diff{\blue{:\longleftrightarrow}}$$
$$\gdef\op#1{\blue{\operatorname{#1}}}$$
$$\gdef\limp{\blue{\Longleftarrow}}$$
$$\gdef\st{\blue{\texttt{s.t.}}}$$
$$\gdef\the{\blue{\Rightarrow}}$$
$$\gdef\wrs{\blue{=:}}$$
$$\gdef\typ{\blue{:\in}}$$
$$\gdef\if{\blue{\texttt{if}}}$$
$$\gdef\inner#1#2{\left\langle\strut#1,#2\right\rangle}$$
$$\gdef\hby{\blue{- :}}$$
$$\gdef\norm#1{\left\Vert\strut#1\right\Vert}$$
$$\gdef\abs#1{\left\vert\strut#1\right\vert}$$
$$\gdef\op#1{\blue{\operatorname{#1}}}$$
$$\gdef\gen#1{\left \langle #1 \right \rangle}$$
$$\gdef\geni#1{\left( #1 \right)}$$
$$\gdef\contra{\blue{\texttt{Opq!}}}$$
$$\gdef\im#1{\operatorname{Im}(#1)}$$
$$\gdef\ke#1{\operatorname{Ker}(#1)}$$
$$\gdef\ord#1{\operatorname{ord}(#1)}$$
$$\gdef\sgn{\operatorname{sgn}}$$
$$\gdef\Aut#1{\operatorname{Aut}(#1)}$$
$$\gdef\mod{\operatorname{mod}}$$
$$\gdef\ideal{\triangleleft}$$
$$\gdef\abs#1{\left\vert#1\right\vert}$$
$$\gdef\P{\mathbb{P}}$$
$$\gdef\iso{\cong}$$
$$\gdef\norsub{\trianglelefteq}$$
$$\gdef\card#1{\operatorname{card}(#1)}$$
$$\gdef\mul{\cdot}$$
$$\gdef\N{\mathbb{N}}$$
$$\gdef\Z{\mathbb{Z}}$$
$$\gdef\Q{\mathbb{Q}}$$
$$\gdef\R{\mathbb{R}}$$
$$\gdef\C{\mathbb{C}}$$
$$\gdef\colortext#1{\blue{\textsf{#1}}}$$
$$\gdef\colormath#1{\blue{\mathsf{#1}}}$$
$$\gdef\rank{\mathrm{rank}}$$
$$\gdef\null{\mathrm{null}}$$
$$\gdef\det{\mathrm{det}}$$
$$\gdef\gcd{\mathrm{gcd}}$$
$$\gdef\lcm{\mathrm{lcm}}$$

### $$\colormath{2.1\;Group\; \sim morphisms}$$

### $$\colortext{2.1.1. Group Homomorphism}$$

### $$\colortext{Group Homomorphism}$$

- $$G, H$$ are groups

- $$f: G \to H$$ is a function

  $$\def$$ $$f$$ is a **group homomorphism** $$\difif$$ $$f(ab) = f(a)f(b) \; \forall a, b \in G$$

> - `Homomorphism preserves the identity element and inverse element`
>
>    - $$f$$ is a homomorphism $$\imply$$ $$f(e_G) = e_H$$, where $$e_G, e_H$$ are identity elements of $$G, H$$ respectively -- by uniqueness of identity element.
>
>    - $$f$$ is a homomorphism $$\imply$$ $$f(a^{-1}) = f(a)^{-1} \; \forall a \in G$$ -- by uniqueness of inverse element.

### $$\colortext{Image and Kernel}$$

- $$G, H$$ are groups

- $$f: G \to H$$ is a group homomorphism

  $$\def$$ $$\im{f} : = \{f(a) \mid a \in G\}$$ is the **image** of $$f$$

  $$\def$$ $$\ke{f} : = \{a \in G \mid f(a) = e_H\}$$ is the **kernel** of $$f$$

> - `Image is a subgroup of $$H$$:` $$\im{f} \leq H$$ -- By $$\colortext{Subgroup Criterion}$$.
>
> - `Kernel is a subgroup of $$G$$:` $$\ke{f} \leq G$$ -- By $$\colortext{Subgroup Criterion}$$.
>
> ---
>
> - $$f$$ is surjective $$\ifif$$ $$\im{f} = H$$ -- By definition of surjective.
>
> - $$f$$ is injective $$\ifif$$ $$\ke{f} = \{e_G\}$$ 
>
>    -- $$\imply:$$ By contradiction.
>
>    -- `<=:` For any $$a, b \in G$$, assume $$f(a) = f(b)$$. Then, $$f(a) (f(b))^{-1} = e_H$$. By homomorphism, $$f(a) (f(b))^{-1} = f(a (b^{-1})) = e_H$$. Thus, $$a (b^{-1}) \in \ke{f}$$ $$\implies$$ $$a (b^{-1}) = e_G$$. Hence, $$a = b$$.
>
> ---
>
> - $$\forall a, b \in G$$, $$f(a) = f(b)$$ $$\ifif$$ $$a b^{-1} \in \ke{f}$$
>
>    -- $$\imply:$$ $$f(a) = f(b)$$ $$\implies f(a) (f(b))^{-1} = e_H$$ $$\implies f(a b^{-1}) = e_H$$ $$\implies a (b^{-1}) \in \ke{f}$$.
>
>   -- `<=:` $$a (b^{-1}) \in \ke{f}$$ $$\implies$$ $$f(a (b^{-1})) = e_H$$ $$\implies f(a) (f(b))^{-1} = e_H$$ $$\implies f(a) = f(b)$$.
>
> - $$\forall a \in G$$, $$f(a) = e_H$$ $$\ifif$$ $$a^{-1} b \in \ke{f}$$ -- Similar to above.
>
> ---
>
> - `Composition of homomorphisms is a homomorphism:` 
> 
>    $$f: G \to H$$, $$g: H \to K$$ are homomorphisms $$\imply$$ $$g \circ f: G \to K$$ is a homomorphism. -- By definition of composition of maps and homomorphisms.

### $$\colortext{2.1.2. Group Isomorphism and Automorphism}$$

### $$\colortext{Group Isomorphism and Isomorphic Groups}$$

- $$G, H$$ are groups

- $$f: G \to H$$ is a function

  $$\def$$ $$f: G \iso H$$ is an **group isomorphism** $$\difif$$ $$f$$ is a group homomorphism and a bijection.

  $$\def$$ $$G \iso H$$ $$\difif$$ $$\exists f: G \iso H$$

> - `Identity map is an isomorphism:` 
> 
>   $$\mathsf{id}_G: G \iso G$$ is an isomorphism. -- Check the definition above.
>
> - `Inverse of isomorphism is an isomorphism:` 
> 
>   $$f: G \to H$$ is an isomorphism $$\imply$$ $$f^{-1}: H \to G$$ is an isomorphism. -- By definition of inverse function and the inverse of homomorphism is a homomorphism.
>
> ---
>
> - `The composition of isomorphisms is an isomorphism:` 
> 
>   $$f: G \iso H$$, $$g: H \iso K$$ are isomorphisms $$\imply$$ $$g \circ f: G \iso K$$ is an isomorphism. -- By definition of composition of maps and isomorphisms.
>
> ---
>
> - `Isomorphic is an equivalence relation:` Check the definition of equivalence relation: `reflexive`, `symmetric`, `transitive`.
>
> ---
>
> - `Isomorphic groups means we could not distinguish them by their group structures.` -- since they are just the same collection of actions with different notations. 

*For now, we could abandon the notation ”$$=$$” to denote the isomorphism between groups and use “$$\iso$$” instead.*

### $$\colortext{Group Automorphisms}$$

- $$G$$ is a group.

  $$\def$$ **a group automorphism** $$\typied$$ $$\sigma: G \to G$$ $$\difif$$ $$\sigma$$ is a group isomorphism.


> - $$\then$$ $$\colortext{A group automorphism can be seen as a permutation of the elements of G.}$$
>
> ---
>
> - $$\then$$ $$\colortext{Identity Map Is an Automorphism:}$$ $$\operatorname{id}_G: G \to G$$ $$\defas$$ $$g \mapsto g$$ is an automorphism. 
> 
>    -- $$\op{Check}$$ the definition above.
>
> ---
>
> - $$\then$$ $$\colortext{Inverse of an Automorphism is an Automorphism:}$$ $$f: G \to G$$ is a group automorphism $$\ifif$$ $$f^{-1}: G \to G$$ is a group automorphism. 
> 
>    -- by definition of inverse maps and the inverse of group isomorphism is still a group isomorphism.
> 
>  ---
>
>  - $$\then$$ $$f: G \to G$$ $$\defas$$ $$g \mapsto g^{-1}$$ is an automorphism $$\ifif$$ $$G$$ is an abelian group. 
>  
>    -- $$\imply:$$ by definition of group automorphisms and inverse of the multiplication.
>
>    -- $$\limply:$$ Homomorphism implied by the abelian group and bijection implied by the uniqueness of inverse element.

### $$\colortext{Group of Group Automorphisms}$$

- $$G$$ is a group.

  $$\def$$ **a group of automorphisms of $$G$$** $$\wras$$ $$\mathrm{Aut}(G)$$ $$\defas$$ $$\{\sigma: G \to G \mid \sigma \text{ is an automorphism}\}$$ with composition of maps as group operation.

  $$\colortext{Well-definedness:}$$ $$\op{Check}$$ the `G1` to `G3` for $$\mathrm{Aut}(G)$$.

> - $$\then$$ $$\mathrm{Aut}(G) \leq S(G)$$.
>
>   -- $$\op{Apply}$$ $$\colortext{Subgroup Criterion}$$ on $$\mathrm{Aut}(G)$$.

### $$\colormath{2.2\;Group\; \sim subgroups}$$

### $$\colortext{2.2.1. Conjugations and Normal Subgroups}$$

### $$\colortext{Conjugations}$$

- $$G$$ is a group.

- $$g$$ $$\in G$$.

   $$\def$$ **a conjugation by $$g$$** $$\wras$$ $$c_g: G \to G$$ $$\defas$$ $$x \mapsto g x g^{-1}$$.

> - $$\then$$ $$\colortext{Conjugation is an Automorphism:}$$ 
> 
>    $$\forall g \in G$$, $$c_g: G \to G$$ $$\defas$$ $$x \mapsto g x g^{-1}$$ is an automorphism. 
>
>    -- $$\op{Check}$$ the definition of automorphism.

### $$\colortext{Conjugacy Classes}$$

- $$G$$ is a group.

- $$x, y$$ $$\in$$ $$G$$.

   - $$\def$$ **the conjugacy on $$G$$** $$\wras$$ $$\sim_{\mathrm{c}}$$ $$\typied$$ $$\sim$$ $$\defas$$ $$x \sim_{\mathrm{c}} y$$ $$\difif$$ $$\exists g \in G$$ $$\st$$ $$y = g x g^{-1}$$.

   -- $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `Reflexivity`, `Symmetry` and `Transitivity` for $$\sim_{\mathrm{c}}$$.

   - $$\def$$ **a conjugacy class** of $$x$$ $$\wras$$ $$Cl(x) \defas \{y \in G \mid x \sim_{\mathrm{c}} y\}$$.

> - $$\then$$ $$\colormath{In\;\mathrm{GL}(n, F), \;the\;conjugacy\;is\;the\;similarity\;relation\;between\;two\;matrices:}$$ $$\if$$ $$A, B \in \mathrm{GL}(n, F)$$ $$\then$$ $$A \sim B$$ $$\ifif$$ $$\exists P \in \mathrm{GL}(n, F)$$ $$\st$$ $$B = P A P^{-1}$$.
>
> ---
>
> - $$\then$$ $$\colortext{There Is No Conjugacy Class in Abelian Group:}$$ $$G$$ is an abelian group $$\ifif$$ $$\forall x, y \in G$$ with $$x \neq y$$, $$x \nsim_c y$$.    
>
>    --$$\imply:$$ for abelian group, since every element is commutative. $$\imply$$ conjugation is just doing nothing $$\imply$$ $$\op{Take}$$ any $$x, y \in G$$ with $$x \neq y$$ $$\implies$$ $$x \nsim_c y$$.
>
>    -- $$\limply:$$ $$\op{Contradiction:}$$ $$\op{Assume}$$ $$G$$ is not abelian $$\imply$$ $$\exists x, y \in G$$ with $$x \neq y$$ $$\st$$ $$xy= yx$$ $$\imply$$ $$x = y x y^{-1}$$ $$\implies$$ $$a \sim b$$, $$\contra$$.
>
>    -- · In other words, $$G$$ is abelian $$\ifif$$ every element in $$G$$ forms its own conjugacy class.


### $$\colortext{Group of Inner Automorphisms}$$

- $$G$$ is a group.

   $$\def$$ **a group of inner automorphisms of $$G$$** $$\wras$$ $$\mathrm{Inn}(G)$$ $$\defas$$ $$\{c_g: G \to G \mid g \in G, c_g \defas x \mapsto g x g^{-1} \}$$ with composition of maps as group operation.

   $$\colortext{Well-definedness:}$$ $$\op{Check}$$ the `G1` to `G3` for $$\mathrm{Inn}(G)$$.

> - $$\colortext{Group of Inner Automorphisms Is a Subgroup of Group of Group Automorphisms:}$$ $$\operatorname{Inn}(G) \leq \Aut{G}$$. 
> 
>    -- since a conjugation is a group automorphism and $$\op{Apply}$$ $$\colortext{Subgroup Criterion}$$ on $$\mathrm{Inn}(G)$$.

### $$\colortext{Normal Subgroups}$$

- $$G$$ is a group.

- $$N$$ $$\leq$$ $$G$$.

   $$\def$$ $$N$$ is a **normal subgroup** of $$G$$ $$\defas$$ $$N \trianglelefteq G$$ $$\difif$$ $$\forall g \in G$$, $$g N g^{-1} = N$$.

   `Well-definedness:` Apply $$\colortext{Subgroup Criterion}$$.

> -  In other words, A normal subgroup $$N$$ is **stable** under conjugations.
>
> ---
>
> - $$\then$$ $$\colortext{Normalilty means Every Element in the Normal Subgroup is Stable Under Any Conjugations:}$$ -- $$N \trianglelefteq G$$ $$\ifif$$ $$\forall g \in G$$ and $$\forall n \in N$$, $$g n g^{-1} \in N$$.
>
>   -- $$\ifif:$$ Immediate from the definition of normality. 
>
> ---
>
> - $$\then$$ $$\colortext{Normal Subgroup is the union of conjugacy class of G:}$$ $$N \norsub G$$ $$\ifif$$ $$\forall g \in G$$, $$Cl(g) \subseteq N$$ or  $$Cl(g) \cap N = \emptyset$$
>
>    -- $$\imply:$$ $$\op{Take}$$ any $$g \in G$$, $$\op{Assume}$$ $$\exists$$ $$n \in Cl(g) \cap N$$ $$\imply$$ for any $$c \in Cl(g)$$, $$\op{Write}$$ $$c = g n g^{-1}$$ $$\imply$$ $$c \in N$$.
>
>    -- $$\limply:$$ $$\op{Take}$$ any $$g \in G$$ and $$n \in N$$, $$\op{Write}$$ the conjugacy class of $$n$$ $$\wras$$ $$Cl(n)$$ $$\imply$$ $$Cl(n) \subseteq N$$ $$\imply$$ $$gng^{-1} \in Cl(n) \subseteq N$$.
>
>    --- To find normal subgroups: $$\op{Find}$$ all conjugacy class $$\textcolor{pink}{\rightarrow}$$ $$\op{Retain}$$ those with order being a factor of $$\abs{G}$$ $$\textcolor{pink}{\rightarrow}$$ $$\op{Check}$$ $$\if$$ they are subgroups(apply $$\colortext{Subgroup Criterion}$$).

### $$\colortext{Simple Groups}$$

- $$G$$ is a group.

   $$\def$$ a **simple group** $$\typied G$$ $$\difif$$ $$G \neq \{e\}$$ and $$\forall N \trianglelefteq G$$, either $$N = \{e\}$$ or $$N = G$$.

> - $$\then$$ $$\colortext{Simple group can not be "factored":}$$ like prime numbers, simple groups can not be ”factored”. A group that is not simple can be factored in to two smaller groups, namely a nontrivial normal subgroup and the corresponding quotient group, which is introduced as following.

### $$\colortext{Quotient Groups}$$

- $$G$$ is a group.

- $$N$$ $$\trianglelefteq$$ $$G$$.

   $$\def$$ **the quotient group of $$G$$ divided by $$N$$** $$\wras$$ $$G / N$$ $$\defas$$ $$G / \sim_{\mathrm{coset}}$$ $$\defas$$ $$\{g N \mid g \in G\}$$ with the group operation $$*: G / N \times G / N \to G / N$$ $$\defas$$ $$(g N, h N) \mapsto (g h) N$$ -- Well-defined by normality of $$N$$ and `G1: Associativity` of $$G$$.

   $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `G1` to `G3` for $$G / N$$.

> - $$\then$$ $$\colortext{Why is It Called Quotient?:}$$ the reason $$G / N$$ is called a quotient group comes form division of integers. When we divide an integer, we regroup the number of into a certain number of collections with the same number of objects. The quotient group is the same idea, the quotient group structure is used to form a natural "regrouping", which are the cosets of $$N$$ in $$G$$. Like the prime number has only 2 divisor, which are $$1$$ and itself. The simple group has only 1 quotient group $$\defas$$ $$\{G \mid G \textsf{ is a simple group}\}$$ "divided" by its trivial normal subgroup and itself, whose cosets are simple group itself. 
>
> ---
>
> - $$\then$$ $$\colortext{the Condition of Normality is Required by Respectfulness of *:}$$ $$\op{Check}$$ that $$*$$ respects the quotient structure. ($$\op{Consider}$$ $$\if$$ $$N$$ is not normal). Regardless of whether left or right cosets used in the definition of quotient set, guaranteed by conjugacy criterion.
>
> ---
>
> - $$\then$$ $$\colortext{Any Quotient Group Deduced by an Abelain Group is Abelain:}$$ $$\if$$ $$G$$ is an abelian group $$\then$$ $$\\forall N \trianglelefteq G$$, $$G / N$$ is an abelian group.
>
>   -- $$\op{Take}$$ any $$g N, h N \in G / N$$ $$\imply$$ $$g N * h N = (g h) N = (h g) N = h N * g N$$.
>
> ---
>
> - $$\then$$ $$\colortext{Automorphism Deduces Isomorphism of Quotient Groups:}$$ $$\if$$ $$N \norsub G$$ and $$\sigma: G \to G$$ is a group automorphism $$\then$$ $$G / N \iso G / \sigma(N)$$.
>
>    -- $$\op{Consider}$$ a map $$\phi: G / N \to G / \sigma(N)$$ $$\defas$$ $$g N \mapsto \sigma(g) \sigma(N)$$, which is a group isomorphism. $$\op{Check}$$ the definition of group isomorphism.
>
> ---
>
>  - $$\then$$ $$\colortext{Exampls of Quotient Groups:}$$ 
> 
>     - $$\then$$ $$\colortext{Quotient Spaces (also see in Linear Algebra):}$$ the quotient space of a vector space is the quotient group of the vector space by its subspace with addition.
>
>      - $$V$$ is a vector space over some $$\mathcal{F}$$.
>
>      - $$W$$ is a subspace of $$V$$.
>
>       $$\def$$ **the quotient space of $$V$$ by $$W$$** $$\wras$$ $$V / W$$ $$\defas$$ $$V / \sim_{\mathrm{coset}}$$ $$\defas$$ $$\{v + W \mid v \in V\}$$ with the group operation $$* \defas +: V / W \times V / W \to V / W$$ $$\defas$$ $$(v + W, w + W) \mapsto (v + w) + W$$.
>
>    - $$\then$$ $$\colortext{Reminders of Integer Division / Addtive Integers Mod n:}$$ the reminder of integer division is the quotient group of the integers by the integers and is isomorphic to the integers modulo the divisor.
>
>     - $$n \in \N^+$$.
>
>     - $$n \Z$$ $$\defas$$ $$\{n k \mid k \in \Z\} \trianglelefteq \Z$$. -- $$\Z$$ is an abelian group.
>
>       $$\def$$ **the quotient group of $$\Z$$ by $$n \Z$$** $$\wras$$ $$\Z / n \Z$$ $$\defas$$ $$\{k + n \Z \mid k \in \Z\}$$ with the group operation $$*: \Z / n \Z \times \Z / n \Z \to \Z / n \Z$$ $$\defas$$ $$(k + n \Z, l + n \Z) \mapsto (k + l) + n \Z$$.
>
>        -- $$\then$$ $$\Z / n \Z$$ $$\iso$$ $$\Z_n$$.
>
>        -- · $$\op{Consider}$$ a map $$\phi: \Z / n \Z \to \Z_n$$ $$\defas$$ $$k + n \Z \mapsto [k]_n$$,  which is a group isomorphism. $$\op{Check}$$ the definition of group isomorphism.
>
>    - $$\then$$ $$\colortext{Real Numbers Mod the Integers:}$$ the quotient group of the real numbers by the integers is isomorphic to the circle group.
>
>      - $$\def$$ **the quotient group of $$\R$$ by $$\Z$$** $$\wras$$ $$\R / \Z$$ $$\defas$$ $$\{x + \Z \mid x \in \R\}$$ with the group operation $$*: \R / \Z \times \R / \Z \to \R / \Z$$ $$\defas$$ $$(x + \Z, y + \Z) \mapsto (x + y) + \Z$$.
>
>     - $$\def$$ **the circle group** $$\wras$$ $$S^1$$ $$\defas$$ $$\{z \in \C \mid |z| = 1\}$$ with the group operation $$*: S^1 \times S^1 \to S^1$$ $$\defas$$ $$(z_1, z_2) \mapsto z_1 z_2$$.
>
>       -- $$\then$$ $$\R / \Z$$ $$\iso$$ $$S^1$$.
>
>       -- · $$\op{Consider}$$ a map $$\phi: \R / \Z \to S^1$$ $$\defas$$ $$x + \Z \mapsto e^{2 \pi i x}$$, which is a group isomorphism. $$\op{Check}$$ the definition of group isomorphism.

### $$\colortext{Cannonical Surjective Homomorphism}$$

- $$G$$ is a group.

- $$N$$ $$\trianglelefteq$$ $$G$$.

   $$\def$$ a **cannonical surjective group homomorphism** $$\defas$$ $$\phi: G \rightarrow G / N$$ $$\defas$$ $$g \mapsto g N$$.

> - `Cannonical projection homomorphism is a surjective group homomorphism:`
>
>    -- `Surjectivity:` Natural from its definition.
>
>    -- `Homorphism:` Natural from the its own definition and the group operation of quotient group.
>
> ---
>
> - `Every normal subgourp is kernel of some group homomorphism:`
>
>   $$\phi$$ is defined as above $$\imply$$ $$\ke(\phi) = N$$. -- By definition of Kernel and the properties of cosets. 
>
>   -- This means for any $$N \norsub G$$, we can always find a group homorphism with it as its kernel by defining its corresponding cannonical projection homomorphism.
>
> ---
>
> - $$\abs{G / N}$$ $$= Frac{\abs{G}}{\abs{N}}$$ --  By Lagrange's Theorem.  

### $$\colortext{2.3 First Isomorphism Theorem and Correspondence Theorem for Groups}$$

### $$\colortext{2.3.1. First Isomorphism Theorem for Groups}$$

### $$\colortext{Theorem 2.3.1. First Isomorphism Theorem for Groups}$$

- $$G, H$$ are groups.

- $$f: G \to H$$ is a group homomorphism.

   - $$\then$$ $$\ke{f} \trianglelefteq G$$.

   - $$\then$$ $$\im{f} \leq H$$.

   - $$\then$$ $$\exists \psi: G / \ke{f} \rightarrow \im{f}$$ $$\defas$$ $$g \ke{f} \mapsto f(g)$$ $$\st$$ $$\psi$$ is a group isomorphism and $$G / \ke{f} \iso \im{f}$$.
  
   - $$\then$$ $$\abs{G} = \abs{\ke{f}} \abs{\im{f}}$$.

#### $$\colortext{Proof:}$$

- `Ker(f) is normal in G:` 
   
   - `Subgroup:` Known result.
   
    - `Normality:` For any $$x \in \ke{f}$$ $$g \in G$$,

      $$
        \begin{aligned}
        f(g x g^{-1}) & = f(g) f(x) f(g^{-1})\\
                      & = f(g) e_H f(g^{-1})\\
                      & = f(g) f(g^{-1}) \\
                      & = f(g g^{-1}) \\
                      & = f(e_G) \\
                      & = e_H
        \end{aligned}
        $$
      

    Hence, $$g x g^{-1} \in \ke{f}$$. Therefore, $$\ke{f}$$ is a normal subgroup of $$G$$. 

- `Im(f) is a subgroup of H:` Known result, since $$f$$ is a homomorphism.

   - `The existence of isomomorphism:` 

     - `Well-definess:` $$\psi$$ is well-defined since $$f$$ is constant on each coset of $$\ke{f}$$.

     - `Homomorphism:` For any $$g_1 \ke{f}$$ and $$g_2\ke{f} \in G/\ke{f}$$,
  
        $$
        \begin{aligned}
        \psi(g_1\ke{f}g_2\ke{f}) &= \phi(g_1g_2\ke{f}) \\
        &= f(g_1g_2) = f(g_1)f(g_2) \\
        &= \psi(g_1\ke{f})\psi(g_2\ke{f})
        \end{aligned}
        $$
     
     - `Bijectivity:`
       
       - `Surjectivity:` Natural from its own definition.

       - `Injectivity:` $$\ke(\psi) = \{e_{G/\ke{f}}\}$$ $$\imply$$ $$\psi$$ is injective.

           For any $$g \in \ke{\psi}$$,

           $$
           \psi(g) = f(g) = e_H
           $$

           Therefore, $$g \in \ke{f}$$ $$\implies$$ $$g\ke{f} = \ke{f}$$. Hence, $$\ke(\psi) = \{e_G \ke{f}\}$$.

   - `The order of G:` By above, $$Frac{\abs{G}}{\abs{\ke{f}}} = \abs{G/\ke{f}} = \abs{\im{f}}$$.
  
> - In other words, every homomorphic image of a group is isomorphic to a quotient group of the group.
>
> ---
> 
> - $$f$$ is surjective $$\imply$$ $$G/\ke{f} \iso H$$ -- by First Isomorphism Theorem with $$\psi: G/\ke{f} \to H$$ $$\defas$$ $$g \ke{f} \mapsto f(g)$$ $$\forall g \in G$$.
>
> ---
>
> - $$N \norsub G$$ $$\ifif$$ $$\exists f$$ such that $$N = \ke{f}$$ -- by First Isomorphism Theorem with $$\psi: G \to G/N$$ $$\defas$$ $$g \mapsto g N$$ $$\forall g \in G$$. 
>
> ---
> 
> - There are similar theorems for monoids, vector spaces, rings, modules, etc. -- Just replace the group homomorphism with the corresponding homomorphism.

### $$\colortext{Applications of First Isomorphism Theorem for Groups}$$

- $$G$$ is a group.

   - $$\then$$ $$G/G \iso \{e\}$$ -- by First Isomorphism Theorem with $$\psi: G/G \to \{e\}$$ $$\defas$$ $$g \mapsto e$$ $$\forall g \in G$$.

   - $$\then$$ $$G/\{e\} \iso G$$. -- by First Isomorphism Theorem with $$\operatorname{id}:G/\{e\} \to G$$ $$\defas$$ $$g \mapsto g$$ $$\forall g \in G$$.

   - $$\then$$ $$\mathrm{GL}_n(\R)/\mathrm{SL}_n(\R) \iso \R^+$$ -- by First Isomorphism Theorem with $$\operatorname{det}: GL_n(\R)/SL_n(\R) \to \R^+$$ $$\defas$$ $$g \mapsto \operatorname{det}(g)$$

   - $$\then$$ $$\Z_n \iso \Z / n \Z$$ -- by first Isomorphism Theorem with $$\psi: \Z \to \Z_n$$ $$\defas$$ $$m \mapsto g \mod n$$ $$\forall m \in \Z$$.


### $$\colortext{Coorresponding Set Functions}$$

- $$G, H$$ are groups.

- $$f: G \to H$$ is a group homomorphism.

   $$\def$$ corresponding set functions $$\defas$$

   - $$f_{\operatorname{Im}}: \mathcal{P}(G) \rightarrow \mathcal{P}(H)$$ $$\defas$$ $$S\mapsto \{f(s) \in H \mid s \in S\}$$.

   - $$f_{\operatorname{Pre}}: \mathcal{P}(H) \rightarrow \mathcal{P}(G)$$ $$\defas$$ $$T\mapsto \{g \in G \mid f(g) \in T\}$$.

> - `Group homomorphisms map subgroups to subgroups:`
>
>    - $$\forall S \leq G$$, $$f_{\operatorname{Im}}(S) \leq H$$. -- Apply $$\colortext{Subgroup Criterion}$$.
>
>    - $$\forall S \leq H$$, $$f_{\operatorname{Pre}(S)} \leq G$$. -- Apply $$\colortext{Subgroup Criterion}$$.
>
> ---
>
> - `Surjective group homomorphisms map normal subgroups to normal subgroups:`
>
>    $$f: G \to H$$ is a surjective group homomorphism $$\imply$$ $$\forall N \trianglelefteq G$$, $$f_{\operatorname{Im}}(N) \trianglelefteq H$$. 
>
>    -- `Subgroup:` Known above.
>
>    -- `Normality:` For any $$m \in f_{\operatorname{Im}}(N)$$, we need to show $$h m h^{-1} \in f_{\operatorname{Im}}(N)\; \forall h \in H$$. Write $$m = f(n)$$ for some $$n \in N$$. By surjecitive, we can write every $$h \in H$$ as $$f(g)$$ for some $$g \in G$$. Calculate $$f(g) f(n) f(g)^{-1} = f(g n g^{-1})$$, where $$g n g^{-1} \in N$$ by normality of $$N$$. Hence $$h m h^{-1} \in f_{\operatorname{Im}}(N)$$.
>
>    --- The surjectiviey is necessary, consider $$N = G \leq H$$ with $$f = \operatorname{id}$$.
>
>    $$f: G \to H$$ is a group homomorphism $$\imply$$ $$\forall N \norsub H, f_{\operatorname{Pre}}(N) \norsub G$$. 
>
>    -- `Subgroup:` Known above.
>
>    -- `Normality:` For any $$m \in f_{\operatorname{Pre}}(N)$$, we need to show $$g m g^{-1} \in f_{\operatorname{Pre}}(N) \; \forall g \in G$$. Calculate $$f(g m g^{-1}) = f(g) f(m) f(g)^{-1} \in N$$ since $$f(m) \in N$$ and $$N$$ is normal.


### $$\colortext{Theorem 2.2.2. Correspondence Theorem for Groups}$$

- $$G$$ is a group.

- $$N$$ $$\trianglelefteq$$ $$G$$.

- $$\mathcal{N} \defas \{H \mid N \subseteq H \leq G\}$$ -- The set of all subgroups $$S$$ of $$G$$ that contain $$N$$.

- $$\mathcal{Q} \defas \{Q \mid Q \leq G/N\}$$ -- The set of all subgroups of $$G /N$$.

- $$\phi: G \to G/N$$ is a cannonical surjective homomorphism $$\defas$$ $$g \mapsto g N$$.

- $$f_{\operatorname{Im}}: \mathcal{P}(G) \rightarrow \mathcal{P}(G/N)$$ is the corresponding set function of $$\phi$$.

   - $$\then$$ $$\forall S \leq G$$ and $$S \supseteq N$$, $$N \trianglelefteq S$$.

   - $$\then$$ $$\forall S \leq G$$ and $$N \trianglelefteq S$$, $$f_{\operatorname{Im}}(S) = S/N \leq G/N$$.

   - $$\then$$ $$f_{\operatorname{Im}}: \mathcal{N} \to \mathcal{Q}$$ is a **bijection** 

   - $$\then$$ $$\forall S$$ such that $$N \trianglelefteq S \leq G$$, $$S \trianglelefteq G$$ $$\ifif$$ $$f_{\operatorname{Im}}(S) \trianglelefteq G/N$$.

   `Proof:` TODO

> - In other words, the algebraic structure of the subgroups of $$G / N$$ is in one-to-one correspondence with the algebraic structure of the subgroups of $$G$$ that contain $$N$$.
>
> ---
> 
> - If $$A, B \in \mathcal{N}$$
>
>   - $$\imply$$ $$A \subseteq B$$ $$\ifif$$ $$A/N \subseteq B/N$$.
>
>   - $$\imply$$ If $$A \subseteq B$$, then $$\abs{B : A} = \abs{B/N : A/N}$$, where $$\abs{B : A}$$ is the index of $$A$$ in $$B$$.
>
>   - $$\imply$$ $$(A \cap B) /N =  A/N \cap B/N$$.
>
>   - $$\imply$$ $$A \trianglelefteq G$$ $$\ifif$$ $$A/N \trianglelefteq G/N$$.
>
> ---
>
> - There are similar theorems for rings, vector spaces, and algebras. -- Just replace the group homomorphism with the corresponding homomorphism.