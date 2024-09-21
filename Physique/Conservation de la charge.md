---
tags:
  - Électromagnétisme
---
On va s'intéresser aux charges présentes dans un volume fini, et on va dériver un équation qui capture l'idée de la conservation de la charge. On considère une région de l'espace finie quelconque $\Omega$. Pour décrire la charge totale comprise dans cette région, on intègre la densité de charge (la charge volumique) sur le volume $$Q = \iiint_\Omega \rho \ \mathrm{d}V$$Comme on veut exprimer la conservation de la charge, on peut s'intéresser à sa variation dans le temps, ainsi en dérivant on obtient $$\begin{align}
\frac{\mathrm{d} Q}{\mathrm{d}t} &= \frac{\mathrm{d}}{\mathrm{d}t} \iiint_\Omega \rho \ \mathrm{d}V\\
\Rightarrow \frac{\mathrm{d}Q}{\mathrm{d}t} &= \iiint_\Omega \frac{\partial \rho}{\partial t} \ \mathrm{d}V
\end{align}$$où on peut inverser l'ordre d'intégration et de dérivation ([règle de Leibniz](https://en.wikipedia.org/wiki/Leibniz_integral_rule)) car on suppose l'intégrale définie (non infinie) sur notre volume d'étude $\Omega$, lui même supposé constant.

En se penchant sur l'idée du changement de la charge totale dans $\Omega$, on se rend compte qu'il faut prendre en compte la quantité de charge qui quitte le volume, et celle qui le pénètre. On représente cela par le courant $I$. Le courant est défini de manière analogue à la charge totale comme le mouvement total de charge, représentée par l'intégrale de la densité de courant sur toute la surface fermée $\partial \Omega$ qui entoure notre volume d'étude $\Omega$ $$I = - \oint_{\partial \Omega} \vec{J} \cdot \mathrm{d} \vec{S}$$

Le courant total sur la surface du volume doit être égal à la variation de la charge dans le volume afin d'assurer la conservation de la charge $$\begin{align}
I &= \frac{\mathrm{d} Q}{\mathrm{d} t}\\
\Rightarrow \oint_{\partial \Omega} \vec{J} \cdot \mathrm{d}\vec{S} &= - \frac{\mathrm{d} Q}{\mathrm{d} t}
\end{align}$$
Ainsi on obtient une égalité qu'on peut réarranger pour obtenir la forme intégrale et locale de la conservation de la charge, notamment en utilisant le [[Identités d'analyse vectorielle#^8b3e75|théorème de la divergence]] $$\begin{align}
\frac{\mathrm{d}Q}{\mathrm{d}t} = \iiint_\Omega \frac{\partial \rho}{\partial t} \ \mathrm{d} V &= - \oint_{\partial \Omega} \vec{J} \cdot \mathrm{d} \vec{S}\\
\Rightarrow \iiint_\Omega \frac{\partial \rho}{\partial t} \ \mathrm{d}V &+ \oint_{\partial \Omega} \vec{J} \cdot \mathrm{d} \vec{S} = 0\\
\Rightarrow \iiint_\Omega \frac{\partial \rho}{\partial t} &+ \nabla \cdot \vec{J} \ \mathrm{d} V = 0, \quad \forall \Omega\\
\Rightarrow \Aboxed{\frac{\partial \rho}{\partial t} &+ \nabla \cdot \vec{J}= 0}
\end{align}$$

![[Pasted image 20240324215215.png]]
Schéma d'un volume contenant une certaine quantité de charge $Q$, avec la densité de charge qui quitte ou pénètre le volume représenté en vert.

> [!NOTE] Discussion de l'équation de continuité 
> - Cas statique : $\displaystyle \frac{\partial \rho}{\partial t} = 0 \Rightarrow \vec{\nabla} \cdot \vec{J} = 0 \Rightarrow \vec{\nabla} \times \vec{B} = \mu_{0} \vec{J}$
> Ce qui fonctionne avec l'expression locale du théorème d'Ampère
> - Cas non statique : $\displaystyle \frac{\partial \rho}{\partial t} \neq 0 \Rightarrow \vec{\nabla}\cdot \vec{J} \neq 0 \Rightarrow \vec{\nabla} \times \vec{B} \neq \mu_{0}\vec{J}$
> Cependant on voit ici que cela ne fonctionne plus avec le théorème d'Ampère
