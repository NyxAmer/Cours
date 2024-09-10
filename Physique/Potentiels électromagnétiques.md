---
tags:
  - Électromagnétisme
---
# Définition des potentiels électromagnétiques

Les équations de maxwell ont deux équations indépendantes du milieu, la [[Théorème de Gauss|loi de Gauss]] et la loi de [[Loi de Faraday|Maxwell-Faraday]] :$$\begin{align}
\vec{\nabla} \cdot \vec{B} = 0 &\Rightarrow \vec{B} = \vec{\nabla} \times \vec{A} \\
\vec{\nabla} \times \vec{E} = - \frac{\partial \vec{B}}{\partial t} &\Rightarrow \vec{\nabla} \times \left( \vec{E} + \frac{\partial \vec{A}}{\partial t} \right) = 0 
\end{align}$$on notera $$\begin{align}
\vec{E} + \frac{\partial \vec{A}}{\partial t} &= - \vec{\nabla}V \\
\Rightarrow \vec{E} &= -\vec{\nabla}V - \frac{\partial \vec{A}}{\partial t} \\
\Rightarrow \vec{B} &= \vec{\nabla} \times \vec{A}
\end{align}$$où :
- $\vec{A}$ : **potentiel vecteur/potentiel magnétique**
- $V$ : **potentiel scalaire/potentiel électrique**

# Transformation / Invariance de jauge

L'invariance de jauge est le fait que les lois de l'électromagnétismes restent inchangées sous certaines transformations, appelées transformations de jauge. 

En l'occurrence, en électromagnétisme, les champs électriques et magnétiques sont des **quantités observables** qui lorsqu'on fait certains changement sur les potentiels qui les engendre, peuvent rester les mêmes. 

Un exemple bien connu est le fait d'ajouter une constante au potentiel électrique, qui ne change alors pas le champ électrique. Cette transformation là est donc une **invariance de jauge**. 

On a définit les potentiels électromagnétiques plus haut, on vérifie alors que les champs électromagnétiques peuvent rester les mêmes lorsqu'on fait une transformation aux potentiels, en ajoutant un gradient $\vec{\nabla}X$ au potentiel vecteur.$$\begin{align}
\vec{A}' &= \vec{A} + \vec{\nabla} X \\
\vec{B}' &= \vec{\nabla} \times \vec{A}' \\
&= \vec{\nabla} \times \vec{A} + \vec{\nabla} \times \vec{\nabla} X \\
&= \vec{B}
\end{align}$$$\vec{A}$ est donc défini à un gradient près. Afin de vérifier l'invariance, il faut faire le changement correspondant sur $V$ $$\begin{align}
V' &= V - \frac{\partial X}{\partial t} \\
\vec{E}' &= - \vec{\nabla}V' - \frac{\partial \vec{A}'}{\partial t} \\
&= - \vec{\nabla}V + \vec{\nabla}\frac{\partial X}{\partial t} - \frac{\partial \vec{A}}{\partial t} - \frac{\partial \vec{\nabla} X}{\partial t} \\
&= \vec{E}
\end{align}$$
On a donc vérifié qu'il existait une classe de transformations non triviales pour lesquelles le champ électromagnétique reste inchangé, appelées transformations de jauge. On les résume ci-après$$\begin{pmatrix}\vec{A} \\ V\end{pmatrix} \mapsto \begin{pmatrix} \vec{A}' = \vec{A} + \vec{\nabla}X \\ V' = V - \frac{\partial X}{\partial t}\end{pmatrix}$$où $X$ est un champ scalaire quelconque.
# Équations de propagation des potentiels

En partant de l'équation d'[[Théorème d'Ampère#^367cfd|Ampère-Maxwell]] et de l'expression des potentiels on peut trouver$$\begin{align}
& \vec{\nabla} \times \vec{B} = \mu_{0} \left( \vec{J} + \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}\right) \\
&\Rightarrow \vec{\nabla} \times (\vec{\nabla} \times \vec{A}) = \mu_{0}\left( \vec{J} + \varepsilon_{0} \frac{\partial}{\partial t} \left( - \vec{\nabla}V - \frac{\partial \vec{A}}{\partial t} \right) \right) \\
&\Rightarrow \vec{\nabla} \times (\vec{\nabla} \cdot \vec{A}) - \nabla^{2} \vec{A} = \mu_{0} \vec{J} - \varepsilon_{0} \mu_{0} \frac{\partial}{\partial t} \vec{\nabla} V - \varepsilon_{0} \mu_{0} \frac{\partial^{2} \vec{A}}{\partial t^{2}} \\
&\Rightarrow \nabla^{2} \vec{A} - \varepsilon_{0} \mu_{0} \frac{\partial^{2} \vec{A}}{\partial t^{2}} - \vec{\nabla} \left( \vec{\nabla} \cdot \vec{A} + \varepsilon_{0} \mu_{0} \frac{\partial V}{\partial t} \right) = - \mu_{0} \vec{J} \\
c^{2} = \frac{1}{\varepsilon_{0} \mu_{0}}&\Rightarrow \nabla^{2} \vec{A} - \frac{1}{c^{2}} \frac{\partial^{2} \vec{A}}{\partial t^{2}} - \vec{\nabla} \left( \vec{\nabla} \cdot \vec{A} + \frac{1}{c^{2}} \frac{\partial V}{\partial t} \right) = -\mu_{0} \vec{J}
\end{align}$$
la [[Théorème de Gauss|loi de Gauss]] $\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\varepsilon_0}$ permet par ailleurs d'écrire $$\begin{align}
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
\end{align}}$$
On se retrouve donc avec deux équations d'onde, une pour le potentiel vecteur, et une autre pour le potentiel scalaire (pouvant être regroupés dans le 4-potentiel), démontrant que les potentiels se propagent comme des ondes à la vitesse $c$. 

Il s'agit également d'une autre manière d'écrire les équations de Maxwell d'une manière qui fait apparaître la symétrie entre magnétisme et électricité.