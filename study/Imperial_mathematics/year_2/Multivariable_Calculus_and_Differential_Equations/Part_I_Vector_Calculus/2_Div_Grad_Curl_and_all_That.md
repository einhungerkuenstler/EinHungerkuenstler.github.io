---
title: 2. Grad, Div, Curl and all That
layout: simple
---

$$\gdef\R{\mathbb{R}}$$
$$\gdef\C{\mathbb{C}}$$
$$\gdef\Z{\mathbb{Z}}$$ 
$$\gdef\N{\mathbb{N}}$$
$$\gdef\Q{\mathbb{Q}}$$
$$\gdef\F{\mathcal{F}}$$
$$\gdef\abs#1{\left| #1 \right|}$$
$$\gdef\pap#1{\frac{\partial \phi }{\partial #1}}$$
$$\gdef\va{\mathbf{a}}$$
$$\gdef\vb{\mathbf{b}}$$
$$\gdef\vc{\mathbf{c}}$$
$$\gdef\ve{\varepsilon}$$
$$\gdef\nvi{\widehat{\mathbf{i}}}$$
$$\gdef\nvj{\widehat{\mathbf{j}}}$$
$$\gdef\nvk{\widehat{\mathbf{k}}}$$
$$\gdef\nve{\widehat{\mathbf{e}}}$$
$$\gdef\ns{\widehat{\mathbf{s}}}$$
$$\gdef\nn{\widehat{\mathbf{n}}}$$
$$\gdef\d{\operatorname{div}}$$
$$\gdef\cu{\operatorname{curl}}$$
$$\gdef\g{\nabla}$$
$$\gdef\vf{\mathbf{A}}$$

#### *For the following, we assume $$\phi$$ is a scalar function and $$\vf$$ is a vector field.*

## 2.1 Gradient

### Definition (Level surfaces set)

- $$\phi = c$$ defines a **level surface** of $$\phi$$, where $$c$$ is a constant.

- If we vary $$c$$, we get a collection of level surfaces.

The collection of level surfaces of $$\phi$$ is called the **level surfaces set** of $$\phi$$ or the **equipotential surfaces** of $$\phi$$.

### Definition (Directional derivative)

- A specific point $$P$$ such that $$\phi = \phi(P)$$/

- $$Q$$ is a neighbouring point of $$P$$.

- The equation of the level surface through $$Q$$ is $$\phi = \phi(Q)$$.

- The normal line to $$\phi = \phi(P)$$ at $$P$$ and the normal line intersects the level surface $$\phi = \phi(Q)$$ at $$N$$

- Since $$N$$ is on the surface level, $$\phi(N) = \phi(P)$$.

- $$s$$ is the length along the normal line along $$PQ$$

- $$n$$ is the length along the normal line from $$PN$$.

- The unit vector $$\ns$$ and $$\nn$$ are the unit vectors along the normal line from $$PQ$$ and $$PN$$ respectively.

Define $$\partial \phi / \partial s$$ to be the **directional derivative** of $$\phi$$ in the direction $$\widehat{\mathbf{s}}$$ at $$P$$ as:

$$
\begin{aligned}
\frac{\partial \phi}{\partial s} & = \lim_{PQ \to 0} \frac{\phi(Q) - \phi(P)}{|PQ|}\\
& = \lim_{Q \to P} \frac{\phi(N) - \phi(P)}{|PN|}\cdot \frac{|PN|}{|PQ|}\\
& = \lim_{N \to P} \frac{\phi(N) - \phi(P)}{|PN|}\cdot \lim_{Q \to P}\frac{|PN|}{|PQ|}\\
& = \frac{\partial \phi}{\partial n} \cdot \lim_{Q \to P}\frac{|PN|}{|PQ|}\\
& = \frac{\partial \phi}{\partial n} \cdot \cos \theta \quad \text{where } \theta \text{ is the angle between } PN \text{ and } PQ\\
& = \frac{\partial \phi}{\partial n} \cdot (\widehat{\mathbf{n}} \cdot \widehat{\mathbf{s}}) \\
\end{aligned}
$$

That is,

