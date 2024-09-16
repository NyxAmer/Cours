---
tags:
  - Diffusion
---
On imagine la région d'un système où la densité $\rho(\vec{r}, t)$ est inhomogène, cette grandeur évolue alors selon des lois physiques.

# Bilan de masse

Dans un volume fixe $\Omega$ la masse totale est définie $$\begin{align}
m(t) &= \iiint_\Omega \rho(\vec{r}, t) \ \mathrm{d}V \\
m(t + \mathrm{d}t) &= \iiint_\Omega \rho(\vec{r}, t + \mathrm{d} t) \ \mathrm{d}V
\end{align}$$et donc la variation de masse $$\begin{align}
\mathrm{d}m &= m(t + \mathrm{d}t) - m(t) \\
&= \iiint_\Omega \rho(\vec{r}, t + \mathrm{d} t) \ \mathrm{d}V - \iiint_\Omega \rho(\vec{r}, t) \ \mathrm{d}V \\
&= \iiint_\Omega \frac{\partial \rho(\vec{r}, t)}{\partial t} \ \mathrm{d}t \ \mathrm{d}V \\
\Rightarrow \frac{\mathrm{d} m}{\mathrm{d} t} &= \iiint_\Omega \frac{\partial \rho(\vec{r}, t)}{\partial t} \ \mathrm{d}V
\end{align}$$La variation de masse est causée par le flux massique entrant à travers la surface fermée $\partial \Omega$ enveloppant $\Omega$. On suppose l'absence de sources de masse dans $\Omega$. $$\Rightarrow \frac{\mathrm{d} m}{\mathrm{d}t} = - \oint_{\partial \Omega} \vec{j} \cdot \mathrm{d} \vec{S}$$où $\vec{j}$ est la densité de flux massique en $\mathrm{kg} \cdot \mathrm{m}^{-2} \cdot \mathrm{s}^{-1}$
Donc le bilan de masse s'exprime $$\iiint_\Omega \frac{\partial \rho(\vec{r}, t)}{\partial t} \ \mathrm{d}V + \oint_{\partial \Omega} \vec{j} \cdot \mathrm{d} \vec{S} = 0$$Avec le [[Identités d'analyse vectorielle#^8b3e75|théorème de la divergence]] cela donne $$\iiint_\Omega \frac{\partial \rho(\vec{r}, t)}{\partial t} + \nabla \cdot \vec{j} \ \mathrm{d}V = 0$$Ainsi, pour que cette relation soit vérifiée $\forall \Omega$, il faut que l'intégrant soit nul $$\begin{align}
\frac{\partial \rho( \vec{r}, t)}{\partial t} + \nabla \cdot \vec{j} = 0 \\
\Rightarrow \frac{\partial \rho( \vec{r}, t)}{\partial t} = - \nabla \cdot \vec{j}
\end{align}$$Il s'agit du bilan de masse local, il donne la relation entre la variation temporelle de la densité et la variation spatiale de la densité du flux massique.

> [!Théorème] Loi de Fick
> Soit la relation reliant $\rho$ et $\vec{j}$ $$\vec{j} = - D \nabla \rho$$

> [!Théorème] Equation de la diffusion
> $$\frac{\partial \rho(\vec{r}, t)}{\partial t} = D \nabla^2 \rho$$

A noter que l'équation de la diffusion est la même que l'équation de la chaleur mais avec des dimensions différentes.

![[Diffusion0001-0500.mp4]]
Un exemple de la diffusion de particules dans une surface 2D obtenu par résolution numérique de l'équation de la diffusion