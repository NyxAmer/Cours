---
tags:
  - Électromagnétisme
aliases:
  - Loi d'Ampère
  - Ampère-Maxwell
---
# Théorème d'Ampère
## Rappel de l'expression intégrale

> [!théorème] Théorème d'Ampère
> En introduisant $\vec{H} = \frac{\vec{B}}{\mu_0}$, le théorème d'ampère s'exprime comme suit $$\Gamma = \oint_C \vec{H} \cdot \mathrm{d}\vec{l} = I$$ 
> ![[Pasted image 20240330170622.png]]

## Expression locale

On rappelle que $I$ est la somme des courants $\vec{J}$ à travers la surface délimitée par $C$ $$I = \iint_S \vec{J}\cdot \mathrm{d}\vec{S}$$en appliquant le [[Identités d'analyse vectorielle#^f6bf6f|théorème de Stokes]] on trouve alors $$\begin{align}
\iint_S (\vec{\nabla} \times \vec{H})\cdot \mathrm{d}\vec{S} &= \oint_{\partial S} \vec{H} \cdot \mathrm{d}\vec{C} = \iint_S \vec{J}\cdot \mathrm{d}\vec{S} \\
&\Rightarrow \boxed{\vec{\nabla} \times \vec{H} = \vec{J}}
\end{align}$$ ou alors en utilisant $\vec{B}$ $$\boxed{\vec{\nabla} \times \vec{B} = \mu_0\vec{J}}$$

## Relation potentiel vecteur-densité de courant

On introduit un champ vectoriel $\vec{A}$ défini tel que $\vec{\nabla} \times \vec{A} = \vec{B}$ $$\begin{align}
\vec{\nabla} \times \vec{B} &= \vec{\nabla} \times (\vec{\nabla} \times \vec{A}) \\
&= \vec{\nabla}(\vec{\nabla} \cdot \vec{A}) - \nabla^2 \vec{A} \\
&= \mu_0 \vec{J}
\end{align}$$si ensuite l'on choisit la jauge de Coulomb, c'est à dire telle que $\vec{\nabla} \cdot \vec{A} = 0$, on trouve$$\nabla^2\vec{A} = -\mu_0 \vec{J}$$On retrouve alors une autre équation de Poisson.

---
# Equation d'Ampère-Maxwell

## Dans le vide
### Forme locale


> [!théorème] Équation d'Ampère-Maxwell (forme locale)
> la forme locale de l'équation d'Ampère-Maxwell s'exprime comme suit $$\boxed{\vec{\nabla} \times \vec{B} = \mu_{0} \left(\vec{J} +\varepsilon_0 \frac{\partial \vec{E}}{\partial t}\right)}$$ avec $\vec{J}$ la densité de courant, $\mu_0$ et $\varepsilon_0$ les constantes du vide et $\vec{E}$ et $\vec{B}$ les champs électrique et magnétique

^367cfd

> [!démo]- Démonstration
Suggestion de Maxwell : Choisir $\vec{V}$ tel que $\vec{\nabla} \times \vec{B} = \vec{V}$ avec $\vec{\nabla}\cdot \vec{V} = 0$ et retrouver la limite statique $\mu_{0} \vec{J}$
>
> Mise en équation : Partant de la [[Théorème de Gauss|loi de Gauss]] $$\begin{align}
\vec{\nabla} \cdot \vec{E} &= \frac{\rho}{\varepsilon_{0}}\\
\Rightarrow \frac{\partial}{\partial t}(\vec{\nabla} \cdot (\varepsilon_{0}\vec{E})) &= \frac{\partial \rho}{\partial t} \\
\Rightarrow \vec{\nabla} \cdot \left( \frac{\partial (\varepsilon_{0} \vec{E})}{\partial t} \right) &= \frac{\partial \rho}{\partial t} = -\vec{\nabla} \cdot \vec{J}
\end{align}$$On trouve alors en faisant usage de l'équation de continuité $$\begin{align}
\vec{\nabla} \cdot \vec{J} + \vec{\nabla} \cdot \left( \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}\right) = 0 \\
\Rightarrow \vec{\nabla} \cdot \left( \vec{J} + \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}\right) = 0 \\
\Rightarrow \vec{V} = \mu_{0}\left(\vec{J} + \varepsilon_{0}\frac{\partial \vec{E}}{\partial t}\right) \\
\Rightarrow \boxed{\vec{\nabla} \times \vec{B} = \mu_{0}\left(\vec{J} + \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}\right)}
\end{align}$$ où $\varepsilon_{0} \frac{\partial \vec{E}}{\partial t}$ définit le courant de déplacement.

