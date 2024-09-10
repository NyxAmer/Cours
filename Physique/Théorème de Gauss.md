---
tags:
  - Électromagnétisme
aliases:
  - Loi de Gauss
---
![[Pasted image 20240330170400.png]]

# Expression intégrale

> [!théorème] Théorème de Gauss
>
> Soit l'expression intégrale du théorème de Gauss (aussi appelé loi de Gauss), donnant l'expression du flux total $\Phi$ du champ électrique $\vec{E}$ à travers une surface fermée $S$ contenant une charge $Q_{\mathrm{int}}$ $$\boxed{\Phi = \oint_S \vec{E}\cdot \mathrm{d}\vec{S} = \frac{Q_{\mathrm{int}}}{\varepsilon_0}}$$ 

^TdGaussInt

> [!démo]- Démonstration par les angles solides
> 
> ![[Pasted image 20240323183023.png]]
> On introduit le concept d'angle solide $\mathrm{d}\Omega$, on a alors la relation suivante $$\mathrm{d}\Omega = \frac{\mathrm{d}A_{\perp}}{r^2} = \frac{\mathrm{d}A \cos \alpha}{r^2}$$de plus on rappelle le flux sur une surface fermée $$\Phi = \oint \vec{E} \cdot \mathrm{d}\vec{A}= \oint \vec{E} \ \mathrm{d}A \cos \theta$$
>  Donc si on considère la contribution d'une charge extérieure, cette dernière a deux contributions au total
>  - Une contribution constante $\mathrm{d}\Phi$ à travers $\mathrm{d}A$
>  - Une contribution constante $\mathrm{d}\Phi'$ à travers $\mathrm{d}A'$> 
> 
>  de plus, par la définition de l'angle solide $$\mathrm{d} \Omega = \frac{\mathrm{d}A_{\perp}}{r^2} = \frac{\mathrm{d}A_{\perp}'}{r'^2}$$donc le flux à travers $\Omega$ est $$\begin{align}
> &\mathrm{d} \Phi = E\ \mathrm{d}A \cos \theta = \frac{kq}{r^2}\mathrm{d}A \cos \theta = -\frac{kq}{r^2}\mathrm{d}A \cos \alpha = -kq \mathrm{d}\Omega \\
> &\mathrm{d} \Phi' = E'\ \mathrm{d}A' \cos \theta' = kq \mathrm{d}\Omega \\
> \Rightarrow &\mathrm{d} \Phi + \mathrm{d} \Phi' = 0
> \end{align}$$
> 
> Contribution des charges internes
> ![[Pasted image 20240323185210.png]]
> On établi alors que $\mathrm{d} \Phi = kq \mathrm{d} \Omega$ et sachant que $$\begin{align}
> \Omega = \int_{S^2} \mathrm{d}\Omega = 4 \pi \\
> \Rightarrow \Phi = kq 4\pi
> \end{align}$$
> 
> Se faisant, le flux total s'écrit $$\boxed{\Phi_{\mathrm{total}} = 4\pi k \sum q_{\mathrm{int}} = \frac{Q}{\varepsilon_0}}$$

Ainsi le théorème de Gauss nous dit que le flux du champ électrique sur une surface est proportionnel à la charge enfermée par la surface.

Lorsque la surface n'enferme aucune charge, alors on devrait s'attendre à ce qu'il y ait autant de ligne de champ qui entre la surface que de lignes qui en sortent. Cela se traduit par un flux total nul. Autrement dit, les charges à l'extérieur de la surface ne contribuent pas au flux électrique total sur cette dernière.

![[Electric-flux-surface-example.svg.png|300]] ![[Electric-flux-no-charge-inside.svg.png|300]]
# Expression locale :)

> [!théorème] Théorème de Gauss (forme locale)
> En tout point de l'espace, le théorème de Gauss vérifie
> $$\boxed{\nabla \cdot \vec{E} = \frac{\rho}{\varepsilon_0}}$$où
> - $\vec{E}$ est le **champ électrique** et $\nabla \cdot \vec{E}$ dénote sa divergence
> - $\rho$ est la **densité de charge**
> - $\varepsilon_0$ est la **constante diélectrique du vide** ou **permittivité du vide** 

^TdGaussLocal

> [!démo]-
> En partant de l'expression de la charge élémentaire $\mathrm{d}q = \rho \mathrm{d}\tau$ et en appliquant 
> - le [[Théorème de Gauss#^TdGaussInt|théorème de Gauss]] $$\begin{align}
\Phi &= \frac{Q}{\varepsilon_0} \\
\Rightarrow \mathrm{d}\Phi &= \frac{\mathrm{d} q}{\varepsilon_0} \\
\Rightarrow \mathrm{d}\Phi &= \frac{\rho \ \mathrm{d} \tau}{\varepsilon_0}
\end{align}$$
> - le [[Identités d'analyse vectorielle#^8b3e75|théorème de la divergence]] $$\begin{align}
\Phi &= \oint_S \vec{E}\cdot \mathrm{d}\vec{S} \\
\Rightarrow \Phi &= \iiint_V (\nabla \cdot \vec{E}) \ \mathrm{d} \tau\\
\Rightarrow \mathrm{d} \Phi &= \vec{\nabla} \cdot \vec{E} \ \mathrm{d} \tau
\end{align}$$Ainsi obtient-on $$\begin{align}
\mathrm{d}\Phi = \nabla\cdot \vec{E} \ \mathrm{d} \tau = \frac{\rho}{\varepsilon_0} \ \mathrm{d}\tau \\
\Rightarrow \Aboxed{\nabla \cdot \vec{E} = \frac{\rho}{\varepsilon_0}}
\end{align}$$

Ainsi voit on exprimé par l'expression locale du théorème de Gauss que la divergence du champ électrique en un point est proportionnel à la densité de charge en ce point. 

Cela veut dire que les charges positives créent un champ électrique divergent et que les charges négatives créent un champ convergent.

![[VFPt_plus_thumb.svg.png|300]] ![[VFPt_minus_thumb.svg.png|300]]
# [Équation de Poisson](https://en.wikipedia.org/wiki/Poisson's_equation)

Par définition, $\vec{E} = - \vec{\nabla} V \Rightarrow \vec{\nabla} \cdot \vec{E} = - \nabla^2 V$ , or d'après le théorème de Gauss $\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\varepsilon_0}$ donc cela donne $$\Rightarrow \nabla^2 V = -\frac{\rho}{\varepsilon_0}.$$
Cette équation différentielle relit donc la densité de charge avec le potentiel électrique, ainsi peut-on facilement déduire la densité de charge à partir du potentiel électrique comme étant négativement proportionnel au laplacien du potentiel électrique.

De plus, cela veut également dire que l'on peut reconstruire le potentiel à partir de la densité de charge en résolvant l'équation.
