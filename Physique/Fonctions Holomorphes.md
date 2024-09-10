---
tags:
  - Maths/Analyse/Complexe
aliases:
  - FH
---
Soit $f : A \subset \mathbb{C} \rightarrow \mathbb{C}$ une fonction définie sur une partie $A$ de $\mathbb{C}$. On note $f : z = x+iy \mapsto f(z) = u(x,y) + i v(x,y)$.

> [!théorème] Dérivabilité :
> $f: A \subset \mathbb{C} \rightarrow \mathbb{C}$ est dite **dérivable** en $z_0 \in A$ si et seulement si il existe $f'(z_0) \in \mathbb{C}$ tel que :$$\lim_{z \rightarrow z_0} \frac{f(z) - f(z_0)}{z - z_0} = f'(z_0)$$

^e5e962

ou de manière équivalente : 

> [!théorème]
> $f$ est dérivable en $z_0 \in A$ ssi $\exists \ \varepsilon(z)$, définie sur $A$, et $f'(z_0) \in \mathbb{C}$ tels que, $\forall \ z \in A$ :  $$\begin{align}
f(z) = f(z_0) + (z-z_0) f'(z-0) + \varepsilon(z) (z-z_0)
\end{align}$$ avec $\displaystyle \lim_{z \rightarrow z_0} \varepsilon(z) = 0$.

# Définition

$f : A \subset \mathbb{C} \rightarrow \mathbb{C}$ est **[[Fonctions Holomorphes|holomorphe]]** sur l'ouvert $U \subset A$ si elle est dérivable en tout point de $U$ et $f'$ est la **fonction dérivée** de $f$ sur $U$. On dira que $f$ est une fonction holomorphe sur $U$. ^083bb0

La définition précédente étant similaire à celle de la dérivée en analyse réelle, on a les mêmes propriété de base, à savoir en particulier :

 - linéarité $(\alpha f + \beta g)' = \alpha f' + \beta g'$
 - formule de leibniz $(f g)' = f' g + f g'$
 - $(\frac{1}{f})' = \frac{-f'}{f^2}$
 - chain rule $(g \circ f)'(z) = g'(f(z)) \cdot f'(z)$

où les domaines de dérivabilité de $g$ et $f$ satisfait les conditions appropriées à la validité de ces formules.

Une [[Fonctions Holomorphes#^083bb0|fonction holomorphe]] sur tout $\mathbb{C}$ est dite **entière**. ^7bcb89

# Dérivation de la fonction réciproque

Soit $f : A \subset \mathbb{C} \rightarrow \mathbb{C}$ une [[Fonctions Holomorphes|FH]] sur l'ouvert $A$ tel que $f'(z)$ soit continue aussi sur $A$. Si on suppose $f'(z_0) \neq 0$  pour $z_0 \in A$, alors il existe un voisinage $V$ de $f(z_0)$ et un voisinage $U$ de $z_0$ tels que $f(z)$ soit une bijection de $U$ dans $V$. La fonction réciproque $f^{-1}(w)$ est de plus une FH sur $V$ et sa dérivée est donnée par :$$(f^{-1})'(w) = \frac{1}{f'(z)}$$où $w = f(z)$.
