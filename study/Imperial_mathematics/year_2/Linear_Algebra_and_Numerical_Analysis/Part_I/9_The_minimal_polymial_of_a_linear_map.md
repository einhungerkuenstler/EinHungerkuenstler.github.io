---
title: 9. The minimal polynomial of a linear map
layout: simple
---

$$\gdef\R{\mathbb{R}}$$
$$\gdef\C{\mathbb{C}}$$
$$\gdef\Z{\mathbb{Z}}$$ 
$$\gdef\N{\mathbb{N}}$$
$$\gdef\Q{\mathbb{Q}}$$
$$\gdef\F{\mathcal{F}}$$
$$\gdef\inner#1#2{\langle #1, #2 \rangle}$$
$$\gdef\norm#1{\left\| #1 \right\|}$$
$$\gdef\abs#1{\left| #1 \right|}$$
$$\gdef\set#1{\left\{ #1 \right\}}$$
$$\gdef\va{\mathbf{a}}$$
$$\gdef\vb{\mathbf{b}}$$
$$\gdef\vc{\mathbf{c}}$$
$$\gdef\deg{\operatorname{deg}}$$
$$\gdef\gcd{\operatorname{gcd}}$$
$$\gdef\di{\operatorname{dim}}$$
$$\newcommand{\imply}{\textcolor{gray}{\Rightarrow}}$$
$$\newcommand{\iimply}{\textcolor{gray}{\Leftarrow}}$$
$$\newcommand{\pro}{\textcolor{orange}{\mathcal{Proof:}}}$$


> For the following, we often use $$f, g$$ to denote $$f(x), g(x) \in \F[x]$$.


#### Definition $$\blue{\textsf{(Minimal polynomial)}}$$

- $$T: V \to V$$ is a linear map.
  
