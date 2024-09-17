---
tags:
  - Mécanique/Analytique
---
# Principe d'Alembert

Dans un système physique, on va décrire toutes les forces qui y existent, et donc pour commencer les forces de contraintes $R$, qui permettent de vérifier les différentes contraintes (par exemple, la force de réaction des solides, les empêchant de se passer au travers). Par définition, ces forces ne travaillent pas$$\mathrm{d}W_R = \vec{R} \cdot \mathrm{d} \vec{s} = 0.$$
On va maintenant modéliser un déplacement virtuel $\delta \vec{r_i}$ comme un déplacement infinitésimal instantané, et en l'appliquant au système, on va étudier ce qui en résulte.

> [!Théorème] Le principe d'Alembert
> Dans un système physique, l'ensemble des forces de contraintes appliquées à un système ne travaillent pas lors d'un déplacement virtuel $\delta \vec{r_i}$. C'est à dire $$\delta W_R = \sum_i \vec{R_i} \cdot \delta \vec{r_i} = 0$$

## Cas statique

Mettons un système à $N$ points, tel qu'un solide indéformable. Les forces de contraintes appliquées à chaque point $\vec{R_i}$ se décomposent entre les forces de contraintes engendrées par l'environnement extérieur au système, et les forces de contraintes internes qui donnent les contraintes internes au système. $$\vec{R_i} = \vec{R}_i^{\mathrm{ext}} + \sum_{i \neq j} \vec{R}_{ij}^{\mathrm{int}}$$On ajoute à cela les forces extérieures pour obtenir toutes les force qui s'appliquent à chaque point$$\vec{F}_i = \vec{F}_i^{\mathrm{ext}} + \vec{R}_i$$or en équilibre, $\forall i$ $$\vec{F}_i = 0.$$
Et donc en considérant le travail des déplacements virtuels, on obtient $$\begin{align}
\delta W &= \sum_i \vec{F}_i \cdot \delta \vec{r}_i \\
\Rightarrow \delta W &= \sum_i \left( \vec{F}_i^{\mathrm{ext}} + \vec{R}_i \right) \cdot \delta \vec{r}_i = 0 \\
\Rightarrow \Aboxed{\delta W &= \sum_i \vec{F}_i^{\mathrm{ext}}  \cdot \delta \vec{r}_i = 0}
\end{align}$$
## Cas dynamique

La différence avec le cas statique est alors la présence de forces d'inerties, telles que données par la deuxième loi de Newton $$\vec{F} = - \dot{\vec{p}}$$Ainsi le travail des déplacements virtuels devient $$\begin{align}
\delta W &= \sum_i \left( \vec{F}_i^{\mathrm{ext}} - \dot{\vec{p}}_i \right) \cdot \delta \vec{r}_i = 0 \\
&= \sum_i \vec{F}_i^{\mathrm{ext}} \cdot \delta \vec{r}_i - \sum_i \dot{\vec{p}}_i \cdot \delta \vec{r}_i \\
&= \delta W^{(1)} + \delta W^{(2)} = 0
\end{align}$$
# Equation d'Euler-Lagrange

On peut dériver l'équation d'Euler-Lagrange uniquement à partir du principe d'Alembert, et on s'y attèle ci-après.
## Dérivation

On va maintenant décrire le système en terme de coordonnées généralisée $q_i$. Pour se faire on commence par donner des relations qu'on admettra pour la suite avec ces coordonnées et les coordonnées habituelles. Ces relations sont démontrables avec des concepts d'analyses mais nous passerons cette étape.

> [!Théorème] Relations admises
> $$\begin{align}
&(a) & \vec{r} &= \vec{r}_i (\mathbf{q}, t) \\
&(b) & \frac{\mathrm{d} \vec{r}_i}{\mathrm{d} t} &= \vec{v} (\mathbf{q}, \dot{\mathbf{q}}, t) = \sum_k \left( \frac{\partial \vec{r}_1}{\partial q_k} \frac{\mathrm{d} q_k}{\mathrm{d} t} \right) + \frac{\partial \vec{r}_i}{\partial t} \\
&(c) & \frac{\partial \vec{v}_i}{\partial \dot{q}_k} &= \frac{\partial \vec{r}_i}{\partial q_k} \\
&(d) & \frac{\mathrm{d}}{\mathrm{d} t} \frac{\partial \vec{r}_i}{\partial q_k} &= \frac{\partial}{\partial q_k} \frac{\mathrm{d} \vec{r}_i}{\mathrm{d} t} = \frac{\partial \vec{v}_i}{\partial q_k} \\
&(e) & \delta \vec{r}_i &= \sum_k \frac{\partial \vec{r}_i}{\partial q_k} \delta q_k + \cancelto{0}{\frac{\partial \vec{r}_i}{\partial t} \delta t}
\end{align}$$

