# 7. Expressions locales de l'EM quasi-stationnaire

## 7.1. Expression locale du [théorème de Gauss](https://en.wikipedia.org/wiki/Gauss%27s_law)

### Rappel de l'expression intégrale

> [!théorème] Théorème de Gauss
> ![[Pasted image 20240330170400.png]]
> Soit l'expression intégrale du théorème de Gauss (aussi appelé loi de Gauss), donnant l'expression du flux total $\Phi$ du champ électrique $\vec{E}$ à travers une surface fermée $S$ contenant une charge $Q$ $$\boxed{\Phi = \oint_S \vec{E}\cdot \mathrm{d}\vec{S} = \frac{Q}{\varepsilon_0}}$$

> [!démo]- Démonstration du théorème de Gauss
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

### Expression locale

En partant du volume élémentaire de charge élémentaire $\mathrm{d}q = \rho \mathrm{d}\tau$ et en appliquant 
- le théorème de Gauss $$\mathrm{d}\Phi = \frac{\rho \mathrm{d} \tau}{\varepsilon_0}$$
- le [théorème de la divergence](https://en.wikipedia.org/wiki/Divergence_theorem) $$\mathrm{d} \Phi = \vec{\nabla} \cdot \vec{E} \ \mathrm{d} \tau$$
on trouve alors $\displaystyle \boxed{\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\varepsilon_0}}$ 

> [!démo]- Démonstration du théorème de la divergence
> Contents

### [Équation de Poisson](https://en.wikipedia.org/wiki/Poisson's_equation)

Par définition, $\vec{E} = - \vec{\nabla} V \Rightarrow \vec{\nabla} \cdot \vec{E} = - \nabla^2 V$ , or d'après le théorème de Gauss $\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\varepsilon_0}$ donc cela donne $$\Rightarrow \nabla^2 V = -\frac{\rho}{\varepsilon_0}$$
## 7.2. Flux du champ magnétique

Par définition, le flux se calcule comme suit $$\Phi = \oint_S \vec{B}\cdot\mathrm{d}\vec{S}$$par le théorème de la divergence$$\Phi = \oint_S \vec{B}\cdot\mathrm{d}\vec{S} = \int_V \vec{\nabla} \cdot \vec{B} \ \mathrm{d}V$$et donc, d'après la loi de Gauss pour le magnétisme, $\vec{\nabla} \cdot \vec{B} = 0$ cela donne au final $$\boxed{\Phi = 0}$$

## 7.3. Expression locale du [théorème d'Ampère](https://en.wikipedia.org/wiki/Amp%C3%A8re's_circuital_law)

### Rappel de l'expression intégrale

> [!théorème] Théorème d'Ampère
> En introduisant $\vec{H} = \frac{\vec{B}}{\mu_0}$, le théorème d'ampère s'exprime comme suit $$\Gamma = \oint_C \vec{H} \cdot \mathrm{d}\vec{l} = I$$ 
> ![[Pasted image 20240330170622.png]]

### Expression locale

On rappelle que $I$ est la somme des courants $\vec{J}$ à travers la surface délimitée par $C$ $$I = \iint_S \vec{J}\cdot \mathrm{d}\vec{S}$$en appliquant le [théorème de Stokes](https://en.wikipedia.org/wiki/Stokes'_theorem) qui peut s'exprimer comme suit 

> [!théorème] Théorème de Stokes
> Soit $S$ une surface orientée lisse dans $\mathbb{R}^3$ avec comme bord $C \equiv \partial S$. Si un champ vectoriel $\vec{F}(x,y,z)$ est défini et a toutes ses dérivées partielles d'ordre 1 continues dans une région contenant $S$ alors $$\iint_S (\vec{\nabla} \times \vec{F})\cdot \mathrm{d}\vec{S} = \oint_{\partial S} \vec{F} \cdot \mathrm{d}\vec{C}$$

> [!démo]- Démonstration du théorème de Stokes
> Contents

On trouve alors $$\begin{align}
\iint_S (\vec{\nabla} \times \vec{H})\cdot \mathrm{d}\vec{S} &= \oint_{\partial S} \vec{H} \cdot \mathrm{d}\vec{C} = \iint_S \vec{J}\cdot \mathrm{d}\vec{S} \\
&\Rightarrow \boxed{\vec{\nabla} \times \vec{H} = \vec{J}}
\end{align}$$ ou alors en utilisant $\vec{B}$ $$\boxed{\vec{\nabla} \times \vec{B} = \mu_0\vec{J}}$$

### Relation potentiel vecteur-densité de courant

On introduit un champ vectoriel $\vec{A}$ défini tel que $\vec{\nabla} \times \vec{A} = \vec{B}$ $$\begin{align}
\vec{\nabla} \times \vec{B} &= \vec{\nabla} \times (\vec{\nabla} \times \vec{A}) \\
&= \vec{\nabla}(\vec{\nabla} \cdot \vec{A}) - \nabla^2 \vec{A} \\
&= \mu_0 \vec{J}
\end{align}$$si ensuite l'on choisit la jauge de Coulomb, c'est à dire telle que $\vec{\nabla} \cdot \vec{A} = 0$, on trouve$$\nabla^2\vec{A} = -\mu_0 \vec{J}$$On retrouve alors une autre équation de Poisson.

## 7.4. Expression locale de la [loi de Faraday](https://en.wikipedia.org/wiki/Faraday%27s_law_of_induction)

> [!théorème] Loi de Maxwell-Faraday
> En partant de l'expression du champ total exprimé grâce aux potentiels scalaire et vecteur on peut arriver à l'expression de Maxwell-Faraday $$\begin{align}
> \vec{E} &= -\vec{\nabla} V - \frac{\partial \vec{A}}{\partial t} \\
> \Rightarrow \vec{\nabla} \times \vec{E} &= -\vec{\nabla} \times \vec{\nabla} V - \vec{\nabla} \times \frac{\partial \vec{A}}{\partial t} \\
> &= -\frac{\partial}{\partial t} (\vec{\nabla} \times \vec{A}) \\
> \Rightarrow &\boxed{\vec{\nabla} \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}} 
> \end{align}$$