$$
\tag{2.1.1}
\frac{\partial \phi}{\partial s} = \frac{\partial \phi}{\partial n} \cdot (\widehat{\mathbf{n}} \cdot \widehat{\mathbf{s}}) = \left(\frac{\partial \phi}{\partial n}\widehat{\mathbf{n}} \right)\cdot \widehat{\mathbf{s}}
$$

> **Remark**:
>
> Since $$\cos \theta \leq 1$$, the maximum direction derivative is at $$P$$ occurs when $$\theta = 0$$, i.e. $$\widehat{\mathbf{n}} = \widehat{\mathbf{s}}$$, meaning that the maximum directional derivative is in the direction of the normal line.

### Definition (Gradient)

The **gradient** is the direction that $$\phi$$ changes most rapidly, which is the direction of the normal line and It is a **vector field**. which maps a point $$P$$ to a vector $$\nabla \phi(P)$$. The gradient is defined as:

$$
\nabla \phi = \frac{\partial \phi}{\partial n}\widehat{\mathbf{n}}
$$

> **Remark**:
>
> - The operator $$\nabla$$ is called the **gradient operator** and it is a vector operator, it is defined as:
>  $$
\nabla = \pap{x}\widehat{\mathbf{i}} + \pap{y}\widehat{\mathbf{j}} + \pap{z}\widehat{\mathbf{k}}
    $$
>
> - The definition of gradient is only adapted to a scalar function $$\phi$$.
> 
> - The gradient is perpendicular to the level surface of $$\phi$$.
>
> - The physical meaning of the gradient at $$P$$ is the direction of the maximum directional derivative of $$\phi$$ at $$P$$.
>
> - Use gradient to find the direction derivative of $$\phi$$ in the direction $$\widehat{\mathbf{s}}$$:
>
>   $$
\frac{\partial \phi}{\partial s} = \nabla \phi \cdot \widehat{\mathbf{s}}
 $$

### Theorem (Gradient in Cartesian coordinates)

- $$\phi = \phi(x, y, z)$$

- $$\nvi, \nvj, \nvk$$ are the unit vectors in the $$x, y, z$$ directions respectively.

$$
\nabla \phi =  \pap{x}\widehat{\mathbf{i}} + \pap{y}\widehat{\mathbf{j}} + \pap{z}\widehat{\mathbf{k}}
$$

**Proof**:

If $$\g \phi = A_1 \nvi + A_2 \nvj + A_3 \nvk$$, then

$$
\begin{aligned}
\nvi \cdot \g \phi & = A_1 \\
\nvj \cdot \g \phi & = A_2 \\
\nvk \cdot \g \phi & = A_3 \\
\end{aligned}
$$

By definition,

$$
\begin{aligned}
\nvi \cdot \g \phi & = \frac{\partial \phi}{\partial x} \\
\nvj \cdot \g \phi & = \frac{\partial \phi}{\partial y} \\
\nvk \cdot \g \phi & = \frac{\partial \phi}{\partial z} \\
\end{aligned}
$$

Hence,

$$
\g \phi = \pap{x}\widehat{\mathbf{i}} + \pap{y}\widehat{\mathbf{j}} + \pap{z}\widehat{\mathbf{k}}
$$ 

<p align="right">$$\square$$</p>

### Theorem (Gradient in cylindrical coordinates)

- $$\phi = \phi(r, \theta, z)$$

- $$\widehat{\mathbf{r}}, \widehat{\boldsymbol{\theta}}, \widehat{\mathbf{z}}$$ are the unit vectors in the $$r, \theta, z$$ directions respectively.

$$
\nabla \phi =  \pap{r}\widehat{\mathbf{r}} + \frac{\widehad{\boldsymnbol{\theta}}}{r}\pap{\theta} + \pap{z}\widehat{\mathbf{z}}
$$

**Proof**:

Before we prove this, we need to know the following:

$$
\begin{aligned}
\widehat{\mathbf{r}} & = \cos \theta \widehat{\mathbf{i}} + \sin \theta \widehat{\mathbf{j}} \\
\widehat{\boldsymbol{\theta}} & = -\sin \theta \widehat{\mathbf{i}} + \cos \theta \widehat{\mathbf{j}} \\
\widehat{\mathbf{k}} & = \widehat{\mathbf{k}} \\
\end{aligned}
$$

We write $$\g \phi = A_1 \widehat{\mathbf{r}} + A_2 \widehat{\boldsymbol{\theta}} + A_3 \widehat{\mathbf{z}}$$, then

