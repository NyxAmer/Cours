---
tags:
  - Électromagnétisme
aliases:
  - Courant libre
  - Charges libres
  - Courant lié
  - Charges liées
---
Quand on applique un champ électrique à un matériaux diélectrique (isolant), le champ induit un petit déplacement des porteurs de charge au sein du matériau. Les électrons se décalent dans une direction et les noyaux dans la direction opposé, créant des dipôles électriques. Cela produit à l'échelle macroscopique une charge liée dans le matériau. 

Par exemple, si toutes les molécules réagissent au champ de la même manière, comme montré dans la figure ci-dessous, cela crée une charge négative sur un coté du matériau, et une charge positive sur le côté opposé. On décrit cette charge facilement avec le vecteur de polarisation $\vec{P}$.
![[Pasted image 20240402224756.png]]

Les charges libres sont alors les charges qui se déplacent dans le matériaux, comme par exemple les électrons de valence dans les matériaux conducteurs. Le courant libre est le courant engendré par leur mouvement. Les charges et courants libres et liés sont relié par les relations$$\begin{align}
Q &= Q_\mathrm{f} + Q_\mathrm{b} = \iiint_\Omega (\rho_\mathrm{f} + \rho_\mathrm{b}) \ \mathrm{d}V = \iiint_\Omega \rho \ \mathrm{d}V \\
I &= I_\mathrm{f} + I_\mathrm{b} = \iint_S (\vec{J}_\mathrm{f} + \vec{J}_b) \cdot \mathrm{d} \vec{S} = \iint_S \vec{J} \cdot \mathrm{d} \vec{S}
\end{align}$$où : 
- $\rho_\mathrm{f}$ et $Q_\mathrm{f}$ sont la densité de charge libre et la charge libre respectivement
- $\rho_\mathrm{b}$ et $Q_\mathrm{b}$ sont la densité de charge liée et la charge liée respectivement
- $\vec{J}_\mathrm{f}$ et $I_\mathrm{f}$ sont le vecteur de courant libre et le courant total libre respectivement
- $\vec{J}_\mathrm{b}$ et $I_\mathrm{b}$ sont le vecteur de courant lié et le courant total lié respectivement

On peut également définir le courant lié et la densité de charge liée en fonction de $\vec{P}$ et $\vec{M}$ $$\begin{align}
\rho_\mathrm{b} &= - \vec{\nabla} \cdot \vec{P} \\
\vec{J}_\mathrm{b} &= \nabla \times \vec{M} + \frac{\partial \vec{P}}{\partial t}
\end{align}$$