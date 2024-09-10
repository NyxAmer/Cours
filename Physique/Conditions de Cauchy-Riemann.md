---
tags:
  - Maths/Analyse/Complexe
---

> [!théorème] Cauchy-Riemann
> Soit $f : A \subset \mathbb{C} \rightarrow \mathbb{C}$ ; $f(z) = u(x,y) + i v(x,y)$ où $z=x+iy \in A$
> $f$ est dérivable en $z_0 = x_0 + i y_0 \in A$ $\iff$ $u(x,y)$ et $v(x,y)$ sont différentiables en $(x_0, y_0)$ et si elles satisfont les **conditions de Cauchy-Riemann** : $$\begin{dcases}
\frac{\partial u(x,y)}{\partial x} \Bigg\rvert_{x_0, y_0} = \frac{\partial v(x,y)}{\partial y} \Bigg\rvert_{x_0, y_0}\\
\frac{\partial u(x,y)}{\partial y} \Bigg\rvert_{x_0, y_0} = - \frac{\partial v(x,y)}{\partial x} \Bigg\rvert_{x_0, y_0}
\end{dcases}$$

> [!démo]+
> la [[Fonctions Holomorphes#^e5e962|condition de dérivabilité]] en $z_0$ s'écrit : $$\begin{align}
\lim_{z \rightarrow z_0 \equiv |z - z_0| \rightarrow 0} \frac{f(z) - f(z_0)}{z - z_0} = \lim_{u \rightarrow 0 \equiv |u| \rightarrow 0} \frac{f(z_0 + u) - f(z_0)}{u} = f'(z_0) \in \mathbb{C}
\end{align}$$où $u=z-z_0 = s+ it$. 
> La limite doit être réalisée quelque soit la façon sont $z$ tend vers $z_0$, c'est à dire dont $u$ tend vers $0$.
> - Si $u$ tend vers $0$ le long de l'axe réel ($t=0$), la condition de dérivabilité donne alors :$$\begin{align}
f'(z_0) &= \lim_{s \rightarrow 0} \left( \frac{u(x_0 + s, y_0) - u(x_0, y_0)}{s} + i\frac{v(x_0 +s, y_0) - v(x_0, y_0)}{s}\right) \\
&= \frac{\partial u}{\partial x} \Bigg\rvert_{x_0, y_0} + i \frac{\partial v}{\partial x} \Bigg\rvert_{x_0, y_0}
\end{align}$$
> - Si $u$ tend vers $0$ le long de l'axe imaginaire ($s=0$), la condition de dérivabilité donne alors:$$\begin{align}
f'(z_0) &= \lim_{t \rightarrow 0} \left( \frac{u(x_0, y_0 + t) - u(x_0, y_0)}{it} + i\frac{v(x_0, y_0 + t) - v(x_0, y_0)}{it}\right) \\
&= \frac{\partial v}{\partial y} \Bigg\rvert_{x_0, y_0} - i \frac{\partial u}{\partial y} \Bigg\rvert_{x_0, y_0}
\end{align}$$
>
> Ces deux expressions étant égales, elles conduisent aux **conditions de Cauchy-Riemann**.


