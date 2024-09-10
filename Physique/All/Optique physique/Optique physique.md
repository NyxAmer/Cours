# 1. Généralités

## 1.1. Équation d'onde, onde plane, onde sphérique 

Les équations de Maxwell permettent d'arriver à des équations d'ondes pour le champ électromagnétique, on ne s'intéressera qu'au champ électrique pour les besoins de l'optique$$\nabla^{2} \vec{E} = \frac{1}{c^{2}}\frac{\partial^2 \vec{E}}{\partial t^2}$$On va ignorer l'aspect vectoriel du champ électrique, on écrira alors $u(\vec{r},t)$ pour la quantité qui représente l'amplitude du champ.

### Onde plane monochromatique

La solution de l'équation d'onde, donnant une onde se propageant en direction de $\vec{k}$ $$u(\vec{r},t) = u_{0}\cos (\omega t - \vec{k} \cdot \vec{r} - \varphi_0)$$On peut vérifier que cela satisfait l'équation d'onde.$$\begin{align}
\nabla^{2} u &= \nabla^{2} u_{0}\cos (\omega t - \vec{k} \cdot \vec{r} - \varphi_{0})\\
&= - u_{0} \cos (\omega t - \vec{k} \cdot \vec{r} - \varphi_{0}) (k_{x}^{2} + k_{y}^{2} + k_{z}^{2}) \\
&= -u_{0} k^{2} \cos(\omega t - \vec{k}\cdot \vec{r} - \varphi_{0)}\\
&= -k^{2} u \\
\frac{1}{c^{2}}\frac{\partial^{2} u}{\partial t^{2}} &= - \omega^{2} u_{0} \cos (\omega t - \vec{k} \cdot \vec{r} - \varphi_{0})\frac{1}{c^{2}}\\
&= \frac{- \omega^{2}}{c^{2}} u \\
\Rightarrow \frac{- \omega^{2}}{c^{2}} u &= -k^{2} u \Rightarrow k = \frac{\omega}{c}
\end{align}$$On constate alors que pour que l'équation d'onde soit satisfaite, l'onde monochromatique doit satisfaire la relation de dispersion $c = \frac{\omega}{k}$ ^1

On notera que la fonction $u(\vec{r}, t)$ est périodique dans l'espace, mais aussi dans le temps

> [!NOTE] Écriture complexe
> Bien souvent, afin de simplifier la notation et les calculs, la fonction exponentielle complexe sera utiliser pour représenter un phénomène périodique, ainsi nous écrirons les ondes monochromatiques ainsi $$u(\vec{r},t) = \mathrm{Re} \left(u_{0} e^{i(\omega t - \vec{k} \cdot \vec{r} - \varphi_0)}\right)$$
> On ne s'intéresse en réalité qu'à la partie réelle de l'écriture complexe, même si cela est souvent omis des notations. On pourra également noter l'amplitude complexe $u_0$ comme comprenant déjà l'information de phase encodée par la variable $\varphi_0$ à l'intérieur de l'exponentielle complexe, ainsi nous noterons ladite amplitude complexe $$\begin{align}
> \bar{u}_{0} &= u_{0} e^{-i \varphi_{0}}\\
> \Rightarrow u(\vec{r}, t) &= \mathrm{Re} \left( \bar{u}_{0} e^{i (\omega t - \vec{k} \cdot \vec{r})} \right)
> \end{align}$$ Par la suite, tout sera noté avec l'écriture complexe, la barre au dessus des variables ne sera pas forcément renseignée.

On note que la phase dans le cosinus ou dans l'exponentielle est la même pour tous les points $\vec{r}$ satisfaisant la relation $\vec{k} \cdot \vec{r} = cte$ qui définit les plans perpendiculaires à $\vec{k}$

### Onde sphérique monochromatique

Une autre solution de l'équation d'onde est donnée par une onde sphérique monochromatique. Dans sa forme complexe, une onde sphérique s'éloignant d'une source ponctuelle à l'origine, s'écrit $$u(r,t) = \frac{u_0}{r} e^{-i(kr - \omega t)}$$où :
- $k = \frac{2 \pi}{\lambda}$
- $r=|\vec{r}|$ 
La phase d'une telle onde est toujours la même sur une surface avec $r$ constant, c'est à dire sur chaque sphères centrées à l'origine.

# 2.Interférence
 
## 2.1. Superposition de deux ondes monochromatiques

