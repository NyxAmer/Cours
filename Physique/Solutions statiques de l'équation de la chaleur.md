---
tags:
  - Thermodynamique/TransfertsThermique
---
Considérer les cas statiques permet de réécrire l'équation de la chaleur en prenant en compte que $\displaystyle \frac{\partial T}{\partial t} = 0$, ainsi l'équation de la chaleur devient une équation de Laplace $$\nabla^2 T = 0$$On examine des cas analytiques à cette équation.
# Solutions simples

## Mur

On considère un mur d'épaisseur $L$ et de surface $S$, on note la température d'un coté $T_1$ et la température de l'autre $T_2$. On décide de résoudre l'équation de la chaleur uniquement le long de l'axe transverse au mur pour des raisons de symétrie du problème, ainsi l'équation de la chaleur devient $$\begin{align}
\nabla^2 T &= \frac{\partial ^2 T}{\partial x^2} = 0\\
\Rightarrow T(x) &= Ax + B
\end{align}$$On a donné la solution générale directement par double intégration. 

En appliquant les conditions limites, à savoir $T(x=0) = T_1, T(x=L) = T_2$ on trouve les valeurs des coefficients $A$ et $B$ et on donne l'expression du champ de température $$\begin{align}
B &= T_1 \\
A &= \frac{T_2 - T_1}{L} \\
\Rightarrow T(x) &= \frac{T_2 - T_1}{L} x + T_1
\end{align}$$
On calcule la densité de flux de température, donnée par la [[Equation de la chaleur#Loi de Fourier|loi de Fourier]]$$\begin{align}
\vec{j}_q &= - \lambda \nabla T\\
\Rightarrow \vec{j}_q &= -\lambda \frac{\mathrm{d} T}{\mathrm{d} x} \vec{e}_x \\
\Rightarrow \vec{j}_q &= \lambda \frac{T_1 - T_2}{L} \vec{e}_x
\end{align}$$Ainsi, en admettant que $T_1 > T_2$, le flux de chaleur sur la surface du mur devient $$\begin{align}
\Phi &= \iint_S \vec{j}_q \cdot \mathrm{d}\vec{S}\\
\Rightarrow \Phi &= S \| \vec{j}_q \| \\
\Rightarrow \Phi &= S \lambda \frac{T_1 - T_2}{L} \\
\Rightarrow T_1 - T_2 &= \frac{L}{\lambda S} \Phi
\end{align}$$On obtient alors une expression analogue à la loi d'Ohm $U = RI$, où on peut identifier $T_1 - T_2$ à la différence de potentiel, $\Phi$ au courant et $\frac{L}{\lambda S}$ à une résistance, qu'on appellera résistance thermique.$$R_{\mathrm{th}} = \frac{L}{\lambda S}$$

## Cylindre creux

On imagine un cylindre creux, de rayon interne $R_1$, de rayon externe $R_2$, de longueur $L$ et suffisamment long pour n'étudier la solution de l'équation de Laplace que le long de la direction radiale en base cylindrique. On défini la température interne $T(r = R_1) = T_1$ et la température externe $T(r = R_2) = T_2$. 

L'expression du laplacien en coordonnées cylindrique est donnée par $$\nabla^2 = \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial}{\partial r}\right) + \frac{1}{r^2} \frac{\partial^2}{\partial \theta^2} + \frac{\partial^2}{\partial z^2}$$ce qui se simplifie à seulement le terme en $r$ dans notre cas d'étude $$\nabla^2 T = \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial T}{\partial r}\right) = 0$$
La solution générale s'exprime alors comme suit $T(r) = A \ln(r) + B$, en appliquant les conditions limites on peut trouver $$\begin{align}
A &= \frac{T_2 - T_1}{\ln(R_2 / R_1)} \\
B &= T_1 + \frac{T_1 - T_2}{\ln(R_2/R_1)} \ln(R_1)\\
\Rightarrow T(r) &= \frac{T_2 - T_1}{\ln(R_2/R_1)} \ln(r) + \frac{T_1 - T_2}{\ln(R_2/R_1)} \ln(R_1) + T_1 \\
&= T_1 + \frac{T_2 - T_1}{\ln(R_2/R_1)} \ln(r/R_1)
\end{align}$$
On part de la loi de Fourier pour exprimer la flux puis la résistance thermique du cylindre  $$\begin{align}
\vec{j}_q (R_1) &= - \lambda \frac{\mathrm{d} T}{\mathrm{d} r} \Bigg\rvert_{R_1} \vec{e}_r \\
&= \frac{\lambda (T_1 - T_2)}{R_1 \ln(R_2/R_1)} \vec{e}_r \\
\Rightarrow \Phi(R_1) &= \| \vec{j}_q \| 2 \pi R_1 L \\
&= \frac{2 \pi \lambda L (T_1 - T_2)}{\ln(R_2/R_1)} \\
\Rightarrow R_{\mathrm{th}} &= \frac{T_1 - T_2}{\Phi}\\
&= \frac{\ln(R_2/R_1)}{2 \pi \lambda L}
\end{align}$$

## Sphère creuse