# 8. Champs EM dépendant du temps

- Électrostatique : $\displaystyle \frac{\partial\vec{E}}{\partial t} = 0$
- Magnétostatique $\displaystyle \frac{\partial \vec{B}}{\partial t} = 0$
- EM $\displaystyle \frac{\partial \vec{B}}{\partial t} \neq 0 \rightarrow \vec{E}, \quad \frac{\partial \vec{E}}{\partial t} \neq 0 \rightarrow \vec{E}$

---
## 8.1. Courant de déplacement

### Conservation de la charge
![[Pasted image 20240324215215.png]]
Sous forme intégrée, la conservation de la charge s'écrit$$\begin{align}
&\oint_{S}\rho \vec{v} \cdot \mathrm{d}\vec{S} = -\frac{\mathrm{d}Q}{\mathrm{d}t} \\ \Rightarrow &\oint_{S} \vec{J}\cdot \mathrm{d}\vec{S} = \iiint_{\Omega} \vec{\nabla}\cdot \vec{J} \mathrm{d} \tau = -\frac{\mathrm{d}Q}{\mathrm{d}t} \\
\Rightarrow &\frac{\mathrm{d}Q}{\mathrm{d}t} = \frac{\mathrm{d}}{\mathrm{d}t} \left(\iiint_{\Omega} \rho \mathrm{d} \tau \right) = \iiint_{\Omega} \frac{\partial \rho}{\partial t} \mathrm{d} \tau \\
\Rightarrow &\boxed{\vec{\nabla} \cdot \vec{J} + \frac{\partial \rho}{\partial t} = 0}
\end{align}$$

> [!NOTE] Discussion de l'équation de continuité 
> - Cas statique : $\displaystyle \frac{\partial \rho}{\partial t} = 0 \Rightarrow \vec{\nabla} \cdot \vec{J} = 0 \Rightarrow \vec{\nabla} \times \vec{B} = \mu_{0} \vec{J}$
> Ce qui fonctionne avec l'expression locale du théorème d'Ampère
> - Cas non statique : $\displaystyle \frac{\partial \rho}{\partial t} \neq 0 \Rightarrow \vec{\nabla}\cdot \vec{J} \neq 0 \Rightarrow \vec{\nabla} \times \vec{B} \neq \mu_{0}\vec{J}$
> Cependant on voit ici que cela ne fonctionne plus avec le théorème d'Ampère

### Equation d'Ampère-Maxwell

> [!théorème] Équation d'Ampère-Maxwell (forme locale)
> la forme locale de l'équation d'Ampère-Maxwell s'exprime comme suit $$\boxed{\vec{\nabla} \times \vec{B} = \mu_{0} \left(\vec{J} +\varepsilon_0 \frac{\partial \vec{E}}{\partial t}\right)}$$ avec $\vec{J}$ la densité de courant, $\mu_0$ et $\varepsilon_0$ les constantes du vide et $\vec{E}$ et $\vec{B}$ les champs électrique et magnétique

> [!démo]- Démonstration
Suggestion de Maxwell : Choisir $\vec{V}$ tel que $\vec{\nabla} \times \vec{B} = \vec{V}$ avec $\vec{\nabla}\cdot \vec{V} = 0$ et retrouver la limite statique $\mu_{0} \vec{J}$
>
> Mise en équation : Partant de $$\begin{align}
\vec{\nabla} \cdot \vec{E} &= \frac{\rho}{\varepsilon_{0}}\\
\Rightarrow \frac{\partial}{\partial t}(\vec{\nabla} \cdot (\varepsilon_{0}\vec{E})) &= \frac{\partial \rho}{\partial t} \\
\Rightarrow \vec{\nabla} \cdot \left( \frac{\partial (\varepsilon_{0} \vec{E})}{\partial t} \right) &= \frac{\partial \rho}{\partial t} = -\vec{\nabla} \cdot \vec{J}
\end{align}$$On trouve alors en faisant usage de l'équation de continuité $$\begin{align}
\vec{\nabla} \cdot \vec{J} + \vec{\nabla} \cdot \left( \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}\right) = 0 \\
\Rightarrow \vec{\nabla} \cdot \left( \vec{J} + \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}\right) = 0 \\
\Rightarrow \vec{V} = \mu_{0}\left(\vec{J} + \varepsilon_{0}\frac{\partial \vec{E}}{\partial t}\right) \\
\Rightarrow \boxed{\vec{\nabla} \times \vec{B} = \mu_{0}\left(\vec{J} + \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}\right)}
\end{align}$$ où $\varepsilon_{0} \frac{\partial \vec{E}}{\partial t}$ définit le courant de déplacement.

### Forme intégrale de l'équation d'Ampère-Maxwell


