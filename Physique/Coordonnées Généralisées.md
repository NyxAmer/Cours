---
tags:
  - Mécanique
---
On imagine un système à $N$ points dont on cherche la position. Il faut donc $N$ vecteurs positions pour caractériser complètement le système, et donc en 3D $\Rightarrow 3N$ coordonnée.

En pratique on peut parfois ignorer certaines coordonnées. Afin de déterminer la position du système de façon unique, on considère les degrés de libertés $\mathbf{f} \leq 3N$. 

Ces grandeurs (coordonnées degrés de liberté) ne correspondent pas forcément aux coordonnées cartésiennes. La position des points est paramétrée par $\mathbf{f}$ grandeurs réelles quelconques notées $q_i$ et regroupées dans un vecteur $\mathbf{q} = \{ q_1 , q_2 , \dots , q_{\mathbf{f}} \}$.

Ainsi on en déduit les vitesses généralisées $\displaystyle \dot{q}_i = \frac{\mathrm{d} q_i}{\mathrm{d}t}, \Rightarrow \dot{\mathbf{q}} = \{ \dot{q}_1, \dot{q}_2 , \dots , \dot{q}_{\mathbf{f}} \}$.

La donnée simultanée des $q_i$ et $\dot{q}_i$ détermine complètement l'**état mécanique** du système.

Les équations qui lient les accélérations aux $q_i$ et $\dot{q}_i$ sont les **équations du mouvement** et permettent de décrire les trajectoires du mouvement du système.

Le nombre de degrés de liberté d'un système dépend du nombre de contraintes qui s'appliquent sur le système. On peut noter les contraintes comme des fonctions de la position, du temps ou d'autres paramètres et on les classifie ainsi.

| Contraintes       | Scléronomes                                                            | Rhéonomes                                                                    |
| ----------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| **Holonomes**     | $f(\mathbf{q}) = 0$                                                    | $f(\mathbf{q}, t) = 0$                                                       |
| **Non-Holonomes** | $f(\mathbf{q}) \leq 0$<br>$f(\mathbf{q}, \dot{\mathbf{q}}) = 0$<br>... | $f(\mathbf{q}, t) \leq 0$<br>$f(\mathbf{q}, \dot{\mathbf{q}}, t) = 0$<br>... |

Dans un système avec $\lambda$ contraintes holonomes, le nombre de degrés de liberté devient $\mathbf{f} = 3N - \lambda$.

