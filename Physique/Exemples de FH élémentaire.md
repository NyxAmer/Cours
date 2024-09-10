---
tags:
  - Maths/Analyse/Complexe
---
# Polynômes

$\displaystyle P(z) = \sum^N_{n=0} a_0z^n$ , $a_n \in \mathbb{C}, N \in \mathbb{N}$
$P(z)$ est une [[Fonctions Holomorphes#^7bcb89|fonction entière]] et $\displaystyle P'(z) = \sum^N_{n=1} n a_n z^{n-1}$ 
# Fonctions Rationnelles

$\displaystyle R(z) = \frac{P(z)}{Q(z)}$, où $P$ et $Q$ sont deux polynômes premiers entre eux. $R(z)$ est une [[Fonctions Holomorphes#^083bb0|FH]] sur $\mathbb{C}$ privée de l'ensemble des zéros de $Q$ et sur ce domaine $\displaystyle R'(z) = \frac{P'(z) Q(z) - P(z) Q'(z)}{Q^2(z)}$ 

# Exponentielle complexe

Si $z = x + iy$ et si on suppose définie l'exponentielle et les fonctions trigonométriques habituelles, on pose $$
e^z = e^{(x + iy)} = e^x (\cos y + i \sin y)
$$et en particulier $$e^{iy} = \cos y + i \sin y \iff \begin{dcases} \cos y = \frac{1}{2} (e^{iy} + e^{-iy}) \\ \sin y = \frac{1}{2i} (e^{iy} - e^{-iy}) \end{dcases}$$
$e^z$ est une [[Fonctions Holomorphes#^7bcb89|fonction entière]] et $(e^z)' = e^z$ 

# Fonctions trigonométriques et hyperboliques

## Trigonométriques

Les fonctions $\cos$ et $\sin$ peuvent se définir ainsi :
$$\begin{align}
\cos z = \frac{e^{iz} + e^{-iz}}{2} \\
\sin z = \frac{e^{iz} - e^{-iz}}{2i}
\end{align}$$
Elles sont entières et ont les propriétés habituelles de leur contrepartie réelle, en particulier :
- $(\cos z)' = -\sin z$, $(\sin z)' = \cos z$   $\forall z \in \mathbb{C}$
- $2 \pi$ périodique
- $\cos^2 z + \sin^2 z = 1$
- $\cos z = 0$ pour $\displaystyle z = (2k + 1) \frac{\pi}{2},\ k\in \mathbb{Z}$
- $\sin z = 0$ pour $\displaystyle z = k \pi,\ k\in \mathbb{Z}$
- $\sin (z + w) = \sin z \ \cos w + \cos z \ \sin w$
- $\cos (z + w) = \cos z \ \cos w - \sin z \ \sin w$
- $\begin{dcases} \cos (-z) = \cos z , \ \cos (\pi - z) = - \cos z \\ \sin( -z) = - \sin z , \ \sin(\pi - z) = \sin z \end{dcases}$

La tangente complexe est quant à elle : $$\tan z = \frac{\sin z}{\cos z} = \frac{1}{i} \frac{1 - e^{-2iz}}{1 + e^{2 iz}},$$elle est $\pi$ périodique et holomorphe sur $\mathbb{C} - \left\{  (2k + 1) \frac{\pi}{2}, \ k \in \mathbb{Z} \right\}$ avec $$(\tan z)' = \frac{1}{\cos^2 z} = 1 + \tan^2 z.$$
## Hyperboliques

