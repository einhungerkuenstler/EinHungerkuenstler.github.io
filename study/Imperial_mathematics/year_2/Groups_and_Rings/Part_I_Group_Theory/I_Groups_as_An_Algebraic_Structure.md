---
title: I. Groups as an Algebraic Structure
layout: simple
---

$$\gdef\def{\pink{\operatorname{def}}}$$
$$\gdef\dfs{\pink{:=}}$$
$$\gdef\ifif{\pink{\iff}}$$
$$\gdef\imp{\pink{\implies}}$$
$$\gdef\diff{\pink{:\longleftrightarrow}}$$
$$\gdef\limp{\pink{\Longleftarrow}}$$
$$\gdef\st{\pink{\texttt{s.t.}}}$$
$$\gdef\the{\pink{\Rightarrow}}$$
$$\gdef\wrs{\pink{=:}}$$
$$\gdef\typ{\pink{:\in}}$$
$$\gdef\if{\pink{\texttt{if}}}$$
$$\gdef\inner#1#2{\left\langle\strut#1,#2\right\rangle}$$
$$\gdef\hby{\pink{- :}}$$
$$\gdef\norm#1{\left\Vert\strut#1\right\Vert}$$
$$\gdef\abs#1{\left\vert\strut#1\right\vert}$$
$$\gdef\op#1{\pink{\operatorname{#1}}}$$
$$\gdef\gen#1{\left \langle #1 \right \rangle}$$
$$\gdef\geni#1{\left( #1 \right)}$$
$$\gdef\contra{\pink{\texttt{Opq!}}}$$
$$\gdef\im#1{\operatorname{Im}(#1)}$$
$$\gdef\ke#1{\operatorname{Ker}(#1)}$$
$$\gdef\ord#1{\operatorname{ord}(#1)}$$
$$\gdef\sgn{\operatorname{sgn}}$$
$$\gdef\Aut#1{\operatorname{Aut}(#1)}$$
$$\gdef\mod{\operatorname{mod}}$$
$$\gdef\ideal{\triangleleft}$$
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
$$\gdef\colortext#1{\pink{\textsf{{#1}}}}$$
$$\gdef\colormath#1{\pink{\mathsf{{#1}}}}$$
$$\gdef\rank{\mathrm{rank}}$$
$$\gdef\null{\mathrm{null}}$$
$$\gdef\det{\mathrm{det}}$$
$$\gdef\gcd{\mathrm{gcd}}$$
$$\gdef\lcm{\mathrm{lcm}}$$

### $$\colortext{1.1 Groups, Subgroups and Cosets}$$

### $$\colortext{Groups}$$

- $$G$$ is a set.

- $$\cdot: G \times G \to G$$ is a group operation on $$G$$.

  $$\def$$ **a group** $$\wrs$$ $$(G ,\cdot)$$ $$\diff$$ $$(G,\cdot)$$ satisfies the following 3 axioms:

   - `G1: Associativity:` $$\forall a, b, c \in G, (a \cdot b) \cdot c = a \cdot (b \cdot c)$$.

   - `G2: Identity:` $$\exists! e \in G, \forall a \in G, e \cdot a = a \cdot e = a$$.

   - `G3: Inverse:` $$\forall g \in G, \exists! g^{-1} \in G, g \cdot g^{-1} = g^{-1} \cdot g = e$$.

> - $$\the$$ for the following, we will not write the group operation explicitly, but we assume that it is clear from the context Instead, we use multiplicative notation for the group operation. We will also attreviate "$$(G,\cdot)$$ is a group" to "$$G$$ is a group". Sometimes, to explicitly specify the group operation, we will write "$$G$$ with $$\cdot$$ is a group'' as $$(G, \cdot)$$.
> 
> - $$\the \colortext{Uniqueness of the Identity and Inverse:}$$
>
>    - `G2` $$\imp$$ the uniqueness of $$e$$. 
>     
>        -- $$\op{Contradiction}$$.
>
>    - `G3` $$\imp$$ the uniqueness of $$g^{-1}$$. 
>    
>        -- $$\op{Contradiction}$$.


### $$\colortext{Proposition 1.1.1. Cancellation Law}$$