$$
\begin{aligned}
A_{1} & =\widehat{\mathbf{r}} \cdot \nabla \phi \\
& = \widehat{\mathbf{r}} \left(\pap{x} \widehat{\mathbf{i}} + \pap{y} \widehat{\mathbf{j}} + \pap{z} \widehat{\mathbf{k}}\right) \\
& = \cos \theta \pap{x} + \sin \theta \pap{y}\quad(\widehat{r} \cdot \widehat{k} = 0) \\
& = \frac{\partial x}{\partial r} \frac{\partial \phi}{\partial x}+\frac{\partial y}{\partial r} \frac{\partial \phi}{\partial y} \\
& = \frac{\partial \phi}{\partial r} \\
\end{aligned}
$$

**Notice that it is not twice, since it is distributed to the two components.**

$$
\begin{aligned}
A_{2} & =\widehat{\theta} \cdot \nabla \phi \\
& = \widehat{\theta} \left(\pap{x} \widehat{\mathbf{i}} + \pap{y} \widehat{\mathbf{j}} + \pap{z} \widehat{\mathbf{k}}\right) \\
& = -\sin \theta \pap{x} + \cos \theta \pap{y}\quad(\widehat{\theta} \cdot \widehat{k} = 0) \\
& = \frac{1}{r}\frac{\partial x}{\partial \theta} \frac{\partial \phi}{\partial x}+\frac{1}{r}\frac{\partial y}{\partial \theta} \frac{\partial \phi}{\partial y} \\
& = \frac{1}{r}\frac{\partial \phi}{\partial \theta} \\
\end{aligned}
$$

$$
A_3 = \widehat{\mathbf{k}} \cdot \nabla \phi = \pap{z}
$$

Hence,

$$
\nabla \phi=\widehat{\mathbf{r}} \frac{\partial \phi}{\partial r}+\frac{\widehat{\theta}}{r} \frac{\partial \phi}{\partial \theta}+\widehat{\mathbf{k}} \frac{\partial \phi}{\partial z} .
$$ 

<p align="right">$$\square$$</p>

### Theorem (Gradient in spherical coordinates)

- $$\phi = \phi(r, \theta, \alpha)$$

- $$\widehat{\mathbf{r}}, \widehat{\boldsymbol{\theta}}, \widehat{\boldsymbol{\alpha}}$$ are the unit vectors in the $$r, \theta, \alpha$$ directions respectively.

$$
\nabla \phi =  \pap{r}\widehat{\mathbf{r}} + \frac{1}{r}\pap{\theta} + \frac{1}{r \sin \theta}\pap{\alpha}
$$

**Proof**:

Before we prove this, we need to know the following:

$$
\begin{aligned}
\widehat{\mathbf{r}} & = \sin \theta \cos \alpha \widehat{\mathbf{i}} + \sin \theta \sin \alpha \widehat{\mathbf{j}} + \cos \theta \widehat{\mathbf{k}} \\
\widehat{\boldsymbol{\theta}} & = \cos \theta \cos \alpha \widehat{\mathbf{i}} + \cos \theta \sin \alpha \widehat{\mathbf{j}} - \sin \theta \widehat{\mathbf{k}} \\
\widehat{\boldsymbol{\alpha}} & = -\sin \alpha \widehat{\mathbf{i}} + \cos \alpha \widehat{\mathbf{j}} 
\end{aligned}
$$

We write $$\g \phi = A_1 \widehat{\mathbf{r}} + A_2 \widehat{\boldsymbol{\theta}} + A_3 \widehat{\boldsymbol{\alpha}}$$, then

$$
\begin{aligned}
A_{1} & =\widehat{\mathbf{r}} \cdot \nabla \phi \\
& = \widehat{\mathbf{r}} \left(\pap{x} \widehat{\mathbf{i}} + \pap{y} \widehat{\mathbf{j}} + \pap{z} \widehat{\mathbf{k}}\right) \\
& = \sin \theta \cos \alpha \pap{x} + \sin \theta \sin \alpha \pap{y} + \cos \theta \pap{z} \\
& = \frac{\partial x}{\partial r} \frac{\partial \phi}{\partial x}+\frac{\partial y}{\partial r} \frac{\partial \phi}{\partial y} + \frac{\partial z}{\partial r} \frac{\partial \phi}{\partial z} \\
& = \frac{\partial \phi}{\partial r} \\
\end{aligned}
$$

