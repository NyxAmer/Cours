---
tags:
  - Maths/Analyse/Complexe
---
Une **série entière** est définis formellement comme $$\sum_{n \in \mathbb{N}} a_n (z-z_0)^n$$avec $(a_n)_{n \in \mathbb{N}}$ est une suite complexe et $z_0 \in \mathbb{C}$ est appelé le **centre de la série**. La somme infinie ci-dessus converge absolument et définit une fonction complexe sur le disque ouvert $D(z_0, R) = \left\{ z \in \mathbb{C} \big\rvert | z - z_0| < R \right\}$ de centre $z_0$ et de rayon $R \in \left[ 0, +\infty \right[$. $R$ et $D(z_0, R)$ sont respectivement le **rayon** et le **disque de convergence**. Celle-ci converge uniformément (même normalement) sur tout disque fermé $D(z_0, r), \ r< R$.

la fonction $\displaystyle f(z) = \sum_{n = 0}^\infty a_n (z-z_0)^n$ est continue sur $D(z_0, R)$.

On peut évaluer $R$ grâce à la règle de Cauchy-Hadamard ou la règle de d'Alembert.
En général, l'étude des propriétés d'une série entière se fait en se ramenant au cas où $z_0 = 0$ par translation.

# Dérivabilité de $f(z)$

$f(z)$ est une [[Fonctions Holomorphes|FH]] sur $D(z_0, R)$ et elle est dérivable terme à terme :$$f'(z) = \sum_{n=1}^\infty n a_n (z - z_0)^{n-1}$$
> [!démo] à faire

Une récurrence immédiate implique alors que $f(z)$ est une fonction indéfiniment dérivable sur son disque de convergence avec $$f^{(m)} (z) = \sum_{n=m}^\infty n(n-1)(n-2) \dots (n-m+1) a_n z^{n-m}$$où la série du membre de droite converge sur le disque $D(0, R)$. Par conséquent, pour une série convergente sur $D(z_0, R)$ on a $$f(z) = \sum_{n=0}^\infty \frac{f^{(n)} (z_0)}{n !} (z - z_0)^n$$c'est à dire que $f(z)$ s'identifie à une **série de Taylor** en $z_0$.

> [!démo] à faire