Nous nous positionnons à une endroit $\vec{r}$ donné et considérons la superposition de deux ondes monochromatiques de fréquence $\omega_1$ et $\omega_2$. En négligeant dans ce cas la dépendance spatiale, on peut écrire $$\begin{align}
u_1(t) &= u_{1,0} e^{i \omega_1 t},& u_2(t) &= u_{2,0} e^{i \omega_2 t}& \\
u_{1,0} &= |u_{1,0}| e^{i \varphi_1},& u_{2,0} &= |u_{2,0}| e^{i \varphi_2}&
\end{align}$$L'onde qui résulte de la superposition de ces deux ondes est la somme des deux champs$$u(t) = u_1(t) + u_2(t)$$L'intensité de la lumière est proportionnelle au module de $u(t)$ au carré$$\begin{align}
|u(t)|^2 &= (u_1(t) + u_2(t))(u_1(t) + u_2(t))^*\\
&= |u_{1,0}|^2 + |u_{2,0}|^2 + 2 \mathrm{Re}(u_1(t) u^*_2 (t)) 
\end{align}$$Les deux premiers termes sont associés aux intensité $I_1$ et $I_2$ des deux ondes prises individuellement. Le dernier terme donne$$\begin{align}
2 \mathrm{Re} (u_1 u^*_2) &= 2 \mathrm{Re} \left(|u_{1,0}| |u_{2,0}| e^{i(\phi_1 - \phi_2)} e^{i(\omega_1 - \omega_2)t}\right)\\
&= 2 |u_{1,0}| |u_{2,0}| \mathrm{Re}\left(e^{i((\omega_1 - \omega_2)t - \Delta \varphi)}\right)
\end{align}$$Le cas le plus intéressant est celui où les ondes ont la même fréquence (ondes isochores). On a alors $$|u(t)|^2 = |u_{1,0}|^2 + |u_{2,0}|^2 + 2 |u_{1,0}| |u_{2,0}| \mathrm{Re}\left(e^{ - i\Delta \varphi}\right)$$En terme d'intensité cela peut s'écrire de la façon suivante$$I = I_1 + I_2 + 2 \sqrt{I_1 I_2} \cos(\Delta \varphi)$$Ceci représente une fonction périodique par rapport à la différence de phase $\Delta \varphi$ entre les deux ondes. Le troisième terme, qui donne l'écart de l'intensité à $I_1 + I_2$, est le terme d'interférence entre les deux ondes.
La valeur maximale de $I$ est trouvée par $\Delta \varphi = n2\pi, n \in \mathbb{Z}$ et vaut $$I_\mathrm{max} = \left( \sqrt{I_1} + \sqrt{I_2} \right)^2$$La valeur minimale est trouvée par $\Delta \varphi = (2n +1)\pi, n \in \mathbb{Z}$ et vaut$$I_\mathrm{min} = \left( \sqrt{I_1} - \sqrt{I_2} \right)^2$$
Expérimentalement, on caractérise le contraste des franges d'interférence par le facteur de visibilité $$V \triangleq \frac{I_\mathrm{max} - I_\mathrm{min}}{I_\mathrm{max} + I_\mathrm{min}} = \frac{2 \sqrt{I_1 I_2}}{I_1 + I_2} \leq 1$$le contraste est maximal quand $I_1 = I_2$, on a $V=1$

## 2.2. Superposition de deux ondes planes monochromatiques se propageant sous différents angles