Ainsi, on applique ces relations au cas du système dynamique (pour obtenir un solution plus générale) $$\begin{align}
\delta W^{(1)} &= \sum_i \vec{F}_i^{\mathrm{ext}} \cdot \delta \vec{r}_i \\
(e) \Rightarrow \delta W^{(1)} &= \sum_k \underbrace{\left( \sum_i \vec{F}_i^{\mathrm{ext}} \cdot \frac{\partial \vec{r}_i}{\partial q_k} \right)}_{\displaystyle Q_k} \delta q_k \\
\delta W^{(2)} &= - \sum_i \dot{\vec{p}}_i \cdot \delta \vec{r}_i  \\
(e) \Rightarrow \delta W^{(2)} &= \sum_k \left( \sum_i m_i \ddot{\vec{r}}_i \cdot \frac{\partial \vec{r}_i}{\partial q_k} \right) \delta q_k 
\end{align}$$Avec $\displaystyle \ddot{\vec{r}}_i \frac{\partial \vec{r}_i}{\partial q_k} = \frac{\mathrm{d}}{\mathrm{d} t} \left( \dot{\vec{r}}_i \frac{\partial \vec{r}_i }{\partial q_k} \right) - \vec{r}_i \frac{\mathrm{d}}{\mathrm{d}t} \frac{\partial \vec{r}_i}{\partial q_k}$. $$\begin{align}
&(d), (c) & \Rightarrow \delta W^{(2)} &= - \sum_k \delta q_k \sum_i \left( m_i \left( \frac{\mathrm{d}}{\mathrm{d} t} \underbrace{\left( \vec{v}_i \cdot \frac{\partial \vec{v}_i}{\partial \dot{q}_k}\right)}_{\displaystyle \frac{1}{2} \frac{\partial}{\partial \dot{q}_k} (\vec{v}_i^2)} - \underbrace{\vec{v}_i \cdot \frac{\partial \vec{v}_i}{\partial q_k}}_{\displaystyle \frac{1}{2} \frac{\partial}{\partial q_k} (\vec{v}_i^2)} \right) \right) \\
& & &= - \sum_k \delta q_k \left( \frac{\mathrm{d}}{\mathrm{d} t} \frac{\partial}{\partial \dot{q}_k} - \frac{\partial}{\partial q_k} \right) \underbrace{\sum_i \frac{1}{2} m_i v_i^2}_{\displaystyle T}
\end{align}$$Ainsi on peut exprimer $\delta W$ en fonction des forces généralisées $Q_k$ et de l'énergie cinétique totale $T$ $$\begin{align}
\delta W &= \delta W^{(1)} + \delta W^{(2)} \\
&= \sum_k \delta q_k \left( Q_k - \left( \frac{\mathrm{d}}{\mathrm{d} t} \frac{\partial}{\partial \dot{q}_k} - \frac{\partial}{\partial q_k} \right) T \right) = 0\\
&\Rightarrow \left( \frac{\mathrm{d}}{\mathrm{d} t} \frac{\partial}{\partial \dot{q}_k} - \frac{\partial}{\partial q_k} \right) T = Q_k
\end{align}$$
Ainsi, si on considère le cas conservatif où les forces sont issues du potentiel $V$ $$\begin{align}
Q_k &= - \sum \vec{F}^{\mathrm{ext}}_i \cdot \frac{\partial \vec{r}_i}{\partial q_k} \\
&= - \sum \nabla_i V \cdot \frac{\partial \vec{r}_i}{\partial q_k}\\
&= - \frac{\partial V(\vec{r})}{\partial q_k}
\end{align}$$Donc il en suit $$\begin{align}
\delta W^{(1)} &= - \sum_k \frac{\partial V_i}{\partial q_k} \delta q_k \\
&\Rightarrow \left( \frac{\mathrm{d}}{\mathrm{d} t} \frac{\partial}{\partial \dot{q}_k} - \frac{\partial}{\partial q_k} \right) T = -\frac{\partial V}{\partial q_k} \\
&\Rightarrow \left( \frac{\mathrm{d}}{\mathrm{d} t} \frac{\partial}{\partial \dot{q}_k} - \frac{\partial}{\partial q_k} \right) (T-V) = 0 \\
&\Rightarrow \boxed{\left( \frac{\mathrm{d}}{\mathrm{d} t} \frac{\partial}{\partial \dot{q}_k} - \frac{\partial}{\partial q_k} \right) \mathcal{L} = 0}
\end{align}$$où on a introduit alors le lagrangien $\mathcal{L} = T-V$. L'équation encadrée à la fin est l'équation d'Euler-Lagrange dans sa définition la plus classique.
 