- $$G$$ is a group.

  - $$\the$$ $$\colortext{Left and Right Cancel:}$$ $$\if$$ $$a, b, c \in G$$ with $$a  b = a c$$ or $$b a = c a$$ $$\the$$ $$b = c$$. 

  - $$\the$$ $$\colortext{Identity Cancel:}$$ $$\if$$ $$x, y \in G$$ with $$xy = y$$ or $$y x = y$$ $$\the$$ $$x = e$$ 

  $$\colortext{Proof:}$$

   - $$\colortext{Left and Right Cancel:}$$ Left multiply by $$a^{-1}$$ or right multiply by $$a^{-1}$$.

   - $$\colortext{Identity Cancel:}$$ Right multiply by $$y^{-1}$$ or left multiply by $$y^{-1}$$. 

### $$\colortext{Abelian Groups}$$

- $$G$$ is a group.
    
   $$\def$$ **an abelian group** $$\typ G$$ $$\diff$$ $$G$$ satisfies the following extra axiom:

   - `AG4: Commutivity:` $$\forall x, t \in G, xy = yx$$.

### $$\colortext{Order of a Group}$$

- $$G$$ is a group.

   $$\def$$ **the order of a group** $$\wrs$$ $$\abs{G} \dfs \operatorname{card}(G)$$.

### $$\colortext{Order of an Element in a Group}$$

- $$G$$ is a group.

   $$\def$$ **the order of an element of a group** $$\wrs \mathrm{ord}: G \to \N^+ \cup \{\infty\}$$ $$\dfs$$ $$\begin{cases} \min\set{n \in \N^+ \mid g^{n} = e} & \if\; \exists n \in \N \;\st\; g^{n}= e \\ \infty & \textsf{otherwise} \end{cases}$$.

