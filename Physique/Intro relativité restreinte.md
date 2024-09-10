---
tags:
  - Relativité/Restreinte
---
# Cadre théorique

Selon la philosophie orthodoxe pour l'élaboration des théories en physique, cette dernière s'attache à caractériser de manière interprétative et prédictive les **phénomènes observables**. Un tel phénomène se produit quelque part dans l'espace et le temps.

Formellement on peut abstraire l'espace ambient comme un espace affine 3D $\Sigma_3$. On le munit d'une origine $O$ afin de caractériser les positions par des vecteurs dans l'espace vectoriel $S_3$ associé à $\Sigma_3$. On munit $S_3$ d'une base $\vec{e_i}$, ce qui correspond à munir $\Sigma_3$ d'un repère cartésien $R_c (O, \vec{e_i})$. 

On ajoutera à cette espace un axe $\mathbb{R}_t$ afin de former l'**espace-temps** $\mathcal{E} = \mathbb{R}_t \times \Sigma_3$. On ajoute sur l'axe $\mathbb{R}_t$ une mesure $\mu_t$ qu'on appellera **horloge** $H$. Cette dernière donne une référence temporelle entre deux évènements qui correspond à la durée entre ces deux évènements. La durée sera définie entre deux dates $t_1$ et $t_2$ comme la mesure de Lebesgue $\mu_t (t_1, t_2) = |t_2 - t_1|$.

L'horloge $H$ sur $\mathbb{R}_t$ et le repère cartésien $R_c$ sur $\Sigma_3$ forment un **référentiel d'espace temps $\mathcal{R}$** sur $\mathcal{E}$. 

On appelle **évènement** un tuplet de coordonnées $\vec{r} = \sum_i x^i \vec{e_i} = x^i \vec{e_i}$ d'espace, et de temps, le localisant complètement dans l'espace et le temps où on définit $x^0$ comme la coordonnée de temps, et $x^n, \ n \ge 1$ représentant les coordonnées d'espace. Ainsi on peut en 3D définir les vecteurs d'espace temps comme suit, les trois notations étant interchangeables.  $$\begin{pmatrix} t \\ \vec{r} \end{pmatrix} = \begin{pmatrix} t \\ x \\ y \\ z \end{pmatrix} = \begin{pmatrix} x^0 \\ x^1 \\ x^2 \\ x^3 \end{pmatrix}$$Le choix du référentiel permet d'établir une correspondance bijective entre $\mathcal{E}$ et $\mathbb{R}^4$. 

Un évènement a une réalité physique qui ne dépend pas du référentiel. Aussi les coordonnées d'un évènement dépendent du référentiel.

En relativité restreinte, on considèrera l'espace ambiant $\Sigma_3$ comme plat (Euclidien) et où la métrique spatiale est la métrique euclidienne.

# Principe de relativité

Le principe de relativité peut s'énoncer comme suit

> [!théorème] Principe de relativité 
> Soit $\mathcal{R}$ un référentiel d'espace-temps donné. 
> 
> >Il existe alors une classe infinie de référentiels $\mathcal{R}(a)$, paramétrée continument par $a \in \mathbb{R}^n$, qui sont physiquement équivalents, c'est à dire dans lesquels les lois de la physique ont la même forme explicite. 
> 
> Une telle classe d'équivalence est appelée **classe d'inertie**. 

Par "lois de la physique" on parle ici des relations explicites liant les observables physiques entre elles.

Construire une **théorie de la relativité** consiste à déterminer les relations liant les coordonnées $(t, \vec{r})$ et $(t', \vec{r}')$ d'un évènement dans deux référentiels $\mathcal{R}(\vec{a})$ et $\mathcal{R}'(\vec{a}')$, appartenant à une même **classe d'inertie**.

# Transformations d'inertie

> [!théorème] Transformations d'inertie
> On notera la transformation $I : (t, \vec{r}) \mapsto (t', \vec{r}')$ la **transformation d'inertie** permettant de passer d'un référentiel à un autre dans une même **classe d'inertie**.
> 
> >L'ensemble $\mathcal{I}$ des transformations d'inertie connectant les référentiels d'une même classe d'inertie forme un groupe avec la composition des transformation comme opération de groupe.

> [!démo]-
> Les classes d'inertie forment une **classe d'équivalence** au sens mathématique du terme. 
> 
> La relation d'équivalence entre $\mathcal{R}$ et $\mathcal{R}'$  implique la **réflexivité** de la transformation d'inertie ($\mathcal{R} \sim \mathcal{R}' \Rightarrow \mathcal{R}' \sim \mathcal{R}$).
> C'est à dire que
>- s'il existe $I : \mathcal{R} \mapsto \mathcal{R}'$ alors il existe un $I^{-1} : \mathcal{R}' \mapsto \mathcal{R}$ 
>- et donc $I \circ I^{-1} =I^{-1} \circ I = \mathbb{1}$.
> 
> où $\mathbb{1}$ est la transformation identité ($\Rightarrow I \circ \mathbb{1} = \mathbb{1} \circ I = I$).
>
>La classe d'équivalence implique aussi la **transitivité** ($\mathcal{R} \sim \mathcal{R}' \sim \mathcal{R}'' \Rightarrow \mathcal{R} \sim \mathcal{R}''$).
>C'est à dire que
>- s'il existe $I : \mathcal{R} \mapsto \mathcal{R}'$ et $I' : \mathcal{R}' \mapsto \mathcal{R}''$ alors $I' \circ I : \mathcal{R} \mapsto \mathcal{R}''$ .
>
>Enfin, elle implique l'**associativité**.
>C'est à dire que
> - s'il existe les transformations $I_1$, $I_2$ et $I_3$ alors $(I_1 \circ I_2) \circ I_3 = I_1 \circ (I_2 \circ I_3)$.
> 
> Ces propriétés sont précisément les axiomes nécessaires pour faire de $\mathcal{I}$ un groupe avec la composition des transformations d'inertie comme opération de groupe.

Connaître les transformations d'inertie connectant deux référentiels de la même classe d'inertie permet par extension de connaître la transformation qui connecte les expressions d'une observable physique dans chacun des référentiels. 

## Hypothèses supplémentaires

Afin de déterminer de quel groupe $\mathcal{I}$ s'agit, et pour en obtenir une formulation explicite, on précise des hypothèses supplémentaires raisonnables sur l'espace temps.

- L'espace temps est homogène
	Les lois de la physique ne doivent pas dépendre de l'endroit ou de l'instant en dans l'espace temps, elles sont invariables par translation.
- L'espace temps est isotrope
	Les lois de la physique ne doivent pas dépendre de la direction dans lesquelles elles se produisent, elles sont invariables par rotation.
- Les lois de la physique sont supposées causales

Cela permet donc de dire que $O(3)$ est un sous groupe de $\mathcal{I}$.