> [!théorème] Équation d'Ampère-Maxwell (forme intégrale)
> la forme intégrale du théorème d'Ampère-Maxwell s'exprime comme suit $$\boxed{\oint_{C} \vec{B} \cdot \mathrm{d} \vec{l} = \mu_{0} \left(I + \varepsilon_{0} \frac{\mathrm{d} \Phi_{\mathrm{el}}}{\mathrm{d} t}\right)}$$où $I$ est le courant net à travers la surface délimitée par $C$ et $\Phi_{\mathrm{el}}$ est le flux électrique sur la dite surface

> [!démo]- Démonstration
> Grâce au théorème de Stokes on peut écrire $$\begin{align}
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

---
## 8.2. Équations de Maxwell

### Équations de Maxwell dans le vide

|                  | forme différentielle                                                                                                  | forme intégrale                                                                                                                           |
| ---------------- | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Gauss            | $$\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\varepsilon_0}$$                                                           | $$\oint_{S} \vec{E} \cdot \mathrm{d} \vec{S}= \frac{Q}{\varepsilon_0}$$                                                                   |
| Gauss magnétique | $$\vec{\nabla} \cdot \vec{B} = 0$$                                                                                    | $$\oint_{S} \vec{B} \cdot \mathrm{d} \vec{S}= 0$$                                                                                         |
| Maxwell-Faraday  | $$\vec{\nabla} \times \vec{E} = - \frac{\partial \vec{B}}{\partial t}$$                                               | $$\oint_{C} \vec{E} \cdot \mathrm{d} \vec{l}= -\frac{\mathrm{d}\Phi_\mathrm{m}}{\mathrm{d}t}$$                                            |
| Ampère-Maxwell   | $$\vec{\nabla} \times \vec{B} = \mu_{0} \left( \vec{J} + \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}\right)$$ | $$\oint_{C} \vec{B} \cdot \mathrm{d} \vec{l}=\mu_{0} \left( I + \varepsilon_{0} \frac{\mathrm{d} \Phi_\mathrm{el}}{\mathrm{d} t}\right)$$ |

### Équations de Maxwell dans un milieu 

|                  | forme différentielle                                                                       | forme intégrale                                                                                                   |
| ---------------- | ------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------- |
| Gauss            | $$\vec{\nabla} \cdot \vec{D} = \rho_\mathrm{f} $$                                          | $$\oint_{S} \vec{D} \cdot \mathrm{d} \vec{S}= Q_\mathrm{f}$$                                                      |
| Gauss magnétique | $$\vec{\nabla} \cdot \vec{B} = 0$$                                                         | $$\oint_{S} \vec{B} \cdot \mathrm{d} \vec{S}= 0$$                                                                 |
| Maxwell-Faraday  | $$\vec{\nabla} \times \vec{E} = - \frac{\partial \vec{B}}{\partial t}$$                    | $$\oint_{C} \vec{E} \cdot \mathrm{d} \vec{l}= -\frac{\mathrm{d}\Phi_\mathrm{m}}{\mathrm{d}t}$$                    |
| Ampère-Maxwell   | $$\vec{\nabla} \times \vec{H} = \vec{J}_\mathrm{f} + \frac{\partial \vec{D}}{\partial t}$$ | $$\oint_{C} \vec{H} \cdot \mathrm{d} \vec{l}= I_\mathrm{f} +  \frac{\mathrm{d} \Phi_\mathrm{ind}}{\mathrm{d} t}$$ |
où :
- $\vec{D} = \varepsilon_{0} \vec{E} + \vec{P}$ est le **vecteur induction électrique**
- $\displaystyle \vec{P} = \frac{\mathrm{d} \vec{p}}{\mathrm{d} \tau}$ est le **vecteur polarisation** avec $\vec{p}$ le **moment dipolaire**
- $\displaystyle \vec{H} = \frac{\vec{B}}{\mu_0} - \vec{M}$ est le vecteur **champ d'aimantation**, ou **champ d'excitation magnétique** (officiellement, il faudrait l'appeler **champ magnétique**, cependant cela porte à confusion avec $\vec{B}$ qu'on devrait appeler **vecteur induction magnétique**)
- $\displaystyle \vec{M} = \frac{\mathrm{d} \vec{m}}{\mathrm{d} \tau}$ est le **vecteur aimantation** avec $\vec{m}$ le **moment magnétique**

> [!théorème] Ampère-Maxwell dans un milieu quelconque
$$\vec{\nabla} \times \vec{B} = \mu_{0} \left( \vec{J}_c + \vec{\nabla} \times \vec{M} + \varepsilon_{0} \frac{\partial \vec{E}}{\partial t} + \frac{\partial \vec{P}}{\partial t}\right)$$
> où :
> - $\vec{J}_{c}$ : courant de conduction
> - $\vec{J}_{a}= \vec{\nabla} \times \vec{M}$ : courant d'aimentation
> - $\varepsilon_{0}\frac{\partial \vec{E}}{\partial t}$ : courant de déplacement du vide
> - $\frac{\partial \vec{P}}{\partial t}$ : courant de polarisation

#### Charges et courant libres

Quand on applique un champ électrique à un matériaux diélectrique (isolant), le champ induit un petit déplacement des porteurs de charge au sein du matériau. Les électrons se décalent dans une direction et les noyaux dans la direction opposé, créant des dipôles électriques. Cela produit à l'échelle macroscopique une charge liée dans le matériau. Par exemple, si toutes les molécules réagissent au champ de la même manière, comme montré dans la figure ci-dessous, cela crée une charge négative sur un coté du matériau, et une charge positive sur le côté opposé. On décrit cette charge facilement avec le vecteur de polarisation $\vec{P}$.
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
---

