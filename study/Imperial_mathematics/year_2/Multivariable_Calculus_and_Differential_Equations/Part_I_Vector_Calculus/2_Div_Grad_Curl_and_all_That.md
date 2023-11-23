---
title: 2. Div, Grad, Curl and all That
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

#### *For the following, we assume $$\phi$$ is a scalar function and $$\vf$$ is a vector field and $$\nvi, \nvj, \nvk$$ are the unit vectors in the $$x, y, z$$ directions respectively.*

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






