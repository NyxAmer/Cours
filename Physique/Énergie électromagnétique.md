---
tags:
  - Électromagnétisme
aliases:
  - Vecteur de Poynting
---
# Cas statique

Dans le cas statique, on définit la densité d'énergie $w$ comme étant $$w = \frac{1}{2} \left(\varepsilon_{0} E^{2}+ \frac{B^2}{\mu_0}\right)$$
# Cas non statique

Si $\vec{E}$ et $\vec{B}$ dépendent du temps, alors $w$ aussi va dépendre du temps. Si $w$ venait à diminuer, où irait l'énergie ?
On définit alors le vecteur de Poynting $\vec{\Pi} = \frac{\vec{E} \times \vec{B}}{\mu_{0}}$, ayant une unité de W/m². 

Ce vecteur donne la direction de propagation de l'énergie électromagnétique par unité de surface et de temps. Il intervient dans la formulation du théorème de Poynting ci-après

> [!théorème] Théorème de Poynting
> Le théorème de Poynting dit que la variation dans le temps de transfert de l'énergie par unité de volume d'une région donnée de l'espace vaut la variation dans le temps de travail fait sur une distribution de charge dans cette région de l'espace, plus le flux d'énergie qui quitte ladite région$$\boxed{-\frac{\partial w}{\partial t} = \vec{\nabla} \cdot \vec{\Pi} + P}$$où : 
> - $\displaystyle -\frac{\partial w}{\partial t}$ est la variation de transfert de l'énergie par unité de volume (en $\mathrm{J}\ \mathrm{m}^{-3}\ \mathrm{s}^{-1}$, équivalent à $\mathrm{W}\ \mathrm{m}^{-3}$)
> - $\vec{\nabla} \cdot \vec{\Pi}$ est le flux d'énergie qui quitte la région de l'espace, 
> - $P$ est la puissance, c'est à dire la variation de travail fait par les champs sur les charges dans la région donnée de l'espace
> 
> En intégrant sur un volume et en utilisant le [[Identités d'analyse vectorielle#^8b3e75|théorème de la divergence]] on obtient la forme intégrale du théorème$$\boxed{-\frac{\mathrm{d}}{\mathrm{d}t} \int_V w \ \mathrm{d}V = \oint_{\partial V} \vec{\Pi} \cdot \ \mathrm{d}\vec{S} + \int_V P \ \mathrm{d}V}$$

> [!démo]- Dérivation du théorème de Poynting
> Soit une distribution de charges $\rho$ avec une vitesse $\vec{v}$, la force de Laplace s'exprime alors$$\vec{F} = \rho(\vec{E} + \vec{v} \times \vec{B})$$Le travail de $\vec{F}$ par unité de temps, c'est à dire la puissance $P$ de $\vec{F}$ devient$$\begin{align}
> P &= \frac{\mathrm{d} W}{\mathrm{d} t} \\
> &= \vec{F} \cdot \vec{v} \\
> &= \rho(\vec{E} + \vec{v} \times \vec{B}) \cdot \vec{v} \\
> &= \rho \vec{E} \cdot \vec{v} + 0 \\
> &= \vec{J} \cdot \vec{E}
> \end{align}$$[[Théorème d'Ampère#^367cfd|Ampère-Maxwell]] : $$\begin{align}
> \vec{\nabla} \times \vec{B} &= \mu_{0}\left(\vec{J} + \varepsilon_{0}\frac{\partial \vec{E}}{\partial t}\right) \\
> \Rightarrow \vec{J} &= \frac{\vec{\nabla} \times \vec{B}}{\mu_{0}}- \varepsilon_{0} \frac{\partial \vec{E}}{\partial t} \\
> \Rightarrow P &= \vec{E} \cdot \frac{\vec{\nabla} \times \vec{B}}{\mu_{0}}- \varepsilon_{0}\vec{E} \cdot \frac{\partial \vec{E}}{\partial t}\\
> &= \vec{E} \cdot \frac{\vec{\nabla} \times \vec{B}}{\mu_{0}} - \frac{\varepsilon_{0}}{2} \frac{\partial E^{2}}{\partial t}
> \end{align}$$En faisant usage de l'identité$$\begin{align}
> \vec{\nabla} \cdot (\vec{a} \times \vec{b}) &= \vec{b} \cdot (\vec{\nabla} \times \vec{a}) - \vec{a} \cdot (\vec{\nabla} \times \vec{b})\\
> \Rightarrow \vec{a} \cdot (\vec{\nabla} \times \vec{b}) &= - \vec{\nabla} \cdot (\vec{a} \times \vec{b}) + \vec{a} \cdot (\vec{\nabla} \times \vec{b}) \\
> \Rightarrow \vec{E} \cdot \frac{\nabla \times \vec{B}}{\mu_{0}} &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} + \vec{B} \cdot \frac{\vec{\nabla} \times \vec{E}}{\mu_{0}}
> \end{align}$$puis grâce à [[Loi de Faraday|Maxwell-Faraday]]$$\begin{align}
> \Rightarrow \vec{E} \cdot \frac{\nabla \times \vec{B}}{\mu_{0}} &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} - \vec{B} \cdot \frac{1}{\mu_{0}} \frac{\partial \vec{B}}{\partial t}\\
> \Rightarrow \vec{E} \cdot \frac{\nabla \times \vec{B}}{\mu_{0}} &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} - \frac{1}{2 \mu_{0}} \frac{\partial B^{2}}{\partial t}\\
> \Rightarrow P &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} - \frac{1}{2 \mu_{0}} \frac{\partial B^{2}}{\partial t} - \frac{\varepsilon_{0}}{2} \frac{\partial E^{2}}{\partial t}\\
> &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} - \frac{1}{2} \left( \frac{1}{\mu_{0}} \frac{\partial B^{2}}{\partial t} + \varepsilon_{0}\frac{\partial E^{2}}{\partial t}\right)\\
> &= - \vec{\nabla}\cdot \frac{\vec{E} \times \vec{B}}{\mu_{0}} - \frac{\partial w}{\partial t}\\
> P &= - \vec{\nabla}\cdot \vec{\Pi} - \frac{\partial w}{\partial t}\\
> \Rightarrow &\boxed{-\frac{\partial w}{\partial t} = \vec{\nabla} \cdot \vec{\Pi} + P}
> \end{align}$$

Ainsi ce théorème permet de vérifier la conservation de l'énergie ainsi que de mettre en évidence l'effet Joule entre autres. 