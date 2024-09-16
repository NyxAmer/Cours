---
tags:
  - Diffusion
---
# A 1 Dimension

## Expression probabiliste

Admettons un particule qui se déplace le long d'une droite avec la probabilité$$\begin{dcases} p & \mathrm{pas \ en \ avant}\\ 1 - p = q & \mathrm{pas \ en \ arrière} .\end{dcases}$$Au bout de $N$ pas, la particule a fait $n$ pas en avant et $N-n$ pas en arrière, donc, en admettant qu'elle fasse un pas de taille constante $a$, sa position est donnée par $$\begin{align}
x &= n a - (N-n)a \\
&= (2n - N)a
\end{align}$$La probabilité que la particule ait fait $n$ pas en avant $\mathbb{P}(n)$ est donnée par une loi binomiale comme suit 

> [!Théorème] Loi binomiale
> La probabilité d'avoir fait $n$ pas en avant avec un probabilité $p$ à chaque étape au bout de $N$ étapes est donnée par
> $$\mathbb{P}(n) = \binom{N}{n} p^n q^{N-n}$$ où : 
> - $\displaystyle \binom{N}{n} = \frac{N !}{n ! (N-n) !}$ est un coefficient binomial
> - $q = 1 - p$ est la probabilité de faire un pas en arrière

 A noter que cette loi vérifie $$\sum_{n=0}^N \mathbb{P}(n) = 1$$car il s'agit du développement du binôme de Newton de $(p + q)^N$, or comme $p + q = 1$  $$\begin{align}
(p+q)^N = \sum_{n=0}^N \binom{N}{n} p^n q^{N-n} \\
\Rightarrow \sum_{n=0}^N \binom{N}{n} p^n q^{N-n} = 1
\end{align}$$
## Propriétés

![[Binomial_distribution_pmf.svg.png]]
Histogrammes de 3 distribution binomiales différentes

Dans notre hypothèse de la particule, on a supposé que chaque pas est de taille constante, ainsi cela implique que ce modèle est discret, ainsi on le décrit à l'aide d'une loi binomiale discrète.

> [!Théorème] Moyenne d'une distribution binomiale
> la moyenne des $n$ notée $\bar{n}$ est donnée par $$\bar{n} = \sum_{n=0}^N n \mathbb{P}(n) = Np$$
> la moyenne quadratique $$\bar{n}^2 = \sum_{n=0}^N n^2 \mathbb{P}(n) = N(N-1)p^2 + Np$$


> [!Théorème] Variance d'une distribution binomiale
> La variance des $n$ notée $\overline{\Delta n^2}$ $$\overline{\Delta n^2} = \overline{(n - \overline{n})^2} = \overline{n^2} - \overline{n}^2 = Npq$$
> L'écart type $\sigma$ $$\sigma = \sqrt{\overline{\Delta n^2}} = \sqrt{Npq}$$

On avait défini le pas comme de taille constante $a$, ainsi la position d'une particule est donnée par $$x = (2n - N)a$$et la position moyenne de toutes les particules $\bar{x}$ est donc donnée par $$\boxed{\bar{x} = (2 \bar{n} - N)a = (2p - 1)Na}$$Cela implique donc que si $p = 0.5$, $\bar{x} = 0$. On comprend en effet que si la particule a autant de chances d'aller d'un côté ou de l'autre, en moyenne elle ne bouge pas. 

On peut s'intéresser à l'écart type de la position des particules, en sachant que $$\begin{align}
x^2 = (4n^2 - 4nN + N^2) a^2 \\
\Rightarrow \overline{\Delta x^2} = \overline{x^2} - \overline{x}^2 = 4Npq a^2
\end{align}$$Ainsi, si $p=0.5$, on trouve que $\overline{\Delta x^2} = Na^2$
## Distribution binomiale pour grands nombres

> [!Théorème] Formule de Stirling
> Pour $n \gg 1$ $$\begin{align}
n! &\approx \sqrt{2 \pi n} \ n^n \ e^{-n} \\
\ln(n !) &\approx n \ln(n) - n + \frac{1}{2} \ln (n) + \frac{1}{2} \ln (2 \pi)  
\end{align}$$

En admettant que $N$ soit suffisamment grand, on pourra chercher à décrire la position de la particule de manière continue avec une loi de probabilité continue. Un distribution binomiale peut être approchée par une distribution normale (ou Gaussienne) lorsque $N$ devient suffisamment grand.

![[De_moivre-laplace.gif]] 

> [!Théorème] Approximation Gaussienne
> Soit $P(n)$ la densité de probabilité d'une loi normale (dite Gaussienne) $$P(n) = \frac{1}{\sigma \sqrt{2 \pi}} \exp \left(  -\frac{1}{2} \left(  \frac{n - \bar{n}}{\sigma} \right)^2 \right)$$où :
> - $\sigma$ est l'écart type, définie comme $\sqrt{Npq}$
> - $\bar{n}$ est la moyenne de $n$, définie comme $\bar{n} = Np$

![[Pasted image 20240916190141.png]]
Tracé de distributions normales avec moyennes $\mu$ et écart type $\sigma$ 

Comme $N$ est très grand, on a $\displaystyle \frac{\delta n}{N} \ll 1 \Rightarrow P(x) \mathrm{d}x = P(n) \delta x$, avec $P(x)$ une densité de probabilité, ainsi $$P(x) = P(n) \frac{\delta n}{\mathrm{d} x} = \frac{1}{2a} P(n)$$donc pour $p = 0.5$, la distribution normale devient explicitement $$P(x) = \frac{1}{a\sqrt{2 \pi N}} \exp \left( - \frac{1}{2N} \left( \frac{x}{a}\right)^2 \right)$$
Si chaque pas prend un temps $\tau$, après $N$ pas, il s'est écoule un temps $t = N \tau$.
Comme $\overline{\Delta x^2} = Na^2 = \frac{a^2}{\tau} t$, on introduit le coefficient $D = \frac{a^2}{2 \tau}$ en $\mathrm{m}^2 \cdot \mathrm{s}^{-1}$ 

# Mouvement Brownien en 3D

En 3D, pour $\vec{r} = (x , y , z)$, la densité de probabilité dans un espace est donnée par $$P(\vec{r}) = P(x) P(y) P(z) = \frac{1}{\Delta x \Delta y \Delta z (2 \pi)^{2/3}} \ \exp \left( - \frac{r^2}{2 \Delta r^2} \right)$$
Par isotropie de l'espace, cela implique $\Delta x^2 = \Delta y^2 = \Delta z^2 = \frac{1}{3} \Delta r^2$ , on pars également du principe que la position moyenne des particules est centrée en $0$, ainsi $\overline{\vec{r}} = \vec{0}$, cela veut donc dire que $\Delta r^2 = \overline{(\vec{r} - \overline{\vec{r}})^2} = \overline{r^2} = N a^2 = 6 Dt$ 

> [!Théorème] Distribution normale 3D
> On donne la distribution de particules dans un espace 3D comme $$P(\vec{r}) = \frac{1}{a} \left( \frac{3}{2 \pi N} \right)^{3/2} \exp \left( \frac{- 3 r^2}{2 N a^2}\right)$$où : 
> - $\vec{r}$ est le vecteur position
> - $r^2 = x^2 + y^2 + z^2$

 