## 8.3. Potentiels électromagnétiques 

### Définition des potentiels électromagnétiques

Les équations de maxwell ont deux équations indépendantes du milieu, la loi de Gauss magnétique et la loi de Maxwell-Faraday :$$\begin{align}
\vec{\nabla} \cdot \vec{B} = 0 &\Rightarrow \vec{B} = \vec{\nabla} \times \vec{A} \\
\vec{\nabla} \times \vec{E} = - \frac{\partial \vec{B}}{\partial t} &\Rightarrow \vec{\nabla} \times \left( \vec{E} + \frac{\partial \vec{A}}{\partial t} \right) = 0 
\end{align}$$on notera $$\begin{align}
\vec{E} + \frac{\partial \vec{A}}{\partial t} &= - \vec{\nabla}V \\
\Rightarrow \vec{E} &= -\vec{\nabla}V - \frac{\partial \vec{A}}{\partial t} \\
\Rightarrow \vec{B} &= \vec{\nabla} \times \vec{A}
\end{align}$$$\vec{A}$ : potentiel vecteur/potentiel magnétique
$V$ : potentiel scalaire/potentiel électrique

### Transformation / Invariance de jauge

L'invariance de jauge est le fait que les lois de l'électromagnétismes restent inchangées sous certaines transformations, appelées transformations de jauge. En l'occurrence, en électromagnétisme, les champs électriques et magnétiques sont des *quantités observables* qui lorsqu'on fait certains changement sur les potentiels qui les engendre, peuvent rester les mêmes. Un exemple bien connu est le fait d'ajouter une constante au potentiel électrique, qui ne change alors pas le champ électrique. Cette transformation là est donc une *invariance de jauge*. On a définit les potentiels électromagnétiques plus haut, on vérifie alors que les champs électromagnétiques peuvent rester les mêmes lorsqu'on fait une transformation aux potentiels, en ajoutant un gradient $\vec{\nabla}X$ au potentiel vecteur.$$\begin{align}
\vec{A}' &= \vec{A} + \vec{\nabla} X \\
\vec{B}' &= \vec{\nabla} \times \vec{A}' \\
&= \vec{\nabla} \times \vec{A} + \vec{\nabla} \times \vec{\nabla} X \\
&= \vec{B}
\end{align}$$$\vec{A}$ est donc défini à un gradient près. Afin de vérifier l'invariance, il faut faire le changement correspondant sur $V$ $$\begin{align}
V' &= V - \frac{\partial X}{\partial t} \\
\vec{E}' &= - \vec{\nabla}V' - \frac{\partial \vec{A}'}{\partial t} \\
&= - \vec{\nabla}V + \vec{\nabla}\frac{\partial X}{\partial t} - \frac{\partial \vec{A}}{\partial t} - \frac{\partial \vec{\nabla} X}{\partial t} \\
&= \vec{E}
\end{align}$$On a donc vérifié qu'il existait une classe de transformations non triviales pour lesquelles le champ électromagnétique reste inchangé, appelées transformations de jauge. On les résume ci-après$$\begin{pmatrix}\vec{A} \\ V\end{pmatrix} \mapsto \begin{pmatrix} \vec{A}' = \vec{A} + \vec{\nabla}X \\ V' = V - \frac{\partial X}{\partial t}\end{pmatrix}$$où $X$ est un champ scalaire quelconque.
### Équations de propagation des potentiels

En partant de l'équation d'Ampère-Maxwell et de l'expression des potentiels on peut trouver$$\begin{align}
& \vec{\nabla} \times \vec{B} = \mu_{0} \left( \vec{J} + \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}\right) \\
&\Rightarrow \vec{\nabla} \times (\vec{\nabla} \times \vec{A}) = \mu_{0}\left( \vec{J} + \varepsilon_{0} \frac{\partial}{\partial t} \left( - \vec{\nabla}V - \frac{\partial \vec{A}}{\partial t} \right) \right) \\
&\Rightarrow \vec{\nabla} \times (\vec{\nabla} \cdot \vec{A}) - \nabla^{2} \vec{A} = \mu_{0} \vec{J} - \varepsilon_{0} \mu_{0} \frac{\partial}{\partial t} \vec{\nabla} V - \varepsilon_{0} \mu_{0} \frac{\partial^{2} \vec{A}}{\partial t^{2}} \\
&\Rightarrow \nabla^{2} \vec{A} - \varepsilon_{0} \mu_{0} \frac{\partial^{2} \vec{A}}{\partial t^{2}} - \vec{\nabla} \left( \vec{\nabla} \cdot \vec{A} + \varepsilon_{0} \mu_{0} \frac{\partial V}{\partial t} \right) = - \mu_{0} \vec{J} \\
c^{2} = \frac{1}{\varepsilon_{0} \mu_{0}}&\Rightarrow \nabla^{2} \vec{A} - \frac{1}{c^{2}} \frac{\partial^{2} \vec{A}}{\partial t^{2}} - \vec{\nabla} \left( \vec{\nabla} \cdot \vec{A} + \frac{1}{c^{2}} \frac{\partial V}{\partial t} \right) = -\mu_{0} \vec{J}
\end{align}$$Gauss $\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\varepsilon_0}$ permet par ailleurs d'écrire $$\begin{align}
\vec{\nabla} \cdot \left(\vec{\nabla} V + \frac{\partial \vec{A}}{\partial t}\right) &= -\frac{\rho}{\varepsilon_{0}}\\
\Rightarrow \nabla^{2} V + \frac{\partial}{\partial t} \vec{\nabla} \cdot \vec{A} &= -\frac{\rho}{\varepsilon_0}
\end{align}$$On choisit $\vec{\nabla} \cdot \vec{A} + \frac{1}{c^{2}}\frac{\partial V}{\partial t} = 0$, Donc on choisit $X$ dans $$\begin{dcases} 
\vec{A}' = \vec{A} + \vec{\nabla}X \\
V' = V - \frac{\partial X}{\partial t}
\end{dcases}$$tel que $$\begin{align}
\vec{\nabla} \cdot \vec{A}' + \frac{1}{c^{2}} \frac{\partial V'}{\partial t} = 0 \\
\Rightarrow \vec{\nabla} \cdot \vec{A} + \nabla^{2}X + \frac{1}{c^{2}} \frac{\partial V}{\partial t} - \frac{1}{c^{2}} \frac{\partial^{2}X}{\partial t^{2}} = 0\\
\Rightarrow \nabla^{2}X-\frac{1}{c^{2}} \frac{\partial^{2} X}{\partial t^{2}} =0
\end{align}$$ainsi, comme il est toujours possible de choisir $X$ tel que la précédente condition soit remplie, on peut écrire à l'aide de la jauge de Lorenz$$\vec{\nabla} \cdot \vec{A} + \frac{1}{c^{2}}\frac{\partial V}{\partial t} = 0 \Rightarrow \boxed{\begin{align}
\nabla^{2} \vec{A} - \frac{1}{c^{2}} \frac{\partial^{2} \vec{A}}{\partial t^{2}} = -\mu_{0} \vec{J} \\
\nabla^{2} V - \frac{1}{c^{2}} \frac{\partial^{2} V}{\partial t^{2}} = - \frac{\rho}{\varepsilon_0}
\end{align}}$$On se retrouve donc avec deux équations d'onde, une pour le potentiel vecteur, et une autre pour le potentiel scalaire (pouvant être regroupés dans le 4-potentiel), démontrant que les potentiels se propagent comme des ondes à la vitesse $c$. Il s'agit également d'une autre manière d'écrire les équations de Maxwell d'une manière qui fait apparaître la symétrie entre magnétisme et électricité.