Nous supposons que les deux ondes planes ont la même fréquence $\omega_1 = \omega_2 = \omega$ et que leurs directions de propagations sont $\vec{k}_1$ et $\vec{k}_2$ respectivement, avec $|\vec{k}_1| = |\vec{K}_2| = k$
Nous supposons aussi que leurs amplitudes et intensités sont les mêmes. Les deux ondes sont donc$$\begin{align}
u_1(\vec{r},t) = |u_0| e^{i \varphi_1} e^{i(\omega t - \vec{k}_1 \cdot \vec{r})} \\
u_2(\vec{r},t) = |u_0| e^{i \varphi_2} e^{i(\omega t - \vec{k}_2 \cdot \vec{r})}
\end{align}$$Leur superposition est $u = u_1 + u_2$ et l'intensité est $$\begin{align}
I &= u u^* \\
&= |u_0|^2 e^{i \omega t}\left( e^{-i \vec{k}_1 \cdot \vec{r}} e^{i \varphi_1} + e^{-i \vec{k}_2 \cdot \vec{r}} e^{i \varphi_2}\right) e^{-i \omega t}\left( e^{i \vec{k}_1 \cdot \vec{r}} e^{-i \varphi_1} + e^{i \vec{k}_2 \cdot \vec{r}} e^{-i \varphi_2}\right) \\
&= |u_0|^2 \left( e^{-i \vec{k}_1 \cdot \vec{r}} e^{i \varphi_1} + e^{-i \vec{k}_2 \cdot \vec{r}} e^{i \varphi_2}\right) \left( e^{i \vec{k}_1 \cdot \vec{r}} e^{-i \varphi_1} + e^{i \vec{k}_2 \cdot \vec{r}} e^{-i \varphi_2}\right) \\
&= |u_0|^2 \left( 2 + e^{i[(\vec{k}_1 - \vec{k}_2) \cdot \vec{r} - \Delta \varphi]} + e^{-i[(\vec{k}_1 - \vec{k}_2) \cdot \vec{r} - \Delta \varphi]}\right) \\
&= 2 I_0 \left( 1 + \cos\left(\Delta \vec{k} \cdot \vec{r} - \Delta \varphi \right)\right) \\
&= 4 I_0 \cos^2\left(\frac{1}{2} \left(\Delta \vec{k} \cdot \vec{r} - \Delta \varphi \right)\right)
\end{align}$$Cette expression montre que l'intensité est modulée spatialement de façon périodique, on a alors des franges d'interférence.
Le vecteur $\Delta \vec{k}$ est le vecteur d'interférence, ou vecteur de réseau.
Les points $\vec{r}$ sur un plan perpendiculaire au vecteur $\Delta \vec{k}$ possèdent tous là même intensité.
La quantité $\Delta \varphi$ est la différence de phase à l'origine.
La distance entre deux franges claires, ou sombres, et appelée interfrange ou pas du réseau d'interférence ou période du réseau d'interférence. Cette période est trouvée par la condition que la phase $\Delta \vec{k} \cdot \vec{r}$ change d'une valeur de $2 \pi$ entre deux maxima ou deux minima, c'est à dire quand$\Delta \vec{k}$ est parallèle à la direction $x$ $$\begin{align}
\Delta \vec{k} \cdot \vec{r} = x\frac{4 \pi}{\lambda} \sin \alpha = 2 \pi \\
\Rightarrow x = \frac{\lambda}{2 \sin \alpha} \triangleq \Lambda
\end{align}$$où : 
- $\alpha$ est le demi angle entre $\vec{k}_1$ et $\vec{k}_2$
- $\Lambda$ est l'interfrange
Plus grand est le demi angle $\alpha$ entre les deux ondes planes plus courte sera l'interfrange $\Lambda$. Notons alors que quand $\Delta \vec{k} \parallel x$ on peut écrire $I$ $$I = 4 I_0 \cos^2 \left( \frac{\pi x}{\Lambda} - \frac{\Delta \varphi}{2} \right)$$

> [!info] Remarque
> La superposition que nous avons utilisé n'est possible que parce que l'équation d'onde est une équation linéaire. Elle ne présente en effet que la première puissance du champ électrique (pas de terme quadratiques, cubiques ou autres). Pour une telle équation, le principe de superposition est satisfait. Si $u_1$ et $u_2$ sont solutions, alors toute combinaisons linéaires de ces solutions l'est aussi.

## 2.3. Trous et fentes de Young

