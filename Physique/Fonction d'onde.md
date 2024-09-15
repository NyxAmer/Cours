---
tags:
  - Mécanique/Quantique
---
# Définition

On définit une fonction complexe qui caractérise l'état de tout système quantique notée généralement $\psi$. On peut choisir de l'exprimer en fonction des coordonnées d'espace temps.

> [!Théorème] Règle de Born
> La densité de probabilité du système est donnée par la norme au carré de la fonction d'onde $$ \mathrm{d} \mathbb{P}(\alpha) = |\braket{ \alpha | \psi }|^2 \ \mathrm{d} \alpha= \braket{ \alpha | \psi }^* \braket{ \alpha | \psi } \ \mathrm{d} \alpha$$

Donc en base de position $\psi(\vec{r},t)$ la densité de probabilité représente la densité de probabilité de présence et s'exprime $$\mathbb{P}(\vec{r},t) = \int_\Omega |\psi(\vec{r},t)|^2 \ \mathrm{d}V$$Cela veut donc dire que, pour que la fonction d'onde ait un sens physique il faut que cette intégrale soit définie. Dans ce cas on la dit de **carré sommable**. A noter que cela implique que la probabilité de présence n'est pas affecté par un facteur de phase $\psi \mapsto \psi e^{i \varphi}$.

> [!Théorème] Superposition
> Si $\psi_1$ et $\psi_2$ sont deux fonctions d'onde possibles pour le meme système, alors la probabilité totale est donnée par $$\mathbb{P} = | \psi_1 + \psi_2 |^2 = \mathbb{P}_1 + \mathbb{P}_2 + \psi_1^* \psi_2 + \psi_2^* \psi_1$$