---
## 8.4. Énergie électromagnétique - Vecteur de Poynting

### Cas statique

Dans le cas statique, on définit la densité d'énergie $w$ comme étant $$w = \frac{1}{2} \left(\varepsilon_{0} E^{2}+ \frac{B^2}{\mu_0}\right)$$
### Cas non statique

Si $\vec{E}$ et $\vec{B}$ dépendent du temps, alors $w$ aussi va dépendre du temps. Si $w$ venait à diminuer, où irait l'énergie ?
On définit alors le vecteur de Poynting $\vec{\Pi} = \frac{\vec{E} \times \vec{B}}{\mu_{0}}$, ayant une unité de W/m². Ce vecteur donne la direction de propagation de l'énergie électromagnétique par unité de surface et de temps. Il intervient dans la formulation du théorème de Poynting ci-après

> [!théorème] Théorème de Poynting
> Le théorème de Poynting dit que la variation dans le temps de transfert de l'énergie par unité de volume d'une région donnée de l'espace vaut la variation dans le temps de travail fait sur une distribution de charge dans cette région de l'espace, plus le flux d'énergie qui quitte ladite région$$\boxed{-\frac{\partial w}{\partial t} = \vec{\nabla} \cdot \vec{\Pi} + P}$$où : 
> - $\displaystyle -\frac{\partial w}{\partial t}$ est la variation de transfert de l'énergie par unité de volume (en $\mathrm{J}\ \mathrm{m}^{-3}\ \mathrm{s}^{-1}$, équivalent à $\mathrm{W}\ \mathrm{m}^{-3}$)
> - $\vec{\nabla} \cdot \vec{\Pi}$ est le flux d'énergie qui quitte la région de l'espace, 
> - $P$ est la puissance, c'est à dire la variation de travail fait par les champs sur les charges dans la région donnée de l'espace
> 
> En intégrant sur un volume et en utilisant le théorème de la divergence on obtient la forme intégrale du théorème$$\boxed{-\frac{\mathrm{d}}{\mathrm{d}t} \int_V w \ \mathrm{d}V = \oint_{\partial V} \vec{\Pi} \cdot \ \mathrm{d}\vec{S} + \int_V P \ \mathrm{d}V}$$

