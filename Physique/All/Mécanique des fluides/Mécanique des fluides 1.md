# 0. Intro - définitions

- **Fluides** : un systèmes d'un très grand nombre de molécules pouvant se déplacer les unes par rapport aux autres, entres autres les gaz et les liquides. Ce système est caractérisé par un *volume* $V$, une *masse* $m$ et un *nombre de molécules* $N$. On peut ajouter à cela la *densité particulaire* $n_{\rho} = \frac{N}{V} = n \frac{N_A}{V} = \frac{m N_A}{M V} = \rho \frac{N_A}{M}$ où $n$ est le *nombre de moles*, $M$ est la *masse molaire*, $\rho$ est la *masse volumique* et $N_A$ est le *nombre d'Avogadro*.
- **Mécanique des fluides :** description du comportement mécanique des fluides comme milieu continu
---
**3 échelles spatiales :**
- macroscopique ($L>$ mm), le fluide est considéré comme un milieu continu (écoulement d'une rivière, etc...)
- microscopique ($L \approx \mathring{\mathrm A}$), le fluide est composé de molécules en agitation thermique perpétuelle
- mésoscopique ($L \approx$ µm), est une échelle intermédiaire, encore continue, on peut considérer des particules de fluides contenant un grand nombre de molécules.
---

# 1. La statique des fluides

## 1.1. Pression

Soit un fluide au repos dans un récipient. Sur un élément de surface $\mathrm{d}S$ de la paroi, le fluide exerce une force $\mathrm{d}\vec{F}$, résultant dans des chocs des molécules du fluide sur la paroi. Cette force est *normale* à $\mathrm{d}S$, on écrit $\mathrm{d} \vec{F} = P \mathrm{d} \vec{S}$, où le vecteur $\mathrm{d}\vec{S}$ est dirigé du fluide vers l'extérieur du récipient.
La grandeur scalaire $P$ s'appelle la *pression* et a pour unité SI le pascal (Pa) en N/m²

La pression atmosphérique normale (valeur moyenne au niveau de la mer). $$P_0 = 1,01325 \cdot 10^{5} \ \mathrm{Pa} = 1 \ \mathrm{atm}$$D'après le principe de l'action réaction, l'élément de surface $\mathrm{d}\vec{S}$ exerce sur le fluide la force opposée $-\mathrm{d}\vec{F}$.

---
### Pression au sein d'un fluide
![[pression.png]]
Dans un fluide, on peut isoler un petit volume d'un point $M$. La force de pression du fluide environnant sur le volume à la surface $\mathrm{d}S$ est $\mathrm{d}\vec{F} = -P \mathrm{d}\vec{S}$ 

### Propriétés

- Dans un fluide en équilibre, la pression est isotrope (indépendante de l'orientation de la surface d'application) $P_x = P_y = P_z = P$
- Les fluides incompressibles transmettent intégralement les écarts de pression ([principe de Pascal](https://fr.wikipedia.org/wiki/Principe_de_Pascal)) 
>La surpression $p$ est totalement transmise du petit piston vers le grand piston, comme $S \gg s$, on a $F = pS \gg f = ps$

## 1.2 Équilibre mécanique d'un fluide dans le champ de pesanteur

La relation fondamentale $$\boxed{\frac{\mathrm{d} P}{\mathrm{d} z} = -\rho g}$$
**Détail de l'équilibre mécanique**
>Équilibre d'un élément de fluide, petit volume $\mathrm{d}\tau$ autour d'un point $M_0$ 
>$P_+ = P(z+\mathrm{d}z)$ et $P_- = P(z)$
>$\Rightarrow P_+ - P_- = P(z+\mathrm{d}z) - P(z) \simeq P'(z) \mathrm{d}z$
>$$\begin{align}
&P_- \mathrm{d}S = P_+ \mathrm{d}S + \rho g \mathrm{d} \tau \Rightarrow P_- \mathrm{d}x \mathrm{d}y = P_+ \mathrm{d}x \mathrm{d}y + \rho g \mathrm{d}x \mathrm{d}y \mathrm{d}z \\
&\Rightarrow P_- - P_+ = \rho g \mathrm{d}z \Rightarrow P(z) - P(z+\mathrm{d}z) = \rho g \mathrm{d}z \\
&\Rightarrow  \frac{P(z) - P(z+\mathrm{d}z)}{\mathrm{d}z} = - \rho g \\
&\Rightarrow \boxed{\frac{\mathrm{d}P}{\mathrm{d}z} = - \rho g}
\end{align}$$

Mais $\rho$ est constante, donc $\frac{\mathrm{d}P}{\mathrm{d}z}$ est constant. Ce qui donne la solution générale $P(z) = -\rho g z + C$ où $C$ est une constante d'intégration qui sera déterminée par les conditions initiales ($P(z_0) = P_0$)
Si $P(z_0) = P_0$, alors $$\begin{align}
&P(z_0) = - \rho g z_0 + C = P_0 \\
\Rightarrow &C = P_0 + \rho g z_0 \\
\Rightarrow &P(z) = -\rho g z + P_0 + \rho g z_0 \\
\Rightarrow &\boxed{P(z) = P_0 -\rho g(z - z_0)} 
\end{align}$$**Loi hydrostatique**
la différence de pression entre deux points quelconques d'un fluide en équilibre est égale au poids d'un cylindre de fluide *de section unité* ayant pour hauteur la dénivellation entre les deux points ($h$)

### Calcul de pression
![[calculdepression1.png]]
$M_1$ et $M_8$ sont à la même altitude $z_1$, ce qui veut donc dire que $P(M_1) = P(M_8) + \rho g (z_1 - z_1) = P(M_8)$, et donc, pareillement, on trouve que $P(M_2) = P(M_3) = P(M_4) = P(M_7)$ et que $P(M_5) = P(M_6)$
de plus $P_2 = P_1 + \rho g (z_1 - z_2)$ et etc...

## 1.3. Théorème d'Archimède

> [!théorème] Poussée d'Archimède
> La résultante des forces de pression exercées sur un corps totalement immergé dans un fluide est opposée au *poids du fluide déplacé*. Cette force est la *[poussée d'Archimède](https://en.wikipedia.org/wiki/Archimedes'_principle)* : $$\boxed{\vec{F}_A = -\rho_f V_i \vec{g}}$$où $V_i$ est le volume du solide immergé et $\rho_f$ est la masse volumique du fluide
> ![[Pasted image 20240323181137.png]]

## 1.4. Application de la relation fondamentale (suite)

En partant de la relation fondamentale $$\frac{\mathrm{d}P}{\mathrm{d}z} = - \rho g$$puis en considérant la loi des gaz parfaits $$\begin{align}
PV = nRT \Rightarrow \frac{n}{V} = \frac{P}{RT}\\
\Rightarrow \frac{m}{MV} = \frac{P}{RT}\\
\Rightarrow \frac{m}{V} = \frac{MP}{RT}\\
\Rightarrow \Aboxed{\rho = \frac{MP}{RT}}
\end{align}$$
### Atmosphère isotherme

On considère d'abord le cas où la température est constante, la relation fondamentale ainsi que la loi des gaz parfaits donnent une l'équation différentielle suivante$$\frac{\mathrm{d}P}{\mathrm{d}z} + aP = 0$$avec $a = \frac{Mg}{RT}$ 
Il s'agit donc d'une équation différentielle linéaire du premier ordre, ayant une solution de la forme$$P = A e^{-az}$$où $A = P(0) = P_0$, ainsi obtient-on la **loi barométrique** $$\boxed{P(z) = P_0 \exp \left( -\frac{Mg}{RT}z \right)}$$
#### Discussions

On peut poser $H = \frac{RT}{Mg}$ donnant ainsi $$P(z) = P_0 \exp \left( -\frac{z}{H}\right)$$Quand $z \ll H$ on trouve alors que $$\begin{align}
\exp \left( -\frac{z}{H}\right) \sim 1- \frac{z}{H}\\
\Rightarrow P(z) \sim P_0 \left( 1- \frac{z}{H} \right) = P_0 - \frac{P_0}{H}z\\
\Rightarrow P(z) \sim P_0 - \rho_0 g z 
\end{align}$$
Dans le cas général $$\begin{align}
P(z)/P_0 = \exp \left( \frac{-z}{H} \right)\\
z=H \Rightarrow P(H)/P_0 = e^{-1} \simeq 0,37
\end{align}$$
![[Pasted image 20240506164204.png]]
### Température affine
Dans le cas où la température varie de manière affine, c'est à dire que $T = T_0(1-cz)$ 
$$\frac{\mathrm{d}P}{\mathrm{d}z} + a(z) P = 0$$où $a(z) = \frac{Mg}{R T_0 (1- cz)}$. La solution de cette équation différentielle est de la forme $$\begin{align}
P(z) = P_0 \exp \left( - \int_0^z a(t)\ \mathrm{d}t \right)\\
- \int_0^z a(t)\ \mathrm{d}t = - \int_0^z \frac{Mg}{RT_0 (1-ct)}\ \mathrm{d}t \\
= \frac{a_0}{c} \int_0^z \frac{-c}{1-ct}\ \mathrm{d}t = \frac{a_0}{c} \left[ \ln(1-ct) \right]_0^z\\
= \frac{a_0}{c}\ln(1-cz)\\
\Rightarrow \Aboxed{P(z) = P_0 (1-cz)^\frac{a_0}{c}}
\end{align}$$
#### Discussions

On obtient donc deux solutions pour la pression atmosphérique, suivant si la température reste constante, ou si elle varie linéairement. On résume les deux résultats $$\begin{align}
P_1(z) = P_0 \exp \left( -\frac{Mg}{R T_0} z \right) \\
P_2(z) = P_0 \left( 1 - \frac{k R}{Mg} \frac{z}{H} \right)^\frac{Mg}{kR}
\end{align}$$ou en utilisant une notation plus compacte $$\begin{align}
P_1(z) = P_0 \exp \left( -\frac{z}{H} \right) \\
P_2(z) = P_0 \left( 1 - cz \right)^\frac{1}{Hc}
\end{align}$$
![[Pasted image 20240506170940.png]]
## Situations de pression non-uniforme (surface non-plane)

Barrage hémicylindrique (rayon $R$) rempli d'eau sur une hauteur $h$

# phénomènes capillaires (capillarité)

Tendance d'un liquide à remonter vers le sommet d'un tube très fin. Phénomènes dus à la tension superficielle

## Traction sur un film de savon posé sur un cadre

Tension superficielle

La tension superficielle est une tension qui existe à la surface d'un liquide au repos, et qui tend à minimiser l'aire de celle-ci. Minimisation de l'énergie de surface à un volume donné $\rightarrow$ surface la plus petite possible

tension superficielle $\sigma$ $$\sigma = \frac{F}{L}$$Travail fourni pour augmenter la surface de $\Delta S$ : $$\Delta W = F \Delta x = \frac{F}{L} L \Delta x = \sigma \Delta S$$Énergie de surface : $$U_\mathrm{surf} = \sigma S$$
## Origine physique de la tension superficielle

Explication : environnement local des molécules à la surface $\rightarrow$ forces localisées au voisinage de la surface tendent à réduire le volume du liquide et plus précisément ou surface

## Lois associées à la capillarité 

### 1. Loi de Laplace

Pression subit un accroissement à la traversée de la surface de séparation de deux fluides, de la face convexe vers la face concave, égal à la tension superficielle de l'interface multipliée par 2 fois la courbure moyenne.$$\Delta P = 2 \sigma C_m$$où :
- $\Delta P = P_2 - P_1$ est la surpression

Caténoïde : $C_m = 0$

#### Loi de Laplace pour une surface sphérique

Surface sphérique rayon $R \rightarrow$ différence de pression entre pression intérieure et pression extérieure : $$\Delta P = \frac{2 \sigma}{R}$$ 
### 2. loi de Jurin

La loi de Jurin s'applique à un fluide dans un tube cylindrique, la hauteur $h$ à laquelle le fluide grimpe dans le tube est donnée par $$h = \frac{2 \sigma \cos \theta}{\rho g r}$$où $\theta$ est l'angle de raccordement, c'est à dire l'angle que décrit le fluide avec la paroi du cylindre.  