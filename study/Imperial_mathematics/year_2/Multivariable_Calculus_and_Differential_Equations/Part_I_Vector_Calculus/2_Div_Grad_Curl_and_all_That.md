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

> *Remark*:
>
> Since $$\cos \theta \leq 1$$, the maximum direction derivative is at $$P$$ occurs when $$\theta = 0$$, i.e. $$\widehat{\mathbf{n}} = \widehat{\mathbf{s}}$$, meaning that the maximum directional derivative is in the direction of the normal line.

### Definition (Gradient)

The **gradient** is the direction that $$\phi$$ changes most rapidly, which is the direction of the normal line. We denote it as $$\g \phi$$ or $$\operatorname{grad} \phi$$:

$$
\nabla \phi = \frac{\partial \phi}{\partial n}\widehat{\mathbf{n}}
$$

> *Remark*:
>
>> - The operator $$\nabla$$ is called the **gradient operator** and it is a vector operator.
>
>> - The gradient is a **vector field**. It is a vector at each point in space.
>
>> - The gradient is perpendicular to the level surface of $$\phi$$.
>
>> - The physical meaning of the gradient at $$P$$ is the direction of the maximum directional derivative of $$\phi$$ at $$P$$.
>
>> - Use gradient to find the direction derivative of $$\phi$$ in the direction $$\widehat{\mathbf{s}}$$:
>>
>>   $$
>>   \frac{\partial \phi}{\partial s} = \nabla \phi \cdot \widehat{\mathbf{s}}
>>   $$

### Theorem (Gradient in Cartesian coordinates)

- $$\phi = \phi(x, y, z)$$

- $$\nvi, \nvj, \nvk$$ are the unit vectors in the $$x, y, z$$ directions respectively.

$$
\nabla \phi =  \pap{x}\widehat{\mathbf{i}} + \pap{y}\widehat{\mathbf{j}} + \pap{z}\widehat{\mathbf{k}}
$$

*Proof*:

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
$$ $$\square$$

### Theorem (Gradient in cylindrical coordinates)

- $$\phi = \phi(r, \theta, z)$$

- $$\widehat{\mathbf{r}}, \widehat{\boldsymbol{\theta}}, \widehat{\mathbf{z}}$$ are the unit vectors in the $$r, \theta, z$$ directions respectively.

$$
\nabla \phi =  \pap{r}\widehat{\mathbf{r}} + \frac{\widehad{\boldsymnbol{\theta}}}{r}\pap{\theta} + \pap{z}\widehat{\mathbf{z}}
$$

*Proof*:

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
$$ $$\square$$

### Theorem (Gradient in spherical coordinates)

- $$\phi = \phi(r, \theta, \alpha)$$

- $$\widehat{\mathbf{r}}, \widehat{\boldsymbol{\theta}}, \widehat{\boldsymbol{\alpha}}$$ are the unit vectors in the $$r, \theta, \alpha$$ directions respectively.

$$
\nabla \phi =  \pap{r}\widehat{\mathbf{r}} + \frac{1}{r}\pap{\theta} + \frac{1}{r \sin \theta}\pap{\alpha}
$$

*Proof*:

Before we prove this, we need to know the following:

$$
\begin{aligned}
\widehat{\mathbf{r}} & = \sin \theta \cos \alpha \widehat{\mathbf{i}} + \sin \theta \sin \alpha \widehat{\mathbf{j}} + \cos \theta \widehat{\mathbf{k}} \\
\widehat{\boldsymbol{\theta}} & = \cos \theta \cos \alpha \widehat{\mathbf{i}} + \cos \theta \sin \alpha \widehat{\mathbf{j}} - \sin \theta \widehat{\mathbf{k}} \\
\widehat{\boldsymbol{\alpha}} & = -\sin \alpha \widehat{\mathbf{i}} + \cos \alpha \widehat{\mathbf{j}} \\
\end{aligned}
$$

We write $$\g \phi = A_1 \widehat{\mathbf{r}} + A_2 \widehat{\boldsymbol{\theta}} + A_3 \widehat{\boldsymbol{\alpha}}$$, then

$$
\begin{aligned}
A_{1} & =\widehat{\mathbf{r}} \cdot \nabla \phi \\