> [!démo]- Dérivation du théorème de Poynting
> Soit une distribution de charges $\rho$ avec une vitesse $\vec{v}$, la force de Laplace s'exprime alors$$\vec{F} = \rho(\vec{E} + \vec{v} \times \vec{B})$$Le travail de $\vec{F}$ par unité de temps, c'est à dire la puissance $P$ de $\vec{F}$ devient$$\begin{align}
> P &= \frac{\mathrm{d} W}{\mathrm{d} t} \\
> &= \vec{F} \cdot \vec{v} \\
> &= \rho(\vec{E} + \vec{v} \times \vec{B}) \cdot \vec{v} \\
> &= \rho \vec{E} \cdot \vec{v} + 0 \\
> &= \vec{J} \cdot \vec{E}
> \end{align}$$Ampère-Maxwell : $$\begin{align}
> \vec{\nabla} \times \vec{B} &= \mu_{0}\left(\vec{J} + \varepsilon_{0}\frac{\partial \vec{E}}{\partial t}\right) \\
> \Rightarrow \vec{J} &= \frac{\vec{\nabla} \times \vec{B}}{\mu_{0}}- \varepsilon_{0} \frac{\partial \vec{E}}{\partial t} \\
> \Rightarrow P &= \vec{E} \cdot \frac{\vec{\nabla} \times \vec{B}}{\mu_{0}}- \varepsilon_{0}\vec{E} \cdot \frac{\partial \vec{E}}{\partial t}\\
> &= \vec{E} \cdot \frac{\vec{\nabla} \times \vec{B}}{\mu_{0}} - \frac{\varepsilon_{0}}{2} \frac{\partial E^{2}}{\partial t}
> \end{align}$$En faisant usage de l'identité$$\begin{align}
> \vec{\nabla} \cdot (\vec{a} \times \vec{b}) &= \vec{b} \cdot (\vec{\nabla} \times \vec{a}) - \vec{a} \cdot (\vec{\nabla} \times \vec{b})\\
> \Rightarrow \vec{a} \cdot (\vec{\nabla} \times \vec{b}) &= - \vec{\nabla} \cdot (\vec{a} \times \vec{b}) + \vec{a} \cdot (\vec{\nabla} \times \vec{b}) \\
> \Rightarrow \vec{E} \cdot \frac{\nabla \times \vec{B}}{\mu_{0}} &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} + \vec{B} \cdot \frac{\vec{\nabla} \times \vec{E}}{\mu_{0}}
> \end{align}$$puis grâce à Maxwell-Faraday$$\begin{align}
> \Rightarrow \vec{E} \cdot \frac{\nabla \times \vec{B}}{\mu_{0}} &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} - \vec{B} \cdot \frac{1}{\mu_{0}} \frac{\partial \vec{B}}{\partial t}\\
> \Rightarrow \vec{E} \cdot \frac{\nabla \times \vec{B}}{\mu_{0}} &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} - \frac{1}{2 \mu_{0}} \frac{\partial B^{2}}{\partial t}\\
> \Rightarrow P &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} - \frac{1}{2 \mu_{0}} \frac{\partial B^{2}}{\partial t} - \frac{\varepsilon_{0}}{2} \frac{\partial E^{2}}{\partial t}\\
> &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} - \frac{1}{2} \left( \frac{1}{\mu_{0}} \frac{\partial B^{2}}{\partial t} + \varepsilon_{0}\frac{\partial E^{2}}{\partial t}\right)\\
> &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} - \frac{\partial w}{\partial t}\\
> P &= - \vec{\nabla}\cdot \vec{\Pi} - \frac{\partial w}{\partial t}\\
> \Rightarrow &\boxed{-\frac{\partial w}{\partial t} = \vec{\nabla} \cdot \vec{\Pi} + P}
> \end{align}$$

Ainsi ce théorème permet de vérifier la conservation de l'énergie ainsi que de mettre en évidence l'effet Joule entre autres. 

---
# 9. Propagation du champ EM
## 9.1. Description mathématique d'une onde

*Généralités*

### Définition
![[ondes progressives regressives.png]]

>onde : perturbation qui se propage
>onde progressive $f (x - vt)$
>onde régressive $f(x+vt$)
### Onde sinusoïdale

$$P = f(x-vt) = A \cos \left(k(x-vt)\right)$$
$\exists$ 2 périodicités :
* période spatiale : $\displaystyle \lambda = \frac{2 \pi}{k}$
* période temporelle : $\displaystyle T = \frac{1}{f} = \frac{2 \pi}{\omega}$ avec $\omega T = k \lambda \Rightarrow \omega = kv$

#### Equation de propagation d'une onde à une dimension

on cherche l'équation différentielle de solution de la forme $$P = f (x \pm vt)$$changement de variable : $u = x \pm vt$
* première différentiation$$\begin{dcases} 
\frac{\partial f}{\partial x} = \frac{\partial f}{\partial u} \frac{\partial u}{\partial x} = \frac{\mathrm{d} f}{\mathrm{d} u} \\
\frac{\partial f}{\partial t} = \frac{\partial f}{\partial u} \frac{\partial u}{\partial t} = \pm v\frac{\mathrm{d} f}{\mathrm{d} u}
\end{dcases}$$
* deuxième différentiation $$\begin{align*}
&\begin{dcases} 
\frac{\partial^2 f}{\partial x^2} = \frac{\partial}{\partial x} \left(\frac{\mathrm{d}f}{\mathrm{d}u}\right) = \frac{\mathrm{d}^2 f}{\mathrm{d}u^2} \frac{\partial u}{\partial x} = \frac{\mathrm{d}^2 f}{\mathrm{d}u^2} \\
\frac{\partial^2 f}{\partial t^2} = \frac{\partial}{\partial t} \left(\pm v\frac{\mathrm{d} f}{\mathrm{d} u}\right) = \pm v\frac{\mathrm{d}^2 f}{\mathrm{d}u^2} \frac{\partial u}{\partial t} = v^2\frac{\mathrm{d}^2 f}{\mathrm{d}u^2}
\end{dcases} \\ 
&\Rightarrow \frac{\partial^2 f}{\partial x^2} - \frac{1}{v^2} \frac{\partial^2 f}{\partial t^2} = 0 \quad \textrm{(Equation de propagation)}\\
&\Rightarrow \square f = 0
\end{align*}$$

c'est une équation linéaire d'ordre 2 de solution générale $f_1(x - vt) + f_2(x+vt)$