On considère une sphère de rayon et température internes $R_1$ et $T_1$ respectivement, et de rayon et température externes $R_2$ et $T_2$ respectivement. On applique la même méthode que précédemment, on détaillera un peu moins les calculs. On commence par rappeler l'expression du laplacien en coordonnées sphériques $$\nabla^2 = \frac{1}{r^2} \frac{\partial}{\partial r} \left( r^2 \frac{\partial}{\partial r} \right) + \frac{1}{r^2 \sin \theta} \frac{\partial}{\partial \theta} \left( \sin \theta \frac{\partial}{\partial \theta}\right) + \frac{1}{r^2 \sin^2 \theta} \frac{\partial ^2}{\partial \varphi^2}$$donc notre cas on résout uniquement selon $r$, car on assume une symétrie sphérique, ainsi on obtient l'équation suivante, dont on donne aussitôt la solution générale et au conditions limites $$\begin{align}
\nabla^2 T &= \frac{1}{r^2} \frac{\partial}{\partial r} \left( r^2 \frac{\partial T}{\partial r} \right) = 0 \\
\Rightarrow T(r) &= \frac{A}{r} + B \\
\Rightarrow A &= \frac{R_1 R_2}{R_2 - R_1}(T_1 - T_2) \\
\Rightarrow B &= T_1 - \frac{R_1}{R_2 - R_1}(T_1 - T_2) \\
\Rightarrow T(r) &= T_1 + \frac{R_2 (T_1 - T_2)}{R_2 - R_1} \left( \frac{R_1}{r} - 1 \right)\\
\Rightarrow \vec{j}_q (R_1) &= - \lambda \frac{\mathrm{d} T}{\mathrm{d} r} \Bigg\rvert_{R_1} \vec{e}_r \\
&= \frac{\lambda R_2}{R_1 (R_2 - R_1)}(T_1 - T_2) \\
\Rightarrow \Phi &= \| \vec{j}_q (R_1) \| 4 \pi R_1^2\\
&= \frac{\lambda 4 \pi R_1 R_2}{R_2 - R_1} (T_1 - T_2)\\
\Rightarrow R_{\mathrm{th}} &= \frac{R_2 - R_1}{4 \pi \lambda R_1 R_2}
\end{align}$$

# Resistance thermique

On a donc introduit le concept de résistance thermique par analogie avec la loi d'Ohm pour l'électricité. 

Ce concept est très puissant car on peut s'en servir de la même manière que dans les circuits électriques, où on peut alors calculer une résistance équivalente en combinant des résistances connues des différents milieux qui composent notre sujet d'étude. 

Les résistances thermiques en série s'additionnent, et les résistance en dérivation se combinent en prenant l'inverse de la somme des inverses des résistances.

## Résistance d'une interface fluide/solide

Pour cette situation, on considère une surface d'échange thermique entre un milieu solide et un milieu fluide. Un fluide, est mis en mouvement spontanément par les changements de température en son sein, il s'agit de mouvements convectifs naturels. Ces mouvements vont donc contribuer à transporter par convection la chaleur loin de l'interface, cela créer un gradient de température et influence le flux thermique. La loi de Newton permet de relier le flux thermique à la différence de température entre la surface et la température limite du fluide (suffisamment loin de la surface pour ignorer son influence).

> [!Théorème] Loi de Newton
> Pour une surface faisant l'interface entre un fluide et un solide, le flux de chaleur est donné par $$\Phi = h S (T_{\mathrm{f}} - T_{\mathrm{S}})$$ où : 
> - $h$ est le coefficient de transfert de chaleur
> - $S$ est la surface de l'interface fluide/solide
> - $T_{\mathrm{f}}$ est la température du fluide loin du mur
> - $T_{\mathrm{S}}$ est la température de la surface

Ainsi, de la même manière que ce qu'on a fait plus tôt, on considère $\Phi$ comme le courant, $T_{\mathrm{f}} - T_{\mathrm{S}}$ comme la différence de potentiel, et donc, la résistance thermique dans ce cas devient $$R_{\mathrm{th}} = \frac{1}{hS}.$$

## Récapitulatif

On donne alors un bref récapitulatif d'expressions pour les résistance thermiques de différentes situations ou géométries simples


| Milieu                  | Résistance thermique                        |                                                                              |
| ----------------------- | ------------------------------------------- | ---------------------------------------------------------------------------- |
| Couche plane            | $$\frac{L}{\lambda S}$$                     | $L$ : épaisseur<br>$S$ : surface                                             |
| Couche cylindrique      | $$\frac{\ln(R_2/R_1)}{2 \pi \lambda L}$$    | $R_1$ : rayon interne<br>$R_2$ : rayon externe<br>$L$ : longueur du cylindre |
| Couche Sphérique        | $$\frac{R_2 - R_1}{4 \pi \lambda R_1 R_2}$$ | $R_1$ : rayon interne<br>$R_2$ : rayon externe                               |
| Interface fluide/solide | $$\frac{1}{hS}$$                            | $S$ : surface                                                                |
où $\lambda$ représente la conductivité du milieu solide et $h$ représente le coefficient de transfert de chaleur dans le cas de l'interface fluide/solide.