## Théorie 

Ainsi avons-nous dérivé l'équation d'Euler-Lagrange, donc nous redonnons un résumé de ce que nous avons démontré.

> [!Théorème] Equation d'Euler-Lagrange
> Dans un système physique à $N$ points dont on a identifié les [[Coordonnées Généralisées]] $q_k$, les équations du mouvement seront alors données en général par $$\left( \frac{\mathrm{d}}{\mathrm{d} t} \frac{\partial}{\partial \dot{q}_k} - \frac{\partial}{\partial q_k} \right) T = Q_k$$où :
> - $Q_k$ sont les forces généralisées définies comme $\displaystyle \sum_i \vec{F}^{\mathrm{ext}}_i \cdot \frac{\partial \vec{r}_i}{\partial q_k}$
> - $T$ est l'énergie cinétique totale du système $\displaystyle \sum_i \frac{1}{2} m_i v_i^2$
>
> Si on étudie un système meut par des forces conservatives, c'est à dire qui dérivent d'un potentiel $V$. On introduit alors le lagrangien $\mathcal{L} = T-V$ et les équations du mouvement sont données par $$\boxed{\left( \frac{\mathrm{d}}{\mathrm{d} t} \frac{\partial}{\partial \dot{q}_k} - \frac{\partial}{\partial q_k} \right) \mathcal{L} = 0}.$$

C'est une formulation de la mécanique classique qui est équivalente au formalisme newtonien. Cependant, ce formalisme là présente des avantages sur son prédécesseur ; en somme, les équations du mouvements sont plus simples à retrouver une fois les coordonnées généralisées bien définies car il suffit d'appliquer la même équation quelque soit le système.

> [!example]+ Exemple de l'oscillateur harmonique
> On imagine une masse attachée à un ressort de constante de raideur $C$, lui même attaché à un support solide inamovible, et on s'intéresse au mouvement de la masse $m$. On suppose ce système dans le vide, avec comme seule force s'exerçant sur la masse la force de restitution du ressort. A cela on ajoute que la masse ne peut se déplacer que dans une direction colinéaire à l'axe principal du ressort que nous nommerons $x$. L'énergie cinétique de la masse est donc $$T = \frac{m}{2} \dot{x}^2$$et le potentiel harmonique est donnée par la loi de Hooke $$V = \frac{C}{2}x^2.$$
> Ainsi le lagrangien devient  $\mathcal{L} = T - V$ $$\mathcal{L} = \frac{m}{2} \dot{x}^2 - \frac{C}{2} x^2.$$
> En appliquant l'équation d'Euler-Lagrange on trouve$$m \ddot{x} + Cx = 0$$
> > [!démo]- détails
> > On va décomposer l'équation d'Euler-Lagrange et calculer chaque termes un à un. Elle devient explicitement $$\frac{\mathrm{d}}{\mathrm{d} t} \frac{\partial}{\partial \dot{x}} \mathcal{L} - \frac{\partial}{\partial x} \mathcal{L} = 0$$où $q = x$ est la coordonnée généralisée utilisée, et donc terme à terme cela donne$$\begin{align}
\frac{\partial}{\partial \dot{x}} \mathcal{L} &= \frac{\partial}{\partial \dot{x}} \left( \frac{m}{2} \dot{x}^2 - \frac{C}{2} x^2 \right) \\
&= m \dot{x}\\
\frac{\mathrm{d}}{\mathrm{d} t} \left( \frac{\partial}{\partial \dot{x}} \mathcal{L} \right) &= \frac{\mathrm{d}}{\mathrm{d} t} (m \dot{x}) = m \ddot{x} \\
\frac{\partial}{\partial x} \mathcal{L} &= \frac{\partial}{\partial x} \left( \frac{m}{2} \dot{x}^2 - \frac{C}{2} x^2 \right) \\
&= - Cx \\
\Rightarrow m \ddot{x} + Cx &= 0
\end{align}$$