> - $$\the$$ $$\if$$ $$G$$ is a finite group with $$\abs{G} = n$$ for some $$n \in \N^+$$ $$\the$$ $$\forall g \in G, \ord{g}\leq n$$. $$\hby$$ follows from **[Pigeonhole Principle](https://en.wikipedia.org/wiki/Pigeonhole_principle)**.

### $$\colortext{Subgroups}$$

- $$(G,\cdot)$$ is a group.

- $$H$$ $$\subseteq$$ $$G$$.

   - $$\def$$ **a subgroup of $$G$$** $$\wrs$$ $$H \leq G$$ $$\typ H\subseteq G$$ $$\diff$$ $$(H, \cdot)$$ satisfies the following 3 axioms:

      - `SG1: Identity:` $$e \in H$$.

      - `SG2: Inverse:` $$\forall g \in H, g^{-1} \in H$$.

      - `SG3: Closure:` $$\forall x, y \in H, xy \in H$$.
  
   - $$\def$$ **a trivial subgroup of $$G$$** $$\dfs$$ $$\set{e} \leq G$$. -- $$\op{Check}$$ `SG1` to `SG3` for $$\set{e}$$.

   - $$\def$$ **a non-proper subgroup of $$G$$** $$\dfs$$ $$G \leq G$$. -- $$\op{Check}$$ `SG1` to `SG3` for $$G$$.

> - $$\the$$ $$\if$$ $$(G,\cdot)$$ is a group and $$H \leq G$$ $$\the$$ $$(H, \cdot)$$ is a group.
>
>    -- $$\op{Check}$$ `G1` to `G3` for $$H$$.
> 
> ---
>
> - $$\the$$ $$\colortext{Subgroups Relations Define A Partial Order on the Set Consisting of Subgroups of A Group:}$$ "$$\leq$$" is a partial order on $$\set{H\mid H \leq G, G \textsf{ is a group}}$$. 
>  
>    -- $$\op{Check}$$ `Reflexivity`, `Anti-symmetry` and `Transitivity`.
>
> ---
>
> - $$\the$$ $$\colortext{Subgroup Criterion:}$$ $$H \leq G$$ $$\ifif$$ $$H \neq \emptyset$$ and $$\forall x, y \in H, x y^{-1} \in H$$. 
> 
>    -- $$\imp:$$ by the definition of subgroup. 
> 
>    -- $$\limp:$$ Show `Identity`, then `Inverse` and `Closure` follows.

### $$\colortext{Cosets}$$

- $$G$$ is a group

- $$H$$ $$\leq$$ $$G$$. 
  
   - $$\def$$ the **left coset** of $$H$$ in $$G$$ by some $$g \in G$$ $$\wrs$$ $$g H$$ $$\typ gH \subseteq G$$ $$\dfs \set{g h \mid h \in H}$$.

   - $$\def$$ the **right coset** of $$H$$ in $$G$$ by some $$g \in G$$ $$\wrs$$ $$H g$$ $$\typ Hg \subseteq G$$ $$\dfs \set{h g \mid h \in H}$$.  

>  - $$\the \colortext{In the Same Left/Right Sosets}$$ $$\ifif$$ $$\colortext{Substraction from Left/Right Gives An Element of Subgroup:}$$ $$\forall x, y \in G$$, $$x$$ and $$y$$ $$\in gH$$ (or $$Hg$$) for some $$g \in G$$ $$\ifif$$ $$x^{-1} y \in H$$.  
> 
>    -- $$\imp:$$ $$\if$$ $$x, y \in gH$$ $$\the$$ $$x = g h_1, y = g h_2$$ for some $$h_1, h_2 \in H$$, so $$x^{-1} y = h_1^{-1} h_2 \in H$$.
> 
>    -- $$\limp:$$ $$\op{Set}$$ $$g \dfs x^{-1} y \in H$$ $$\imp$$ $$x = x e$$, $$y = x g$$.
> 
>  --- 
>
> - $$\the$$ $$\colortext{For Every Element in a Left/Right Coset}$$ $$\ifif$$ $$\colortext{Generates the Same Left/Right Coset:}$$ $$\forall x, y \in G$$, $$xH = yH$$ (or $$Hx = Hy$$)  $$\ifif$$ $$x \in yH$$ (or $$x \in H y$$).
>
>   -- $$\imp:$$ $$\if$$ $$xh \in xH$$ for some $$h \in H$$. Since $$xH = yH$$, $$xh \in yH$$ $$\imp$$ $$xh = yh'$$ for some $$h' \in H$$ $$\imp$$ $$x = y(h'h^{-1}) \in yH$$.
>
>   -- $$\limp:$$ $$\if$$ $$x \in yH$$, then $$x = yh$$ for some $$h \in H$$. $$\imp$$ $$\forall s \in H$$, $$xs = y(hs) \in yH$$ $$\imp$$ $$xH \subseteq yH$$. Similarly, $$yH \subseteq xH$$.
> 
>  --- 
>
> - $$\the$$ $$\colortext{All Left/Right Cosets Form a Partition of the Whole Group:}$$ $$\forall x \in G$$, $$\exists! y \in G$$ $$\st$$ $$x \in yH$$ and $$\exists! y \in G$$, $$\st$$ $$x \in Hy$$. 
>
>   -- $$\op{Take}$$ any $$x \in G$$ with $$x \in yH$$ and $$x \in zH$$ for some $$y, z \in G$$ $$\imp$$ $$y = z$$ by above.
>
>   -- · $$\the$$ $$\def$$ **an equivalence relation** on a group $$G$$ $$\wrs$$ $$\sim_{\mathrm{coset}}$$ $$\typ$$ $$\sim$$ $$\dfs$$ $$x \sim_\mathrm{coset} y$$ $$\diff$$ $$x,y \in gH$$ for same $$g \in G$$.
>   --- · $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `Reflexivity`, `Symmetry` and `Transitivity`.
> 
> ---
> 
> - $$\the$$ $$\colortext{All Left/Right Cosets Have the Same Cardinality:}$$ $$\forall g \in G$$, $$\abs{gH} = \abs{Hg} = \abs{H}$$. 
> 
>    -- $$\op{Check}$$ that the map $$h \mapsto gh(hg)$$ is a bijection from $$H$$ to $$aH(Ha)$$.
>
> ---

> For the following statements about **"could be seen"**, actually it means that there is a **group isomorphism** between the two groups, which we will discuss later and the relation $$=$$ dose not mean that the equality holds in the set theory sense. We just use “$$=$$” to denote the **"isomorphism"**.

### $$\colortext{1.2 Some Abstract Groups}$$

### $$\colortext{Product Groups}$$

- $$(G, \cdot_G)$$ and $$(H, \cdot_H)$$ are groups.

   $$\def$$ $$\cdot: G \times H \to G \times H$$ $$\dfs$$ $$(g, h) \mapsto (g \cdot_G h, g \cdot_H h)$$.

   $$\def$$ **a product group** $$\wrs$$ $$G \times H$$ $$\dfs$$ $$(G \times H, \cdot)$$.

   $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `G1` to `G3` for $$G \times H$$.

> - $$\the$$ $$\colortext{Trivial Product Groups:}$$ $$\set{(g, e) \mid g \in G} \leq G \times H$$ and $$\set{(e, h) \mid h \in H} \leq G \times H$$.
> 
>    -- $$\op{Apply}$$ $$\colortext{Subgroup Criterion}$$ on $$\set{(g, e)}$$ and $$\set{(e, h)}$$.
>
> ---
>
> - $$\the$$ $$G$$ and $$H$$ are abelian $$\ifif$$ $$G\times H$$ is abelian. 
>
>   -- by definition of product groups and abelian groups.

### $$\colortext{Permutations}$$

- $$n \in \N^+$$.

- $$X$$ is a set with $$\card{X} = n$$.

   $$\def$$ **a permutation on $$X$$** $$\wrs$$ $$\sigma: X \to X$$ $$\diff$$ $$\sigma$$ is a bijection.

> - $$\the$$ $$\colortext{Permutations Notations:}$$ 
> 
>    -- $$X \dfs \{1, 2, 3, 4, 5\}$$.
>
>    -- · $$\colortext{Two-row Notation:}$$ the permutation $$\sigma$$ could also be written in **two-row notation**, for instance $$\sigma: X \to X \dfs n \mapsto \begin{cases} n + 1& \if\; n < 5 \\ 1 & \if \;n = 5 \end{cases}$$ $$\wrs$$ $$\begin{pmatrix} 1 & 2 & 3 & 4 & 5 \\ 2 & 3 & 4 & 5 & 1 \end{pmatrix}$$.
> 
>    -- · $$\colortext{Cycle Notation:}$$ the permutation $$\sigma$$ could be written as **a product of cycle notation**, for instance $$\sigma \dfs \begin{pmatrix} 1 & 2 & 3 & 4 & 5 \\ 2 & 3 & 1 & 5 & 4 \end{pmatrix}$$ $$\wrs$$ $$(1 2 3)(4 5)$$.
> 
>    -- · $$\colortext{Permutation Matrices:}$$ the permutation $$\sigma$$ could be written as **a permutation matrix**, for instance $$\sigma \dfs \begin{pmatrix} 1 & 2 & 3 & 4 & 5 \\ 2 & 3 & 1 & 5 & 4 \end{pmatrix}$$ $$\wrs$$ $$\begin{pmatrix} 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 1 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 1 & 0 \end{pmatrix}$$.

### $$\colortext{Symmetric Groups}$$

- $$X$$ is a set.

   $$\def$$ **a symmetric group** on $$X$$ $$\wrs$$ $$S(X)$$ $$\dfs$$ $$\{\sigma \mid \sigma: X \to X \textsf{ is a permutation}\}$$ with composition of maps as group operation.

   $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `G1` to `G3` for $$S(X)$$.

> - $$\the$$ $$\if$$ $$n \in \N^+$$ and $$X$$ is a finite set with $$\card{X} = n$$ $$\the$$ $$\abs{S(X)} = n!$$ 
> 
>    -- to count the number of permutations of $$X$$, we can first choose the image of $$1$$ from $$n$$ elements, then choose the image of $$2$$ from $$n - 1$$ elements, and so on.

### $$\colortext{Sign of a Permutation}$$

- $$n \in$$ $$\N^+$$.

- $$X$$ is a finite set with $$\card{X} = n$$.

- $$S(X)$$ is the symmetric group defined on $$X$$.

  - $$\def$$ **the inversion number of $$\sigma$$** $$\wrs$$ $$\mathrm{inv}: S(X) \to \N$$ $$\dfs$$ $$\sigma \mapsto \abs{\{(i, j) \mid i, j\in \{1,2, \dots, n\} \textsf{ with } i < j\textsf{ and }\sigma(i) > \sigma(j)\}}$$.
  
  - $$\def$$ **the sign of a permutation** $$\wrs$$ $$\sgn: S(X) \to \{-1, 1\}$$ $$\dfs$$ $$\sigma \mapsto (-1)^{\mathrm{inv}(\sigma)}$$.
  
  - $$\def$$ **an even permutation** $$\typ$$ $$\sigma \in S(X)$$ $$\diff$$ $$\sgn(\sigma) = 1$$.
  
  - $$\def$$ **an odd permutation** $$\typ$$ $$\sigma \in S(X)$$ $$\diff$$ $$\sgn(\sigma) = -1$$.

> - $$\the$$ $$\forall \sigma, \tau \in S(X)$$, $$\sgn(\sigma \circ \tau) = \sgn(\sigma) \cdot \sgn(\tau)$$.
>
>    -- by the definition of sign of a permutation.
>
> - $$\the$$ $$\forall \sigma \in S(X)$$, $$\sgn(\sigma^{-1}) = \sgn(\sigma)$$. 
>
>   -- $$\op{Take}$$ any $$\sigma \in S(X)$$, $$\op{Calculate}$$ $$\sgn(e) = \sgn(\sigma \circ \sigma^{-1}) = \sgn(\sigma) \cdot \sgn(\sigma^{-1}) = 1$$.
>
> ---
>
> - $$\the$$ $$\colortext{Using the Sign of a Permutation to Define Determinant of a Matrix:}$$
>
>   - $$n \in \N^+$$.
>
>   - $$A \in M_{n \times n}(F)$$.
>
>    $$\def$$ **the determinant of $$A$$** $$\wrs$$ $$\det: M_{n \times n}(F) \to F$$ $$\dfs$$ $$\dfs (a_{ij}) \mapsto \sum_{\sigma \in S_n} \sgn(\sigma) \prod_{i = 1}^{n} a_{i \sigma(i)}$$.

### $$\colortext{Alternating Groups}$$

- $$n \in \N^+$$.

- $$X$$ is a finite set with $$\card{X} = n$$.

- $$S(X)$$ is the symmetric group defined on $$X$$.

   $$\def$$ **an alternating group** $$\wrs$$ $$A_n$$ $$\typ$$ $$A_n \leq S(X)$$ $$\diff$$ $$A_n \dfs \{\sigma \in S(X) \mid \sgn(\sigma) = 1\}$$.

   $$\colortext{Well-definedness:}$$ Check `G1` to `G3` for $$A_n$$ and $$\op{Apply}$$ $$\colortext{Subgroup Criterion}$$ on $$A_n$$. 

> - $$\the$$ $$\op{Note}$$ that $$S(X) \setminus A_n$$ $$= \{\sigma \in S(X) \mid \sgn(\sigma) = -1\}$$ is not a subgroup of $$S(X)$$.
>
>  -- since the composition of any two odd permutations is an even permutation.

### $$\colortext{Cyclic Group Generated by an Element}$$

- $$G$$ is a group.

- $$g \in$$ $$G$$.

    $$\def$$ **the cyclic group generated by $$g \in G$$ $$\wrs$$ $$\langle g \rangle$$ $$\dfs$$ $$\set{g^n \mid n \in \Z}$$ with $$\cdot: \langle g \rangle \times \langle g \rangle \to \langle g \rangle$$ $$\dfs$$ $$(g^i, g^j) \mapsto g^{i + j}$$ as group operation.

   $$\colortext{Well-definedness:}$$ Check `G1` to `G3` for $$\langle g \rangle$$.

### $$\colortext{Cyclic Group of Order n and Generator}$$

- $$n \in \N \cup \{\infty\}$$.

- $$G$$ is a group with $$\abs{G} = n$$.

   - $$\def$$ **a cyclic group of order $$n$$** $$\wrs$$ $$C_n$$ $$\typ$$ $$G$$ $$\diff$$ $$\exists g \in G$$ $$\st$$ $$G = \langle g \rangle$$ and $$\ord{g} = n$$.

   - $$\def$$ **a generator of $$C_n$$** $$\typ$$ $$g \in G$$ $$\diff$$ $$G = \langle g \rangle$$.


> - $$\the$$ $$\colortext{the generator of a cyclic group is not unique: } For example, $$1$$ and $$-1$$ are both generators of $$(\Z, +) = \langle 1 \rangle = \langle -1 \rangle$$.
> 
> ---
>
> - $$\the$$ $$\colortext{Cyclic group is abelian:}$$ $$C_n$$ is cyclic $$\imp$$ $$\forall g^i, g^j \in G, g^i g^j = g^j g^i$$ -- By the definition of cyclic group. But, the converse is not true. -- For example, $$(\Q, +)$$ is abelian but not cyclic.
>
> ---
>
> - $$\the$$ $$C_n$$ is cyclic $$\ifif$$ $$\exists g \in G, \forall a \in G, \exists ! n \in \{0, \dots, \ord{g} - 1\}, a = g^n$$. 
> 
>    -- $$\imp:$$ Let $$g$$ be a generator of $$G$$, then for any $$a \in G$$, 
>      
>    --- $$\colortext{Existence}$$ $$\exists m \in \Z$$, s.t. $$a = g^m$$. Let $$i := m \mod \ord{g}$$, then $$a = g^i$$.
>
>    --- $$\colortext{Uniqueness:}$$ $$\op{Contradiction:} If $$\exists i, j \in \{0, \dots, \ord{g} - 1\}$$, s.t. $$a = g^i = g^j$$, then $$g^{i - j} = e$$, hence $$\ord{g} \mid i - j$$, but $$i - j \in \{0, \dots, \ord{g} - 1\}$$, so $$i - j = 0$$, which is a contradiction. It follows that $$i = j$$.
>
>    -- $$\limp$$ By the definition of cyclic group.
> 
> ---
> 
> - $$\the$$ $$C_n$$ is cyclic $$\imp$$ There is at most one $$a \in G$$ s.t. $$\abs{a} = 2$$. -- By contradiction. If $$\exists a, b \in G, a \neq b$$ with $$\abs{a} = \abs{b} = 2$$, then $$a^2 = b^2 = e$$. By cyclicity, we write $$a = g^i, b = g^j$$, where $$g$$ is a generator of $$C_n$$ and $$i ,j \in \{0, \dots, n - 1\}, n =\ord{g}$$. Then $$g^i \neq e, g^j \neq e$$ and $$g^{2i} = g^{2j} = e$$. Hence, $$n \mid 2i, n \mid 2j$$, but $$2i, 2j \in \{0, 2, \dots, 2n - 2\}$$, so $$2i = 2j = 0$$ or $$2i = 2j = n$$. It follows that $$i = j = 0$$ or $$i = j = \frac{n}{2}$$ if $$n$$ is even, which is a contradiction.

### $$\colortext{1.3 Some Concrete Groups}$$

### $$\colortext{General Linear Group}$$

- $$\F$$ is a field.

- $$n \in \N^+$$.

- $$M_{n \times n}(\F)$$ is the set of all $$n \times n$$ matrices with entries in $$\F$$.

   $$\def$$ a **general linear group of rank $$n$$** $$\wrs$$ $$\mathrm{GL}(n, \F)$$ $$\dfs$$ $$\{A \in M_{n \times n}(\F) \mid A \textsf{ is invertible}\}$$ with matrix multiplication as group operation.

   $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `G1` to `G3` for $$\mathrm{GL}(n, \F)$$.

>  - $$the$$ $$\colortext{Symmetric group is a subgroup of general linear group:}$$ the symmetric group $$S(X)$$ could be seen as a subgroup of $$GL(n, \F)$$ by identifying the permutation $$f$$ with the matrix $$A$$ whose $$i$$-th column is the $$f(i)$$-th standard basis vector. -- For example, $$f = (1 2 3) \in S_3$$ could be identified with $$A = \begin{pmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix} \in GL(3, \F)$$.
>
> ---
>
> - $$\the$$ $$\colortext{Cyclic group is a Subgroup of General Linear Group:}$$ $$C_n$$ could be seen as a subgroup of $$GL(1, \F)$$ by using the rotational matrix $$A = \begin{pmatrix} \cos \frac{2 \pi}{n} & -\sin \frac{2 \pi}{n} \\ \sin \frac{2 \pi}{n} & \cos \frac{2 \pi}{n} \end{pmatrix} \in GL(2, \F)$$ as the generator.


### $$\colortext{Special Linear Group}$$

- $$\F$$ is a field.

- $$n \in \N^+$$.

- $$M_{n \times n}(\F)$$ is the set of all $$n \times n$$ matrices with entries in $$\F$$.

   $$\def$$ **a special linear group of rank $$n$$** $$\wrs$$ $$\mathrm{SL}(n, \F)$$ $$\dfs$$ $$\{A \in \mathrm{GL}_{n \times n}(\F) \mid \det(A) = 1\}$$ with matrix multiplication as group operation.

   $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `G1` to `G3` for $$\mathrm{SL}(n, \F)$$.

### $$\colortext{Orthogonal Group}$$

- $$\F$$ is a field.

- $$n \in \N^+$$.

   $$\def$$ **an orthogonal group of rank n** $$\wrs$$ $$\mathrm{O}(n, \F)$$ $$\dfs$$ $$\{A \in \mathrm{GL}_{n \times n}(\F) \mid A^\top A = A A^\top = I\}$$ with matrix multiplication as group operation.

   $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `G1` to `G3` for $$\mathrm{O}(n, \F)$$.

### $$\colortext{Special Orthogonal Group}$$

- $$\F$$ is a field.

- $$n \in \N^+$$.
  
  $$\def$$ **a special orthogonal group of rank n** $$\wrs$$ $$\mathrm{SO}(n, \F)$$ $$\dfs$$ $$\{A \in \mathrm{O}_{n \times n}(\F) \mid \det(A) = 1\}$$ with matrix multiplication as group operation.

### $$\colortext{Dihedral Group}$$

- $$n \in \N^+$$.

  - $$\def$$ **a rotation generator** $$\wrs$$ $$r$$ $$\typ$$ $$\mathrm{O}(2,\R)$$ $$\dfs$$ $$\left(\begin{array}{cc} \cos \frac{2 \pi}{n} & -\sin \frac{2 \pi}{n} \\ \sin \frac{2 \pi}{n} & \cos \frac{2 \pi}{n} \end{array}\right)$$. -- rotate the plane by the angle of $$\frac{2\pi}{n}$$.
 
  $$\def$$ **a reflection generator** $$\wrs$$ $$s$$ $$\typ$$ $$\mathrm{O}(2,\R)$$ $$\dfs$$ $$\left(\begin{array}{cc} 1 & 0 \\ 0 & -1 \end{array}\right)$$. -- reflect the plane about the $$x$$-axis.

  $$\def$$ **a dihedral group on a regular $$n$$-polygon** $$\wrs$$ $$D_{2n}$$ $$\typ$$ $$D_{2n} \leq \mathrm{O}(2, \R)$$ $$\dfs$$ $$\langle r, s \rangle = \set{r^i s^j \mid i \in \{0, \dots, n - 1\}, j \in \{0, 1\}}$$ with matrix multiplication as group operation.

   $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `G1` to `G3` for $$D_{2n}$$.

> - $$\the$$ $$\colortext{Dihedral Group is a Subgroup of Orthogonal Group:}$$
> 
>    $$D_{2n} \leq O(2, \R)$$. 
> 
>    -- by the definition of dihedral group. The dihedral is a subgroup that consists the Euclidean distance-preserving transformations of the plane, which includes rotations and reflections. 
>
>  ---
>
> - $$\the$$ $$\colortext{Dihedral Group is a Subgroup of Symmetric Group:}$$
>
>   $$D_{2n} \leq S(X)$$. 
> 
>    -- since rotation and reflection could be seen as a permutation of the vertices of a regular $$n$$-gon if we identify the vertices with the elements of $$X = \{1, \dots, n\}$$.
>
> ---
>
> - $$\the$$ $$\abs{D_{2n}} = 2n$$. 
> 
>    -- by the definition of dihedral group. 
>
> ---
>
> - $$\the$$ $$\colormath{Dihedral\;Group\;is\;Non-abelian\;if\;n \geq 3}$$.
>
>    $$\if$$ $$n \geq 3$$ $$\the$$ $$D_{2n}$$ is not abelian. 
> 
>    -- when $$n = 1$$, $$D_{2} = \set{e, (1, 2)} = C_2$$, which is abelian. When $$n = 2$$, $$D_{4} = \set{e, r, s, rs} = K_4$$, which is abelian (Introduced in the following.) When $$n \geq 3$$, $$D_{n}$$ is non-abelian. 
> 
>    -- · $$\colortext{A Conterexample:}$$ when $$n = 3$$, $$rs = (1 2)$$ and $$sr = (1 3)$$, so $$rs \neq sr$$. 

### $$\colortext{Klein Four-group}$$

- $$\{e, a, b,c\}$$ is a set with $$4$$ elements.

   $$\def$$ **the Klein four-group** $$\wrs$$ $$K_4$$ $$\dfs$$ $$\{e, a, b, c\}$$ with the group operation defined by the following table:

| $$\cdot$$ | $$e$$ | $$a$$ | $$b$$ | $$c$$ |
| --- | --- | --- | --- | --- |
| $$e$$ | $$e$$ | $$a$$ | $$b$$ | $$c$$ |
| $$a$$ | $$a$$ | $$e$$ | $$c$$ | $$b$$ |
| $$b$$ | $$b$$ | $$c$$ | $$e$$ | $$a$$ |
| $$c$$ | $$c$$ | $$b$$ | $$a$$ | $$e$$ |

   $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `G1` to `G3` for $$K_4$$.

> - $$\the$$ $$K_4$$ is abelian. 
>
>   -- $$\op{Check}$$ `AG4` for $$K_4$$.
>
> - $$\the$$ $$K_4$$ is the smallest non-cyclic group. 
>
>   -- by the definition of Klein four-group.
>
> - $$\the$$ $$K_4 = D_4 \leq S_4$$. 
> 
>   -- $$\op{Write}$$ $$K_4$$ in permutation form, i.e. $$K_4 = \set{e, (1 2)(3 4), (1 3)(2 4), (1 4)(2 3)}$$.


### $$\colortext{1.4 Groups Defined on Integers Mod n}$$

### $$\colortext{The Set of Equivalence Classes of Integers Mod n}$$

- $$n$$ $$\in$$ $$\N^+$$.

   $$\def$$ $$[a]_n := \set{a + kn \mid k \in \Z}$$ as the **equivalence class of $$a$$ modulo $$n$$**.

   $$\def$$ $$\Z_n = \{[0]_n, [1]_n, \dots, [n - 1]_n\}$$ as the **set of equivalence classes of integers modulo $$n$$**.

   $$\colortext{Well-definedness:}$$ $$\op{Check}$$ `Reflexivity`, `Symmetry` and `Transitivity` for $$[a]_n$$.

### $$\colortext{Additive Group of Integers Mod n}$$

- $$n$$ $$\in$$ $$\N^+$$.

   $$\def$$ $$\Z_n$$ with $$[a]_n + [b]_n = [a + b]_n$$ as group operation is the **additive group of integers modulo $$n$$**.

   $$\colortext{Well-definedness:} $$\op{Check} `G1` to `G3` for $$\Z_n$$.

> - $$\the$$ $$\Z_n$$ is a cyclic abelian group with $$[1]_n$$ as the generator. -- Check the abelian groups axioms `associativity`, `identity`, `inverse` and `commutivity`.

### $$\colortext{Multiplicative Group of Integers Mod n}$$

- $$n$$ $$\in$$ $$\N^+$$.

   $$\def$$ $$\Z_n^{\times} := \{[a]_n \in \Z_n \mid \gcd(a, n) = 1, a\in \{1, \dots, n - 1\}\}$$ with $$[a]_n \cdot [b]_n = [a \cdot b]_n$$ as group operation is the **multiplicative group of integers modulo $$n$$**.

   $$\colortext{Well-definedness:} $$\op{Check} `G1` to `G3` for $$\Z_n$$.

> - $$\Z_n^{\times}$$ is an abelian group. -- Check the abelian groups axioms `associativity`, `identity`, `inverse` and `commutivity`.

### $$\colortext{1.5 Applications of Groups}$$

### $$\colortext{Index of a Subgroup}$$

- $$G$$ is a finite group.

- $$H$$ $$\leq$$ $$G$$.

   $$\def$$ **the index of $$H$$ in $$G$$** $$\wrs$$ $$\abs{G : H} \dfs \frac{\abs{G}}{\abs{H}}$$.

### $$\colortext{Theorem 1.5.1. Lagrange's Theorem}$$

- $$G$$ is a finite group.

- $$H$$ $$\leq$$ $$G$$.

   - $$\the$$ $$\abs{H} \mid \abs{G}$$ and  $$\abs{G} = \abs{G : H} \cdot \abs{H}$$.

   - $$\the$$ $$\forall g \in G$$, $$\ord{g} \mid \abs{G}$$ and $$\ord{g} = \abs{G : \langle g \rangle} \cdot \abs{\langle g \rangle}$$.

   $$\colortext{Proof:}$$

   - Immediate from the definition of index.

   - Let $$H = \langle g \rangle$$, which is a cyclic subgroup of $$G$$ generated by $$g$$. Then apply the first part.

> - `A group with prime order is cyclic:` $$G$$ is a group with $$\abs{G} = p$$ for some prime number $$p$$ $$\imp$$ $$G$$ is cyclic and $$\if$$ $$g \neq e$$ $$\the$$ $$G = \langle g \rangle$$. -- By Lagrange's theorem. Since $$\abs{G} = p$$, $$\abs{G : \langle g \rangle} = 1$$ or $$p$$, so $$\abs{G : \langle g \rangle} = 1$$, which means $$G = \langle g \rangle$$.


### $$\colortext{Euler Totient Function}$$

- $$n$$ $$\in$$ $$\N^+$$.

    $$\def$$ $$\varphi(n) := \abs{\Z_n^{\times}} = \abs{\{[a]_n \in \Z_n \mid \gcd(a, n) = 1, a\in \{1, \dots, n - 1\}\}}$$ as the **Euler totient function**.

### $$\colortext{Theorem 1.5.3. Euler's Theorem}$$

- $$n$$ $$\in$$ $$\N^+$$.

- $$a \in \Z$$ with $$\gcd(a, n) = 1$$.

   $$\the$$ $$a^{\varphi(n)} \equiv 1 \mod n$$.

   $$\colortext{Proof:}$$ Let $$G = \Z_n^{\times}$$, which is a group with $$\abs{G} = \varphi(n)$$. Let $$H = \langle a \rangle$$, which is a cyclic subgroup of $$G$$ generated by $$a$$. Then apply Lagrange's theorem.