### Forme intégrale


> [!théorème] Équation d'Ampère-Maxwell (forme intégrale)
> la forme intégrale du théorème d'Ampère-Maxwell s'exprime comme suit $$\boxed{\oint_{C} \vec{B} \cdot \mathrm{d} \vec{l} = \mu_{0} \left(I + \varepsilon_{0} \frac{\mathrm{d} \Phi_{\mathrm{el}}}{\mathrm{d} t}\right)}$$où $I$ est le courant net à travers la surface délimitée par $C$ et $\Phi_{\mathrm{el}}$ est le flux électrique sur la dite surface

> [!démo]- Démonstration
> Grâce au [[Identités d'analyse vectorielle#^f6bf6f|théorème de Stokes]] on peut écrire $$\begin{align}
> &\oint_{C} \vec{B} \cdot \mathrm{d} \vec{l} = \iint_{S} (\vec{\nabla} \times \vec{B}) \cdot \mathrm{d} \vec{S} &\\
> & = \mu_{0} \left(\iint_{S} \vec{J} \cdot \mathrm{d} \vec{S} + \varepsilon_{0} \iint_{S} \frac{\partial \vec{E}}{\partial t} \cdot \mathrm{d} \vec{S} \right) &\\
> \Rightarrow &\boxed{\oint_{C} \vec{B} \cdot \mathrm{d} \vec{l} = \mu_{0} \left(I + \varepsilon_{0} \frac{\mathrm{d} \Phi_{\mathrm{el}}}{\mathrm{d} t}\right)}&
> \end{align}$$

> [!example] Exemple : chargement d'une capacité
> ![[Pasted image 20240328224901.png]]
> Si on considère un condensateur, dont on représente un schéma ci-dessus, on va analyser le champ magnétique sur les surface $A_1$ et $A_2$
>
> En appliquant le théorème d'Ampère en ne considérant que $I = \iint_{S} \vec{J}\cdot \mathrm{d} \vec{S}$ $$\begin{align}
B_{\phi} = \frac{\mu_{0}I}{2 \pi r} \qquad (A_{1})\\
B_{\phi} = 0 \qquad (A_{2})
\end{align}$$
>
>En considérant le courant total $I + \varepsilon_{0} \frac{\mathrm{d} \Phi_\mathrm{el}}{\mathrm{d} t}$ $$\begin{align}
B_{\phi} = \frac{\mu_{0}I}{2 \pi r} \qquad (A_{1}) \\
(A_{2}) \oint_{C} \vec{B}\cdot \mathrm{d} \vec{l} &= \mu_{0} \left(0 + \varepsilon \frac{\mathrm{d} \Phi_\mathrm{el}}{\mathrm{d}t}\right) = 2 \pi r B_{\phi} \\
\Phi_\mathrm{el} &= SE = \frac{S \sigma}{\varepsilon_{0}} = \frac{Q}{\varepsilon_{0}}\\
\Rightarrow \varepsilon_{0} \frac{\mathrm{d} \Phi_\mathrm{el}}{\mathrm{d}t} &= \frac{\mathrm{d} Q}{\mathrm{d} t} = I \\
\Rightarrow \oint_{C} \vec{B} \cdot \mathrm{d} \vec{l} &= \mu_{0}I
\end{align}$$ 

## Dans un milieu

> [!théorème] Ampère-Maxwell dans un milieu quelconque
$$\vec{\nabla} \times \vec{B} = \mu_{0} \left( \vec{J}_c + \vec{\nabla} \times \vec{M} + \varepsilon_{0} \frac{\partial \vec{E}}{\partial t} + \frac{\partial \vec{P}}{\partial t}\right)$$
> où :
> - $\vec{J}_{c}$ : courant de conduction
> - $\vec{J}_{a}= \vec{\nabla} \times \vec{M}$ : courant d'aimentation
> - $\varepsilon_{0}\frac{\partial \vec{E}}{\partial t}$ : courant de déplacement du vide
> - $\frac{\partial \vec{P}}{\partial t}$ : courant de polarisation