L'expérience de Young (Thomas Young, 1773-1825) a mis le mot final au débat de l'époque sur l'existence ou non d'une nature ondulatoire de la lumière. L'expérience de Young date de 1803 et peut être représentée schématiquement de la façon suivante ![[Pasted image 20240406172204.png|365]] ![[Pasted image 20240406200056.png|320]]
Il est évident que la compréhension complète du phénomène nécessite de tenir compte de la diffraction en plus de l'interférence. Si on était dans une approche d'optique géométrique, alors la lumière quitterait l'ouverture primaire sans pouvoir éclairer les ouvertures du second plan, et l'on s'attendrait tout au plus à voir apparaître deux bandes éclairées sur l'écran. Nous éviterons de tenir compte de la diffraction pour le moment, qui ne ferait que moduler l'enveloppe de la solution que nous trouverons. On considèrera que les onde qui quittent $S_1$ et $S_2$ sont assimilable à des ondes cylindriques. On verra plus tard que cela revient à appliquer le principe de Huygens-Fresnel à une très petite ouverture, donnant alors une enveloppe suffisamment large pour qu'on puisse l'ignorer pour les points proches de l'axe optique. Le problème est donc un problème d'interférences d'ondes cylindriques (sphériques dans le plan de coupe passant par l'axe optique). Comme les ondes provenant de $S_1$ et de $S_1$ proviennent de la même ouverture en amont $S$ supposée à équidistance de $S_1$ et $S_2$, alors ont pourra dire qu'elles ont la même phase.
![[Pasted image 20240406195845.png]]
On peut dire que les deux sources $S_1$ et $S_2$ sont suffisamment loin de l'écran pour que l'on puisse noter leurs amplitudes $\frac{u_0}{s}$. On ne fera pas cette approximation pour la phase qui est nécessaire afin d'expliquer l'interférence. On peut donc noter les amplitudes des champs comme suit$$\begin{align}
u_1(r,t) &= \frac{u_0}{s} e^{-i \omega t} e^{ik r_1} \\
u_2(r,t) &= \frac{u_0}{s} e^{-i \omega t} e^{ik r_2} .
\end{align}$$Donc leur superposition devient$$\begin{align}
u &= u_1 + u_2 \\
u &=  \frac{u_0}{s} e^{-i \omega t} \left( e^{ikr_1} + e^{ikr_2} \right).
\end{align}$$Ainsi l'intensité du champ donne$$\begin{align}
I &= u u^* \\
&= \left(\frac{u_0}{s} e^{-i \omega t} \left( e^{ikr_1} + e^{ikr_2} \right)\right) \left(\frac{u_0}{s} e^{i \omega t} \left( e^{-ikr_1} + e^{-ikr_2} \right)\right) \\
&= \frac{u_0^2}{s^2} \left( e^{ikr_1} + e^{ikr_2} \right) \left( e^{-ikr_1} + e^{-ikr_2} \right) \\
&= \frac{u_0^2}{s^2} \left( 2+ e^{ik(r_1 - r_2)} + e^{-ik(r_1 - r_2)} \right) \\
&= 2 \frac{u_0^2}{s^2} (1+ \cos(k(r_1 - r_2)))\\
&= 4 \frac{u_0^2}{s^2} \cos^2\left(\frac{k}{2}(r_1 - r_2)\right) \\
&= 4 \frac{u_0^2}{s^2} \cos^2\left(\frac{\pi}{\lambda}(r_1 - r_2)\right) \\
I &= 4 \frac{u_0^2}{s^2} \cos^2\left(\frac{\pi}{\lambda} \Delta r\right).
\end{align}$$De plus, on constate que l'on peut trouver $\Delta r$ géométriquement grâce à l'approximation des petits angles. Sur le dessin, $\Delta r \equiv S_1 B$. Dans le triangle rectangle $\triangle S_1 S_2 B$, rectangle en $B$ on a$$\sin \theta_m = \frac{\Delta r}{a}$$or grâce à l'approximation des petits angles ($\sin \theta \simeq \theta$)on obtient alors $$\begin{align}
\Rightarrow \theta_m &= \frac{\Delta r}{a} \\
\Rightarrow \Delta r &= \theta_m a.
\end{align}$$Or on a également dans le grand triangle rectangle $\triangle S_2 O P \simeq \triangle S_1 O P$ (on peut faire cette approximation grâce aux petits angles, car on considère $a \ll s$) la relation suivante $$\begin{align}
\tan \theta_m &= \frac{y_m}{s} \\
\Rightarrow \theta_m &\simeq \frac{y_m}{s} \\
\Rightarrow \Delta r &= \frac{y_m}{s} a \\
I &= 4 \frac{u_0^2}{s^2} \cos^2\left(\frac{\pi}{\lambda} \frac{y_m}{s} a\right)
\end{align}$$donc pour avoir un maximum de l'intensité, il faut imposer une condition sur l'argument du cosinus carré $$\begin{align}
\cos^2 \theta = 1 \Rightarrow \theta &= m \pi,\ m \in \mathbb{Z} \\
\Rightarrow \frac{\pi}{\lambda} \frac{y_m}{s} a &= m \pi \\
\Rightarrow \frac{y_m}{\lambda s} a &= m \\
\Rightarrow y_m &= m \frac{\lambda s}{a}
\end{align}$$et enfin, afin de déterminer l'interfrange $\Lambda = \Delta y$, il faut examiner deux maxima adjacents. Pour se faire on peut utiliser deux entiers consécutifs et faire la différence $$\begin{align}
\Lambda &= \Delta y = y_{m+1} - y_m\\
&= (m+1) \frac{\lambda s}{a} - m \frac{\lambda s}{a}\\
\Lambda &= \frac{\lambda s}{a}
\end{align}$$
 
# 3. Diffraction

Le phénomène de diffraction consiste en "l'éparpillement" de la lumière quand une onde est matériellement limitée, par exemple lorsqu'elle doit passer par un diaphragme de petite dimension. Aussi bien que le phénomène d'interférence, la diffraction est manifestation de la nature ondulatoire de la lumière. Elle marque la limite de l'optique géométrique.

> [!NOTE] Principe d'Huygens-Fresnel
> 
> - **Huygens :** Chaque élément (point) d'un front d'onde peut être regardé comme étant une source secondaire qui émet une ondelette sphérique. La position du front d'onde à un temps $\Delta t$ plus tard correspond à l'enveloppe de toutes les ondelettes.
> 
> - **Contribution de Fresnel :** Les ondelettes secondaire donnent lieu à une interférence réciproque. Il en suit que, en appliquant le principe de superposition de l'optique linéaire, l'amplitude complexe de l'onde reçue dans un point $P$ distant est la somme des amplitudes de toutes les ondelettes élémentaires parvenant en $P$ depuis les différents points de la source secondaire
> ![[Pasted image 20240328160427.png]]

## 3.1. Diffraction à une fente

Nous traitons tout d'abord la diffraction à une fente de manière simple es s'appuyant sur le principe de Huygens-Fresnel. Le même problème peut être traité de façon plus générale dans le cadre de l'optique de fourrier qui ne sera traitée que partiellement dans ce cours.
![[Pasted image 20240328160751.png]]
On ne va s'intéresser qu'à la figure de diffraction (figure d'interférence) à une distance très grande à la droite de la fente. Ceci est le régime de *diffraction de Fraunhofer* ou du *champ lointain* (far field), en opposition à la *diffraction de Fresnel* (*champ proche*, near field)

La lumière en direction de l'angle $\theta$ parcours une distance légèrement différente si son ondelette prend origine en $y=0$ ou dans un point $y \neq 0$ $$\rho (y) - \rho(0) = -y \sin \theta$$La différence de phase à l'écran entre la lumière 'arrivant en direction $\theta$ à partie des points $y=y$ et $y=0$ est donc $$\frac{2 \pi}{\lambda} (\rho(z)- \rho(0)) = -\frac{2\pi}{\lambda} y \sin \theta $$Donc l'onde arrivant à l'écran sous l'angle $\theta$ à partir du segment en position $y$ sera $$u(y) = u(0) e^{-iky\sin \theta} = u(0) e^{-i \beta y}$$où $u(0)$ est l'amplitude complexe de l'onde arrivant au centre de la fente. En intégrant sur la largeur de la fente, on obtient la superposition de toues les ondelettes venant de la fente$$\begin{align}
u &= \int_{-s/2}^{s/2} u(0) e^{-i \beta y}\ \mathrm{d}y = u(0) \int_{-s/2}^{s/2} e^{-i \beta y}\ \mathrm{d}y \\
&= u(0) \frac{-1}{i \beta} \left(e^{-i \beta \frac{s}{2}} - e^{i \beta \frac{s}{2}} \right) \\
&= u(0) \frac{1}{i \beta} 2i \frac{1}{2i} \left(e^{i \beta \frac{s}{2}} - e^{-i \beta \frac{s}{2}} \right) \\
&= u(0) \frac{2}{\beta} \frac{s}{s} \sin\left(\frac{\beta s}{2}\right) \\
u(\theta) &= u(0) \left(s \frac{\sin \left( \frac{ks}{2} \sin \theta \right)}{\frac{ks}{2} \sin \theta} \right)
	\end{align}$$Pour l'intensité sous l'angle $\theta$, on a avec $I \propto u u^{*} = |u(\theta)|^2$ $$\begin{align}
I(\theta) \propto |u|^{2}= |u(0)|^{2}s^{2}\frac{\sin^2 \left( \frac{ks}{2} \sin \theta \right)}{\left(\frac{ks}{2} \sin \theta\right)^2} \\
\Rightarrow \boxed{I(\theta) = I_{0}\ \mathrm{sinc}^{2} \left(\frac{ks}{2} \sin \theta\right)}
\end{align}$$Avec $\displaystyle x = \frac{ks \sin \theta}{2}$, on a donc $\displaystyle \boxed{I(\theta) = I_{0} \frac{\sin^{2} x}{x^2}}$ 
![[Pasted image 20240328155949.png]]
Il est utile de représenter la même chose aussi en fonction de de l'angle $\theta$ directement (avec $\theta = \arcsin \frac{\lambda x}{\pi s}$)
![[Pasted image 20240328155855.png]]
$\rightarrow$ plus petite est la fente, plus étendue sera la figure de diffraction

## 3.2. Diffraction par un réseau

De la même façon que précédemment pour la diffraction à une fente unique, on peut établir une relation pour l'intensité diffractée par un réseau composé d'une série périodique de fentes. Considérons le réseau suivant composé de fentes de largeur $s$ espacées périodiquement d'une distance $\Lambda$. La largeur de la zone illuminée par une onde plane est $L$.

### Condition pour interférence constructive

Considérons la lumière provenant de deux fentes voisines. Nous voulons déterminer l'angle $\theta$ pour lequel on observe une interférence constructive pour une lumière qui tombe sur le réseau sous une angle $\theta_0$  

> [!théorème] Relation fondamentale des réseaux
> Différence de chemin entre les deux ondes provenant de ces 2 fentes $$\Lambda \sin \theta - \Lambda \sin \theta_{0} = \Lambda (\sin \theta - \sin \theta_0)$$ Ceci doit être égale à une multiple de la longueur d'onde de la lumière $\lambda$.$$\Lambda (\sin \theta - \sin \theta_{0})= m \lambda$$ ![[Pasted image 20240328161833.png|210]] ![[Pasted image 20240328161846.png|220]] ![[Pasted image 20240328161904.png|210]] 

### Relation fondamentale en forme vectorielle

On peut écrire la relation précédente aussi sous la forme $$\begin{align}
\frac{1}{\lambda} \sin \theta - \frac{1}{\lambda} \sin \theta_{0} &= \frac{m}{\Lambda} \\
\frac{2 \pi}{\lambda} \sin \theta - \frac{2 \pi}{\lambda} \sin \theta_{0} &= \frac{2\pi}{\Lambda} m
\end{align}$$ Définissons les vecteurs suivants 
- **vecteur du réseau** $\displaystyle \vec{K} = \frac{2 \pi}{\Lambda} \hat{y}$ 
- **vecteur d'onde incident** $\displaystyle \vec{k}_{0} = \frac{2 \pi}{\lambda} \begin{pmatrix}0 \\ \sin \theta_{0}\\ \cos \theta_0\end{pmatrix}$
- **vecteur d'onde diffracté** $\displaystyle \vec{k} = \frac{2 \pi}{\lambda} \begin{pmatrix}0 \\ \sin \theta\\ \cos \theta\end{pmatrix}$
 
donc la formule précédente devient $$k_{y} - k_{0,y} = m K_{y} = \Delta k_{y}$$Plus généralement $$\vec{k} \cdot \vec{K} - \vec{k}_{0}\cdot \vec{K} = m |\vec{K}|$$Notons que pour $m=0$, on a $\vec{k}_{0}= \vec{k}$, cet ordre correspond à la transmission directe
Nous venons de considérer un *réseau de transmission*, cependant la pluspart des réseaux sont utilisés en réflexion, nous allons donc considérer les *réseaux de réflexion*. On peut montrer que pour la réflexion, la relation fondamentale des réseaux devient $$\Lambda (\sin \theta + \sin \theta_{0)}= m \lambda$$L'ordre 0 correspond alors à la réflexion spéculaire. Par contre on peut aussi montrer que la forme vectorielle de la relation fondamentale des réseaux maintient la forme que nous avons déterminé pour une réseau de transmission. On a donc toujours $$\left(\vec{k} - \vec{k}_{0} \right) \cdot \vec{K} = m |\vec{K}|$$Nous revenons maintenant dans le cas du réseau de diffraction dans le but de calculer l'amplitude de l'onde diffractée.

### Amplitude de l'onde diffractée

Rappelons tout d'abord l'amplitude diffractée par une seule fente de largeur $s$ $$u(\theta) = u(0) s \frac{\sin \left( \frac{\pi}{\lambda} s\sin \theta \right)}{\frac{\pi}{\lambda} s\sin \theta} $$Ceci avait été trouvé dans le cas où l'angle d'incidence $\theta_0$ était nul, dans le cas $\theta_{0}\neq 0$, cela se transforme en $$u(\theta) = u(0) s \frac{\sin \left( \frac{\pi}{\lambda} s(\sin \theta - \sin \theta_0)\right)}{\frac{\pi}{\lambda} s(\sin \theta - \sin \theta_0)} $$Si maintenant on considère l'ensemble des fentes du réseau, il faut sommer sur les amplitudes pour toutes les fentes différentes. Les amplitudes différent par une terme de phase correspondant à la différence de chemin parcouru$$\Delta \phi_{m} = \frac{2 \pi}{\lambda} \Lambda (\sin \theta - \sin \theta_{0})m$$Ce déphasage est calculé par rapport à une fente centrale parmi $N$ fentes où l'indice $m$ va de $-n$ à $+n$ ($N= 2n+1$)
 On obtient alors $$\begin{align}
u_{\mathrm{tot}}(\theta) &= u(0) s \frac{\sin \left( \frac{\pi}{\lambda} s(\sin \theta - \sin \theta_0)\right)}{\frac{\pi}{\lambda} s(\sin \theta - \sin \theta_{0})} \sum_{m = -n}^{n}  e^{i \Delta \phi_{m}}\\
&= u(\theta) \sum_{m = -n}^{n}  e^{i \frac{2 \pi}{\lambda} \Lambda (\sin \theta - \sin \theta_{0})m} \\
&= u(\theta) \sum_{m = -n}^{n}  e^{i \Delta \phi m} \\
u_{\mathrm{tot}}(\theta) &= u(\theta) e^{-i \Delta \phi n} \frac{1- e^{i \Delta \phi N}}{1 - e^{i \Delta \phi}} \\
&= u(\theta) \frac{e^{-i \Delta \phi \frac{N}{2}}}{e^{-i \frac{\Delta \phi}{2}}} \frac{1- e^{i \Delta \phi N}}{1 - e^{i \Delta \phi}} \\
&= u(\theta) \frac{e^{-i \frac{\Delta \phi N}{2}} - e^{i \frac{\Delta \phi N}{2}}}{e^{-i \frac{\Delta \phi }{2}} - e^{i \frac{\Delta \phi }{2}}} \\
u_{\mathrm{tot}}(\theta) &= u(\theta) \frac{\sin\left( \frac{N \Delta \phi}{2} \right)}{\sin\left( \frac{\Delta \phi}{2} \right)}
\end{align}$$En réintroduisant l'expression pour $u(\theta)$ et pour $\Delta \phi$ on obtient $$u_{\mathrm{tot}}(\theta) = u(0) s N \frac{\sin \left( \frac{\pi}{\lambda} s(\sin \theta - \sin \theta_0)\right)}{\frac{\pi}{\lambda} s(\sin \theta - \sin \theta_0)}  \frac{\sin\left( \frac{N \pi \Lambda}{\lambda}(\sin \theta - \sin \theta_{0}) \right)}{N \sin\left( \frac{ \pi \Lambda}{\lambda}(\sin \theta - \sin \theta_{0}) \right)}$$Avec $\Delta k_{y}= k_{y} - k_{0,y} = \frac{2 \pi}{\lambda} (\sin \theta - \sin \theta_0)$, on obtient $$u_{\mathrm{tot}}(\theta) = u(0) s N \frac{\sin \left( \frac{\Delta k_{y} }{2}s \right)}{\frac{\Delta k_{y} }{2}s}  \frac{\sin\left( \frac{\Delta k_{y} }{2} N \Lambda\right)}{N \sin\left( \frac{\Delta k_{y} }{2} \Lambda \right)}$$Pour l'intensité ($I(\theta) \propto u_{\mathrm{tot}}(\theta) u^{*}_{\mathrm{tot}}(\theta)$) $$\boxed{I(\theta) = u^{2}(0)s^{2}N^{2} \frac{\sin^2 \left( \frac{\Delta k_{y} }{2}s \right)}{\left(\frac{\Delta k_{y} }{2}s\right)^2}  \frac{\sin^2\left( \frac{\Delta k_{y} }{2} N \Lambda\right)}{N^2 \sin^2\left( \frac{\Delta k_{y} }{2} \Lambda \right)}}$$Donc l'expression de $I(\theta)$ contient le terme en $\sin^2\left(\frac{\Delta k_y}{2}s\right)$ qui caractérise l'intensité de diffraction à une fente unique de largeur $s$. Ceci est multiplié par la *fonction de réseau*$$\mathrm{R}\left(\frac{\Delta k_{y} \Lambda}{2}\right) = \frac{\sin^2\left( \frac{\Delta k_{y} }{2} N \Lambda\right)}{N^2 \sin^2\left( \frac{\Delta k_{y} }{2} \Lambda \right)}$$Cette fonction est périodique et paire![[Pasted image 20240328173222.png]]
 La fonction de réseau est périodique et a ses maxima à$$\frac{\Delta k_{y} \Lambda}{2} = m \pi,\ m \in \mathbb{Z}$$En introduisant dans cette condition l'expression pour $\Delta k_y$ on retrouve bien la relation fondamentale des réseaux.
 La figure de diffraction sera donc donnée par des piques périodiques avec l'enveloppe de leur intensité correspondant à la figure de diffraction à une fente élémentaire du réseau
 ![[Pasted image 20240328173707.png]]![[Pasted image 20240328173715.png]]![[Pasted image 20240328173724.png]] 
 On peut montrer que si $N$ est grand, la fonction $\mathrm{R}\left(\frac{\Delta k_{y} \Lambda}{2}\right)$ prend, dans le voisinage d'un maximum, la forme d'un sinus cardinal carré. En utilisant la "larguer du faisceau incident" $L = N \Lambda$, on peut alors écrire pour le voisinage de $\Delta k_{y}= 0$ $$\mathrm{R} \simeq \frac{\sin^{2}\left(\frac{\Delta k_{y}L}{2}\right)}{\left(\frac{\Delta k_{y}L}{2}\right)^2}$$Cela montre que la répartition d'intensité dans tout le voisinage des maxima correspond à cella de la figure de diffraction d'une fente de largeur égale à la zone illuminée $L$ du réseau. Pour la fonction sinus cardinal carré, la Largeur totale à mi hauteur (FWHM) est $$\mathrm{FWHM} = \Delta(\Delta k_y)_{1/2} \simeq \frac{2 \pi 0,89}{L} \propto \frac{1}{L}$$Donc plus large est la zone illuminée (plus de fentes du réseau retenus), plus précis sera l'angle de diffraction pour les ordres de diffraction du réseau.
 Les réseaux de diffraction sont utilisés dans les spectromètres pour séparer les composantes spectrales (distinguer les longueur d'onde). Il est donc important d'illuminer une zone large du réseau pour obtenir une bonne résolution spectrale. Similairement, l'utilisation d'un pas $\Lambda$ petit sert aussi à améliorer la résolution

## 3.3. Principe de Babinet

Considérons le cas d'une ouverture et de son complément (obstacle opaque avec la même forme de l'ouverture). Appelons $S$ l'extension du plan de l'ouverture et $S_1$ la surface de l'ouverture ainsi que de son complément. Soit $a_1(P)$ le champ optique complexe reçu dans le point $P$ de l'écran lointain si l'ouverture $S_1$ est présente.
Soit $a_2(P)$ le champ optique reçu en $P$ si l'obstacle est présent.
Soit $a(P)$ le champ optique reçu en $P$ si ni l'obstacle ni l'ouverture ne sont présent.
Puisque les champs $a_1$ et $a_2$ sont obtenus par la même intégrale mais sur des domaines complémentaires, il suit tout de suite que $$a_{1}(P)+ a_{2}(P) = a(P)$$
### Conséquences
- si le point $P$ se trouve dans une zone qui n'est pas illuminée en absence de tout obstacle, alors le champ produit par l'ouverture et son complément vont être identique mais en opposition de phase.
- si $a_{1}(P) =0 \Rightarrow a_{2}(P) = a(P)$ C'est à dire que dans ce cas, l'intensité en $P$ en présence de l'obstacle est ka même que pour le champ libre.
On peut donc en conclure qu'à l'exception de la zone illuminée par le champ libre, la figure de diffraction d'une ouverture et de son complément sont identiques.