**Notice that it is not triple, since it is distributed to the three components.**

$$
\begin{aligned}
A_{2} & =\widehat{\theta} \cdot \nabla \phi \\
& = \widehat{\theta} \left(\pap{x} \widehat{\mathbf{i}} + \pap{y} \widehat{\mathbf{j}} + \pap{z} \widehat{\mathbf{k}}\right) \\
& = \cos \theta \cos \alpha \pap{x} + \cos \theta \sin \alpha \pap{y} \quad (\widehat{\theta} \cdot \widehat{k} = 0) \\
& = \frac{1}{r}\frac{\partial x}{\partial \theta} \frac{\partial \phi}{\partial x}+\frac{1}{r}\frac{\partial y}{\partial \theta} \frac{\partial \phi}{\partial y} \\
& = \frac{1}{r}\frac{\partial \phi}{\partial \theta} \\
\end{aligned}
$$

$$
\begin{aligned}
A_{3} & =\widehat{\alpha} \cdot \nabla \phi \\
& = \widehat{\alpha} \left(\pap{x} \widehat{\mathbf{i}} + \pap{y} \widehat{\mathbf{j}} + \pap{z} \widehat{\mathbf{k}}\right) \\
& = -\sin \alpha \pap{x} + \cos \alpha \pap{y} \quad (\widehat{\alpha} \cdot \widehat{k} = 0) \\
& = \frac{1}{r \sin \theta}\frac{\partial x}{\partial \alpha} \frac{\partial \phi}{\partial x}+\frac{1}{r \sin \theta}\frac{\partial y}{\partial \alpha} \frac{\partial \phi}{\partial y} \\
& = \frac{1}{r \sin \theta}\frac{\partial \phi}{\partial \alpha} \\
\end{aligned}
$$

Hence,

$$
\nabla \phi=\widehat{\mathbf{r}} \frac{\partial \phi}{\partial r}+\frac{\widehat{\theta}}{r} \frac{\partial \phi}{\partial \theta}+\frac{\widehat{\alpha}}{r \sin \theta} \frac{\partial \phi}{\partial \alpha}
$$

<p align="right">$$\square$$</p>

### Equation of a tangent plane to $$\phi = \phi(P)$$

- $$(\g \phi)_P$$ is the gradient at $$P$$.

- $$\mathbf{r}$$ is the position vector.

- $$\mathbf{r}_P$$ is the position vector at $$P$$.

Since $$\g \phi$$ is normal to the level surface $$\phi = \phi(P)$$, the equation of the tangent plane to $$\phi = \phi(P)$$ at $$P$$ is:

$$
(\mathbf{r} - \mathbf{r}_P) \cdot (\g \phi)_P = 0
$$

In component form, it is:

$$
\left(\frac{\partial \phi}{\partial x}\right)_{P}\left(x-x_{P}\right)+\left(\frac{\partial \phi}{\partial y}\right)_{P}\left(y-y_{P}\right)+\left(\frac{\partial \phi}{\partial z}\right)_{P}\left(z-z_{P}\right)=0 
$$

where $$\left(\pap{x}\right)_P$$, $$\left(\pap{y}\right)_P$$ and $$\left(\pap{z}\right)_P$$ are the partial derivatives of $$\phi$$ at $$P$$ and are constants.


## 2.2 Divergence and Curl

### Definition (Divergence)

The **divergence** of a vector field $$\vf$$ is a **scalar function** that maps a point $$P$$ to a scalar $$\d \vf(P)$$. The divergence is defined as:

$$
\d \vf = \nabla \cdot \vf
$$

### Theorem (Divergence in Cartesian coordinates)

- $$\vf = A_1 \nvi + A_2 \nvj + A_3 \nvk$$

- $$\nvi, \nvj, \nvk$$ are the unit vectors in the $$x, y, z$$ directions respectively.

$$
\d \vf = \pap{x}A_1 + \pap{y}A_2 + \pap{z}A_3
$$

**Proof**:

$$
\begin{aligned}
\operatorname{div} \mathbf{A} & = \left(\frac{\partial}{\partial x}\widehat{\mathbf{i}} + \frac{\partial}{\partial y}\widehat{\mathbf{j}} + \frac{\partial}{\partial z}\widehat{\mathbf{k}}\right) \cdot (A_1\widehat{\mathbf{i}} + A_2\widehat{\mathbf{j}} + A_3\widehat{\mathbf{k}}) \\
& = \frac{\partial A_1}{\partial x} + \frac{\partial A_2}{\partial y} + \frac{\partial A_3}{\partial z} \\
& = \sum_{i=1}^{3} \frac{ \partial A_i}{\partial x_i}
\end{aligned}
$$

<p align="right">$$\square$$</p>

> **Remark**:
>
>> - The definition of divergence is only adapted to a vector field $$\vf$$.
>
>> - The physical meaning of the divergence at $$P$$ is the net flow of $$\vf$$ out of a small closed surface around $$P$$ per unit volume as the volume shrinks to zero.
> 
>> - The dot product in the definition of divergence $$\g \cdot \vf$$ is not commutative, i.e. $$\g \cdot \vf \neq \vf \cdot \g$$. Since the left hand side is a **scalar operator** and the right hand side is divergence of a vector field, which is a **scalar**.

### Definition (Curl)

The **curl** of a vector field $$\vf$$ is a **vector field** that maps a point $$P$$ to a vector $$\cu \vf(P)$$. The curl is defined as:

$$
\cu \vf = \nabla \times \vf
$$

### Theorem (Curl in Cartesian coordinates)

- $$\vf = A_1 \nvi + A_2 \nvj + A_3 \nvk$$

- $$\nvi, \nvj, \nvk$$ are the unit vectors in the $$x, y, z$$ directions respectively.

$$
\cu \vf = \left(\pap{y}A_3 - \pap{z}A_2\right)\nvi + \left(\pap{z}A_1 - \pap{x}A_3\right)\nvj + \left(\pap{x}A_2 - \pap{y}A_1\right)\nvk
$$

**Proof**:
$$
\begin{aligned}
\operatorname{curl} \mathbf{A} & = \left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
A_{1} & A_{2} & A_{3}
\end{array}\right|\\
& = \left(\frac{\partial A_3}{\partial y} - \frac{\partial A_2}{\partial z}\right)\widehat{\mathbf{i}} + \left(\frac{\partial A_1}{\partial z} - \frac{\partial A_3}{\partial x}\right)\widehat{\mathbf{j}} + \left(\frac{\partial A_2}{\partial x} - \frac{\partial A_1}{\partial y}\right)\widehat{\mathbf{k}} \\
& = \sum_{i=1}^{3} \ve_{ijk} \frac{\partial A_k}{\partial x_j} \\
\end{aligned}
$$

<p align="right">$$\square$$</p>

> **Remark**:
>
>> - The definition of curl is only adapted to a vector field $$\vf$$.
>
>> - The physical meaning of the curl at $$P$$ is the net rotation of $$\vf$$ around $$P$$ per unit volume as the volume shrinks to zero.
>
>> - The cross product in the definition of curl $$\g \times \vf$$ is not commutative, i.e. $$\g \times \vf \neq \vf \times \g$$. Since the left hand side is a **vector operator** and the right hand side is curl of a vector field, which is a **vector**. 

> **Remark**:
>
> These simple form for $$\d$$ and $$\cu$$ are only adapted to Cartesian coordinates since $$\mathbf{i}, \mathbf{j}, \mathbf{k}$$ are constant vectors. For other coordinates, we need to use the chain rule to derive the formula.


## 2.3 Operations with the gradient operator

### Some important sum and product formulas

$$\g, \d, \cu$$ are all **linear operators**, i.e. for any scalar $$\alpha$$ and vector fields $$\vf, \vg$$:

$$
\begin{aligned}
& \text { (i) } \nabla\left(\phi_{1}+\phi_{2}\right) =\nabla \phi_{1}+\nabla \phi_{2}, \\
& \text { (ii) } \operatorname{div}(\mathbf{A}+\mathbf{B}) =\operatorname{div} \mathbf{A}+\operatorname{div} \mathbf{B}, \\
&\text { (iii) } \operatorname{curl}(\mathbf{A}+\mathbf{B}) =\operatorname{curl} \mathbf{A}+\operatorname{curl} \mathbf{B} .
\end{aligned}
$$

