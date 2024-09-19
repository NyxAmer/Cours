---
tags:
  - Thermodynamique/TransfertsThermique
---
L'équation de la chaleur est dérivable de manière analogue à l'[[Equation de la diffusion]] mais avec des grandeurs physiques différentes.

> [!théorème] Grandeurs physiques 
>- le **champ de température** $T(\vec{r}, t)$ en $\mathrm{K}$
>	représente la température à chaque point de l'espace à chaque instant
>- le **gradient de température** $\nabla T$ en $\mathrm{K} \cdot \mathrm{m}^{-1}$
>	représente la direction dans laquelle la température change le plus dans l'espace
>- le **Flux de chaleur** $\Phi$ en $\mathrm{W}$
>	l'énergie transférée par unité de temps à travers une surface
>- la **densité de flux de chaleur** $\vec{j}_q$ en $\mathrm{W} \cdot \mathrm{m}^{-2}$
>	représente la direction et la magnitude de l'énergie transférée à travers une surface par unité de surface
>- la **conductivité thermique** $\lambda$ en $\mathrm{W} \cdot \mathrm{m}^{-1} \cdot \mathrm{K}^{-1}$
>	représente la capacité d'un matériaux à transférer la chaleur par unité de longueur
>- la **diffusivité thermique** $\displaystyle \alpha = \frac{\lambda}{\rho c_p}$ en $\mathrm{m}^2 \cdot \mathrm{s}^{-1}$
>	représente la vitesse à laquelle la chaleur se propage dans un milieu
>- le **coefficient de transfert de chaleur** $h$ en $\mathrm{W} \cdot \mathrm{m}^{-2} \cdot \mathrm{K}^{-1}$
>	représente la capacité d'un matériaux à transférer la chaleur par unité de surface

# Bilan d'enthalpie

De la même manière que l'on a pu faire un bilan de masse, ou de charges, on s'intéresse au bilan d'enthalpie au sein d'un volume fermé quelconque $\Omega$, ainsi l'enthalpie totale dans le volume peut s'exprimer $$H(t) = \iiint_\Omega h_v (\vec{r}, t) \ \mathrm{d}V$$où :
- $\mathrm{d}V = \mathrm{d}x \mathrm{d}y \mathrm{d}z$
- $h_v$ est l'enthalpie volumique

Ainsi, l'enthalpie à un temps $t + \mathrm{d}t$ devient $$H(t + \mathrm{d}t) = \iiint_\Omega h_v (\vec{r}, t + \mathrm{d}t) \ \mathrm{d}V$$ce qui nous permet d'en déduire la variation d'enthalpie dans le temps $$\begin{align}
\mathrm{d}H &= H(t + \mathrm{d}t) - H(t) \\
&= \iiint_\Omega h_v(\vec{r}, t + \mathrm{d}t) - h_v (\vec{r}, t) \ \mathrm{d}V\\
&= \iiint_\Omega \frac{\partial h_v}{\partial t} \ \mathrm{d}t \ \mathrm{d}V\\
\Rightarrow \frac{\mathrm{d}H}{\mathrm{d}t} &= \iiint_\Omega \frac{\partial h_v}{\partial t} \ \mathrm{d}V
\end{align}$$De plus, on peut relier une variation d'enthalpie volumique à une variation de température grâce ç la relation $\mathrm{d} h_v = \rho c_p \ \mathrm{d}T$ , cela donne $$\frac{\mathrm{d} H}{\mathrm{d}t} = \rho c_p \iiint_\Omega \frac{\partial T}{\partial t} \ \mathrm{d}V$$où on a considéré $\rho$ et $c_p$ constants.

En introduisant $\vec{j}_q$, on peut relier la variation d'enthalpie à cette grandeur avec la relation suivante $$\frac{\mathrm{d} H}{\mathrm{d} t} = - \oint_{\partial \Omega} \vec{j}_q \cdot \mathrm{d}\vec{S}$$Ce qui nous permet d'écrire le bilan d'enthalpie avec le [[Identités d'analyse vectorielle#^8b3e75|théorème de la divergence]] $$\begin{align}
&\Rightarrow \rho c_p \int_\Omega \frac{\partial T}{\partial t} \ \mathrm{d}V + \oint_{\partial \Omega} \vec{j}_q \cdot \mathrm{d} \vec{S} = 0 \\
&\Rightarrow \int_\Omega \rho c_p \frac{\partial T}{\partial t} + \nabla \cdot \vec{j}_q \ \mathrm{d}V = 0, \quad \forall \Omega\\
&\Rightarrow \rho c_p \frac{\partial T}{\partial t} + \nabla \cdot \vec{j}_q = 0\\
&\Rightarrow \rho c_p \frac{\partial T}{\partial t} = - \nabla \cdot \vec{j}_q
\end{align}$$On obtient alors le bilan local d'enthalpie, il s'agit d'une relation qui doit rester vraie en tout points de l'espace.

# Loi de Fourier

On s'intéresse alors à la loi de Fourier pour continuer de transformer le bilan d'enthalpie. Elle se formule ainsi 

> [!Théorème] Loi de Fourier
> Dans une région d'un système où il existe un gradient de température, ce dernier est proportionnel à la densité du flux de chaleur $$\vec{j}_q = - \lambda \nabla T$$

# Equation de la chaleur

En utilisant la loi de Fourier et le bilan local d'enthalpie on peut retrouver une équation différentielle exprimée uniquement en terme du champ de température.

> [!théorème] Equation de la chaleur
> Dans un système, la variation dans le temps de la température en un point est proportionnel au laplacien du champ de température$$\begin{align}
\rho c_p \frac{\partial T}{\partial t} = - \lambda \nabla^2 T \\
\Rightarrow \frac{\partial T}{\partial t} = \alpha \nabla^2 T
\end{align}$$où
> - $\displaystyle \alpha = \frac{\lambda}{\rho c_p}$ est la diffusivité thermique