#### Onde à 3 dimensions

![[Ondes planes.png]]
##### Onde plane se propageant selon $x$+
$P = f(x-vt)$ 
Surface d'onde ou front d'onde est tel que $P$ est constant sur la surface à un temps donnée, pour une onde plane, la surface d'onde est alors un plan
##### **Onde plane se propageant dans une direction quelconque $\vec{k}$**
$P = f(\vec{k} \cdot \vec{r} - \omega t)$
##### Onde plane sinusoïdale
Pour une propagation selon $x$ positif : $P = A \cos (kx - \omega t)$
Pour une propagation selon une direction quelconque $\vec{k}$ : $P = A \cos (\vec{k} \cdot \vec{r} - \omega t)$ où $\vec{k}$ est le vecteur d'onde de norme $k$ (nombre d'onde).

##### Equation de propagation d'une onde à 3 dimensions

Partant de $f(\vec{k} \cdot \vec{r} - \omega t)$ et posant $\vec{k} \cdot \vec{r} - \omega t = a$ on trouve$$\frac{\partial f}{\partial x} = \frac{\mathrm{d} f}{\mathrm{d} a} \frac{\partial a}{\partial x} = k_x \frac{\mathrm{d} f}{\mathrm{d} a}$$et pareillement pour $y$ et $z$ $$\Rightarrow \begin{dcases} 
\frac{\partial^2 f}{\partial x^2} = k_x^2 \frac{\mathrm{d}^2 f}{\mathrm{d} a^2} \\
\frac{\partial^2 f}{\partial y^2} = k_y^2 \frac{\mathrm{d}^2 f}{\mathrm{d} a^2} \\
\frac{\partial^2 f}{\partial z^2} = k_z^2 \frac{\mathrm{d}^2 f}{\mathrm{d} a^2} 
\end{dcases}$$De même $$\frac{1}{\omega^2} \frac{\partial^2 f}{\partial t^2} = \frac{\mathrm{d}^2 f}{\mathrm{d} a^2}$$En remarquant que $k_x^2 + k_y^2 + k_z^2 = k^2$ et que $kv=\omega$ $$\begin{align*} 
&\Rightarrow \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2} - \frac{1}{v^2}\frac{\partial^2 f}{\partial t^2} = 0 \\
&\iff \nabla^2 f - \frac{1}{v^2}\frac{\partial^2 f}{\partial t^2} = 0 \\
&\iff \square f = 0
\end{align*}$$**Remarque** : Équation indépendante de $\vec{k}$, toute onde plane de vitesse $v$ est solution de l'équation d'onde pour toute direction $\Rightarrow$ infinité de solutions particulières, et solution générale $= \sum$ ondes planes générées en faisant varier $\vec{k}$ $\rightarrow$ toute onde à 3 dimensions de vitesse $v = \sum$ ondes planes

##### Ondes transversales et longitudinales 

###### Ondes longitudinales :
si $\vec{f}$ est un vecteur, alors $\vec{f} \parallel \vec{k}$ 

> [!example]+ Exemple
> une onde sonore, c'est à dire, la propagation d'ondes de pressions dans l'air. Cette onde induit un mouvement des molécules parallèlement à $\vec{k}$
> ![[Onde_compression_impulsion_1d_30_petit.gif]]

###### Ondes transversales : 
si $\vec{f}$ est un vecteur, alors $\vec{f} \perp \vec{k}$ 

> [!example]+ Exemple
> onde EM
> ![[Onde_cisaillement_impulsion_1d_30_petit.gif]] ![[Electromagneticwave3D.gif]]
> 

##### Ondes sphériques 

En symétrie sphérique, le Laplacien prend la forme $$\nabla^2 = \frac{1}{r} \frac{\partial^2 (rf)}{\partial r^2}$$on écrit donc l'équation d'onde $$\begin{align*} 
\frac{\partial^2 (rf)}{\partial r^2} - \frac{1}{v^2} \frac{\partial^2 (rf)}{\partial t^2} = 0 \\
\psi = rf \Rightarrow \frac{\partial^2 \psi}{\partial r^2} - \frac{1}{v^2} \frac{\partial^2 \psi}{\partial t^2} = 0 
\end{align*}$$
- **Solutions :** les deux solutions indépendantes en $\psi$ sont alors $\psi = \psi(r \pm vt)$
ainsi les ondes $f$ sont $$\begin{dcases} 
f_{\mathrm{sortante}} (r, t) = \frac{\psi (r-vt)}{r} \\ 
f_{\mathrm{rentrante}} (r, t) = \frac{\psi (r+vt)}{r}
\end{dcases}$$
- **Discussion :** 
>Onde plane $\rightarrow$ amplitude constante
>Onde sphérique $\rightarrow$ amplitude $\propto \frac{1}{r}$ 
>Cela se justifie par la conservation de l'énergie

### Propagation d'ondes EM

![[EM-Wave.gif]]
#### Equations de Maxwell

