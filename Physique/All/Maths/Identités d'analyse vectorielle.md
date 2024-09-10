---
tags:
  - Maths/Analyse/Vectorielle
---

$$\nabla \times \nabla \psi = \mathbf{0}$$
$$\nabla \cdot (\nabla \times \mathbf{A}) = 0$$
$$\nabla \cdot (\mathbf{A} \times \mathbf{B}) = \mathbf{B} \cdot (\nabla \times \mathbf{A}) - \mathbf{A} \cdot (\nabla \times \mathbf{B})$$
$$\nabla \times (\mathbf{A} \times \mathbf{B}) = \mathbf{A}(\nabla \cdot \mathbf{B}) - \mathbf{B} (\nabla \cdot \mathbf{A}) + (\mathbf{B} \cdot \nabla )\mathbf{A} - (\mathbf{A} \cdot \nabla )\mathbf{B}$$
$$\mathbf{A} \times (\nabla \times \mathbf{B}) = (\nabla \mathbf{B}) \cdot \mathbf{A} - \mathbf{A} \cdot (\nabla \mathbf{B})$$


$$\begin{align}
\nabla \times (\nabla \times \mathbf{A}) &= \nabla(\nabla \cdot \mathbf{A}) - \nabla^2 \mathbf{A}
\end{align}$$



> [!théorème] Théorème de Stokes
> Soit $S$ une surface orientée lisse dans $\mathbb{R}^3$ avec comme bord $C \equiv \partial S$. Si un champ vectoriel $\vec{F}(x,y,z)$ est défini et a toutes ses dérivées partielles d'ordre 1 continues dans une région contenant $S$, alors $$\iint_S (\nabla \times \mathbf{F})\cdot \mathrm{d}\mathbf{S} = \oint_{\partial S} \mathbf{F} \cdot \mathrm{d} \mathbf{C}$$

^f6bf6f

> [!théorème] Théorème de la divergence
> Soit $V$ un sous ensemble de $\mathbb{R}^n$ (donc quand $n=3$, $V$ représente un volume) compact ayant un bord lisse par morceaux $\partial V \equiv S$. Si le champ vectoriel $\mathbf{F}$ est continu dérivable dans au moins $V$, alors $$\iiint_V (\nabla \cdot \mathbf{F})\ \mathrm{d}V = \oint_{\partial V} \mathbf{F} \cdot \ \mathrm{d} \mathbf{S}$$

^8b3e75