- $$m(x) \in \F[x]$$ is a polynomial.

    If the three following conditions holds:

    1. `T is a root of m(T)`: $$m(T) = 0$$.

    2. `Monic`: $$m(x)$$ is [monic](https://en.wikipedia.org/wiki/Monic_polynomial)

    3. `Minimal`: $$\deg(m(x))$$ is as small as possible when 1 and 2 holds.

    Then $$m(x)$$ is called the **minimal polynomial** of $$T$$.

> **Remark**:
>
> For matrix, the definition of the minimal polynomial is the same as the definition of the minimal polynomial of a linear map just by replacing $$T$$ with $$A$$.


#### Proposition 9.1 $$\blue{\textsf{(Uniqueness and divisibility of minimal polynomial)}}$$

- $$T: V \to V$$ is a linear map.

  Then,

  1. `Existence`: $$T$$ has a minimal polynomial.
   
  2. `Uniquness`: The minimal polynomial of $$T$$ is unique, denoted by $$m_T(x)$$. i.e. if $$p(x)$$ is another minimal polynomial of $$T$$, then $$p(x) = m_T(x)$$.
  
  3. `Divisibility`: For $$p(x) \in \F[x]$$, 
       
      $$
      p(T) = 0 \iif m_T(x) \mid p(x)
      $$

$$\pro$$

1. `Existence`: 

    By [the Cayley-Hamilton Theorem](https://en.wikipedia.org/wiki/Cayley%E2%80%93Hamilton_theorem), there exists a polynomial (the characteristic polynomial) $$c(x)$$ such that $$c(T) = 0$$. If we divide $$c(x)$$ by its leading coefficient, we get a monic polynomial $$m(x)$$ such that $$m(T) = 0$$. If we could not find another monic polynomial $$p(x)$$ such that $$p(T) = 0$$ and $$\deg(p(x)) < \deg(m(x))$$, then $$m(x)$$ is the minimal polynomial of $$T$$.

2. `Uniquness`: (Prove by **contradiction**).

    Assume there exists $$m{(x)}$$ and $$m_1(x)$$ satisfying the conditions of the minimal polynomial of $$T$$. Then, 

    - $$m(T) = 0$$ and $$m_1(T) = 0$$.

    - $$m(x)$$ and $$m_1(x)$$ are monic.

    - $$\deg(m(x)) = \deg(m_1(x))$$.
  
    Then, $$\deg(m(x) - m_1(x)) < \deg(m(x))$$ and $$(m(x) - m_1(x))(T) = 0$$. This contradicts the minimality of $$m(x)$$. Therefore, $$m(x) = m_1(x)$$.

3. `Divisibility`: 
     
    - $$\imply$$: Assume $$p(x) \in \F[x]$$ and $$p(T) = 0$$, by the [Eucilidean Algorithm](https://en.wikipedia.org/wiki/Euclidean_algorithm), there exists $$q(x), r(x) \in \F[x]$$ such that 

      $$
      p(x) = q(x) m_T(x) + r(x)
      $$

      and either $$r(x) = 0$$ or $$\deg(r(x)) < \deg(m_T(x))$$. Then, by the assumption that we have,

      $$
      p(T) = q(T)m_T(T) + r(T) = 0
      $$

      by the definition of the [minimal polynomial](#definition-the-minimal-polynomial). Since $$m_T(T) = 0$$, we have $$r(T) = 0$$. Then, we have

      $$
      r(x) = 0 \imply p(x) = q(x) m_T(x) \imply m_T(x) \mid p(x)
      $$

      - $$\iimply$$: Assume $$m_T(x) \mid p(x)$$, then for $$p(x) \in \F[x]$$, we have

      $$
      m_T(x) \mid p(x) \imply p(x) = m_T(x) q(x) \text{ for some } q(x) \in \F[x]
      $$
        
      Then, by the conditions of the [minimal polynomial](#definition-the-minimal-polynomial), we have

      $$
      p(T) = m_T(T) q(T) = 0  \quad \square
      $$


#### Proposition 9.2 $$\blue{\textsf{(The minimal polynomial divides the characteristic polynomial and share the same roots)}}$$

- $$T: V \to V$$ is a linear map.

- $$c_T(x)$$ is the characteristic polynomial of $$T$$.

- $$m_T(x)$$ is the minimal polynomial of $$T$$.

  Then,

  1. `Divides characteristic polynomial`: $$m_T(x) \mid c_T(x)$$.
  
  2. `Shares the same roots`: If $$\lambda \in \F$$ and $$c_T(\lambda) = 0$$, then $$m_T(\lambda) = 0$$.

$$\pro$$

1. `Divides characteristic polynomial`: 

    It is following from the [Proposition 9.1](#proposition-9.1-the-minimal-polynomial-divides-the-characteristic-polynomial) and [the Cayley-Hamilton Theorem](https://en.wikipedia.org/wiki/Cayley%E2%80%93Hamilton_theorem).

2. `Shares the same roots`: 

    Assume $$v$$ is an eigenvector of $$T$$ with respect to $$\lambda$$, i.e.

    $$
    T(v) = \lambda v
    $$

    Then, by the definition of the [minimal polynomial](#definition-the-minimal-polynomial), we have

    $$
    m_T(T)(v) = 0 \imply m_T(T)(v) = m_T(\lambda)(v) = 0
    $$

    Hence, $$m_T(\lambda) = 0$$. $$\square$$

#### Theorem 9.3 $$\blue{\textsf{(The minimal polynomial divides the characteristic polynomial)}}$$

- $$T: V \to V$$ is a linear map.

- $$p(x) \in \F[x]$$ is an irreducible factor of $$\chi_T(x)$$.

  Then, $$p(x) \mid m_T(x)$$.

$$\pro$$


#### Proposition 9.4 $$\blue{\textsf{(The relations of polynomials of linear maps with its corresponding invariant map and quotient map)}}$$

- $$T: V \to V$$ is a linear map.

- $$T_w: V \to V$$ is the invariant map of $$T$$ with respect to $$w \in V$$.

- $$\overline{T}: V / \F[w] \to V / \F[w]$$ is the quotient map of $$T$$ with respect to $$w \in V$$.


  Then,

  1. `Product`: $$c_T(x) = c_{T_w}(x) c_{\overline{T}}(x)$$.

  2. `Common divisior`: $$m_{T_w}(x) \mid m_T(x)$$ and $$m_{\overline{T}}(x) \mid m_T(x)$$.


$$\pro$$