Pour un milieu localement neutre ($\rho = 0$) et isolant ($\sigma = 0$), on a :$$\begin{align}
&\vec{\nabla} \times \vec{H} = \frac{\partial \vec{D}}{\partial t} &\vec{B} = \mu \vec{H} & &\mu=\mu_0 \mu_r  \\
&\vec{\nabla} \times \vec{E} = -\frac{\partial \vec{B}}{\partial t} &\vec{D} = \varepsilon \vec{H} & &\varepsilon=\varepsilon_0 \varepsilon_r 
\end{align}$$ l'identité $\vec{\nabla} \times (\vec{\nabla} \times \vec{U}) = \vec{\nabla}(\vec{\nabla} \cdot \vec{U}) - \nabla^2 \vec{U}$ donne$$\begin{align*}
\vec{\nabla} \times (\vec{\nabla} \times \vec{H}) &= \vec{\nabla}(\vec{\nabla} \cdot \vec{H}) - \nabla^2 \vec{H} = - \nabla^2 \vec{H}\\
&= \vec{\nabla} \times\left(\frac{\partial \vec{D}}{\partial t}\right) \\
&= \varepsilon \frac{\partial}{\partial t}\left( \vec{\nabla} \times \vec{E} \right) \\
&= - \varepsilon \frac{\partial^2 \vec{B}}{\partial t^2} \\
&= - \nabla^2 \vec{H} = - \frac{\nabla^2 \vec{B}}{\mu}
\end{align*}$$ce qui donne l'équation de propagation des champs $$\Rightarrow \boxed{ \begin{align} 
\nabla^2 \vec{E} - \varepsilon \mu \frac{\partial^2 \vec{E}}{\partial t^2} = 0 \\
\nabla^2 \vec{B} - \varepsilon \mu \frac{\partial^2 \vec{B}}{\partial t^2} = 0
\end{align}}$$
#### Solution en onde plane 

Equation d'onde du type $$\nabla^2 \psi - \varepsilon \mu \frac{\partial^2 \psi}{\partial t^2} = 0$$où $\psi$ représente une composante quelconque de $\vec{E}$ ou $\vec{B}$, on définit alors par identification $$\mu \varepsilon = \frac{1}{v^2} \Rightarrow v = \frac{c}{n} = \frac{1}{\sqrt{\varepsilon \mu}}$$où $n$ est l'indice de réfraction. La solution générale $$\psi(\vec{r}, t) = f(\vec{k} \cdot \vec{r} - \omega t) + g(\vec{k} \cdot \vec{r} + \omega t)$$et on peut écrire les solutions sinusoïdale sous la forme complexe $$\psi(\vec{r}, t) \propto \exp\left(i\left(\vec{k} \cdot \vec{r} - \omega t\right)\right)$$
#### Propriétés de $\vec{E}$, $\vec{B}$ et $\vec{k}$ 

On peut montrer que $\left(\vec{E}, \vec{B}, \vec{k}\right)$ forment un trièdre rectangle direct. En effet on trouve$$\begin{align}
&\vec{\nabla} \cdot \vec{E} = i \vec{k} \cdot \vec{E} & &\vec{\nabla} \times \vec{E} = i \vec{k} \times \vec{E} \\
&\vec{\nabla} \cdot \vec{B} = i \vec{k} \cdot \vec{B} & &\vec{\nabla} \times \vec{B} = i \vec{k} \times \vec{B}
\end{align}$$Or comme $\rho = 0$ $$\begin{align}
&\vec{\nabla} \cdot \vec{E} = 0 &\Rightarrow &i\vec{k} \cdot \vec{E} = 0 &\Rightarrow &\vec{k} \perp \vec{E} \\
&\vec{\nabla} \cdot \vec{B} = 0 &\Rightarrow &i\vec{k} \cdot \vec{B} = 0 &\Rightarrow &\vec{k} \perp \vec{B} 
\end{align}$$
Par ailleurs, $$\begin{align}
&\vec{\nabla} \times \vec{E} + \frac{\partial \vec{B}}{\partial t} = 0 &\Rightarrow &i\vec{k} \times \vec{E} = i \omega \vec{B}\\
&\vec{\nabla} \times \vec{B} - \mu \varepsilon \frac{\partial \vec{E}}{\partial t}= 0 &\Rightarrow &i\vec{k} \times \vec{B} + i\varepsilon \mu \omega \vec{E}= 0 
\end{align}$$
#### Polarisation 

Comme $\vec{E}$ est transversal on peut l'écrire comme $$\vec{E} = (E_1 \hat{e}_1 + E_2 \hat{e}_2) \exp \left( i\left(\vec{k} \cdot \vec{r} - \omega t\right)\right) $$où $E_1$ et $E_2$ sont des constantes complexes qui contiennent l'information sur la phase entre eux. On peut écrire $E_1 = E_0^{(1)} e^{i \alpha}$ et $E_2 = E_0^{(2)} e^{i \beta}$ où $E_0$ est l'amplitude du champ et $\alpha$ et $\beta$ représente la phase. 

##### Polarisation linéaire

la polarisation linéaire se produit quand $\beta = \alpha \pm m \pi$, ce qui donne $$\vec{E} = (E_0^{(1)} \hat{e}_1 + E_0^{(2)} \hat{e}_2) \exp \left( i\left(\vec{k} \cdot \vec{r} - \omega t\right)\right)$$![[Linearly_polarized_wave_-_45_degrees.gif]]

##### Polarisation circulaire

la polarisation circulaire se produit lorsque $E_0^{(1)} = E_0^{(2)} = E_0$ et que $\beta = \alpha \pm \frac{\pi}{2}$, cela donne $$\vec{E} = E_0(\hat{e}_1 \pm i\hat{e}_2) \exp \left( i\left(\vec{k} \cdot \vec{r} - \omega t\right)\right)$$![[Circular_LH_polarization.gif]]
![[Circular_RH_polarization.gif]]
##### Polarisation elliptique

La polarisation elliptique est le cas général
![[Elliptical_RH_polarization.gif]]