The proof is trivial by the definition of the $$\nabla$$ operator.

$$\g, \d, \cu$$ satisfy the **product rule**, i.e. for any scalar $$\phi, \psi$$ and vector fields $$\vf$$:

$$
\begin{aligned}
& \mathrm{ (iv) } \nabla(\phi \psi) =\phi \nabla \psi+\psi \nabla \phi \\
& \mathrm{ (v) } \operatorname{div}(\phi \mathbf{A}) =\phi \operatorname{div} \mathbf{A}+\nabla \phi \cdot \mathbf{A} .
\end{aligned}
$$

**Proof of (v)**:

$$
    \begin{aligned}
    \d(\phi \vf) & = \left(\nvi \frac{\partial}{\partial x} + \nvj \frac{\partial}{\partial y} + \nvk \frac{}{z}\right) \cdot \left(\phi A_1 \nvi +\phi A_2 \nvj + \phi A_3 \nvk\right) \\
    & = \frac{\partial \phi A_1}{\partial x} + \frac{\partial \phi A_2}{\partial y} + \frac{\partial \phi A_3}{\partial z} \\
    & = \phi \left(\frac{\partial A_1}{\partial x} + \frac{\partial A_2}{\partial y} + \frac{\partial A_3}{\partial z}\right) + A_1 \frac{\partial \phi}{\partial x} + A_2 \frac{\partial \phi}{\partial y} + A_3 \frac{\partial \phi}{\partial z} \\
    & = \phi \d \vf + \g \phi \cdot \vf \\
    \end{aligned}
$$

If we use the Einstein summation convention, the form and the proof will be much simpler:

$$
\begin{aligned}

\g \phi & = \nve_i \frac{\partial \phi}{\partial x_i}\\
  
\d \vf & = \frac{\partial A_i}{\partial x_i}\\
  
[\g \phi]_i & = \frac{\partial \phi}{\partial x_i}\\
  
[\cu \vf]_i & = \ve_{ijk} \frac{\partial A_k}{\partial x_j}

\end{aligned}
$$

where $$[\:\;]_i$$ denotes the $$i$$ th component of the vector.

Therefore, 

$$
    \begin{aligned}
    \d (\phi \vf) & = \frac{\partial \phi A_i}{\partial x_i} \\
    & = \phi \frac{\partial A_i}{\partial x_i} + A_i \frac{\partial \phi}{\partial x_i} \\
    & = \phi \d \vf + (\vf \cdot \g) \phi \\
    \end{aligned}
$$

### Other important formulas

$$
\begin{aligned}
& \text { (vi) } \operatorname{curl}(\phi \mathbf{A})  =\phi \operatorname{curl} \mathbf{A}+\nabla \phi \times \mathbf{A}, \\
& \text { (vii) } \operatorname{div}(\mathbf{A} \times \mathbf{B}) =\mathbf{B} \cdot \operatorname{curl} \mathbf{A}-\mathbf{A} \cdot \operatorname{curl} \mathbf{B}, \\
& \text { (viii) } \operatorname{curl}(\mathbf{A} \times \mathbf{B})  =(\mathbf{B} \cdot \nabla) \mathbf{A}-\mathbf{B} \operatorname{div} \mathbf{A}-(\mathbf{A} \cdot \nabla) \mathbf{B}+\mathbf{A} \operatorname{div} \mathbf{B}, \\
& \text { (ix) } \nabla(\mathbf{A} \cdot \mathbf{B})  =(\mathbf{B} \cdot \nabla) \mathbf{A}+(\mathbf{A} \cdot \nabla) \mathbf{B}+\mathbf{B} \times \operatorname{curl} \mathbf{A}+\mathbf{A} \times \operatorname{curl} \mathbf{B} .
\end{aligned}
$$

#### *For the following, we assume that our vector and scalar fields are sufficiently smooth that we can interchange the order of differentiation.*

### Definition (The divergence of a gradient: the Laplacian)

- $$\phi = \phi(x, y, z)$$

- $$\nvi, \nvj, \nvk$$ are the unit vectors in the $$x, y, z$$ directions respectively.

- 














