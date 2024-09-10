---
tags:
  - Électromagnétisme
---
# Équations de Maxwell dans le vide

|                                                                     | forme différentielle                                                                                                  | forme intégrale                                                                                                                           |
| ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **[[Théorème de Gauss\|Gauss]]**                                    | $$\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\varepsilon_0}$$                                                           | $$\oint_{S} \vec{E} \cdot \mathrm{d} \vec{S}= \frac{Q_\mathrm{int}}{\varepsilon_0}$$                                                      |
| **[[Théorème de Gauss\|Gauss]] magnétique**                         | $$\vec{\nabla} \cdot \vec{B} = 0$$                                                                                    | $$\oint_{S} \vec{B} \cdot \mathrm{d} \vec{S}= 0$$                                                                                         |
| **[[Loi de Faraday\|Maxwell-Faraday]]**                             | $$\vec{\nabla} \times \vec{E} = - \frac{\partial \vec{B}}{\partial t}$$                                               | $$\oint_{C} \vec{E} \cdot \mathrm{d} \vec{l}= -\frac{\mathrm{d}\Phi_\mathrm{m}}{\mathrm{d}t}$$                                            |
| **[[Théorème d'Ampère#Equation d'Ampère-Maxwell\|Ampère-Maxwell]]** | $$\vec{\nabla} \times \vec{B} = \mu_{0} \left( \vec{J} + \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}\right)$$ | $$\oint_{C} \vec{B} \cdot \mathrm{d} \vec{l}=\mu_{0} \left( I + \varepsilon_{0} \frac{\mathrm{d} \Phi_\mathrm{el}}{\mathrm{d} t}\right)$$ |

# Équations de Maxwell dans un milieu 

|                      | forme différentielle                                                                       | forme intégrale                                                                                                   |
| -------------------- | ------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------- |
| **Gauss**            | $$\vec{\nabla} \cdot \vec{D} = \rho_\mathrm{f} $$                                          | $$\oint_{S} \vec{D} \cdot \mathrm{d} \vec{S}= Q_\mathrm{f}$$                                                      |
| **Gauss magnétique** | $$\vec{\nabla} \cdot \vec{B} = 0$$                                                         | $$\oint_{S} \vec{B} \cdot \mathrm{d} \vec{S}= 0$$                                                                 |
| **Maxwell-Faraday**  | $$\vec{\nabla} \times \vec{E} = - \frac{\partial \vec{B}}{\partial t}$$                    | $$\oint_{C} \vec{E} \cdot \mathrm{d} \vec{l}= -\frac{\mathrm{d}\Phi_\mathrm{m}}{\mathrm{d}t}$$                    |
| **Ampère-Maxwell**   | $$\vec{\nabla} \times \vec{H} = \vec{J}_\mathrm{f} + \frac{\partial \vec{D}}{\partial t}$$ | $$\oint_{C} \vec{H} \cdot \mathrm{d} \vec{l}= I_\mathrm{f} +  \frac{\mathrm{d} \Phi_\mathrm{ind}}{\mathrm{d} t}$$ |
où :
- $\vec{D} = \varepsilon_{0} \vec{E} + \vec{P}$ est le **vecteur induction électrique**
- $\displaystyle \vec{P} = \frac{\mathrm{d} \vec{p}}{\mathrm{d} \tau}$ est le **vecteur polarisation** avec $\vec{p}$ le **moment dipolaire**
- $\displaystyle \vec{H} = \frac{\vec{B}}{\mu_0} - \vec{M}$ est le vecteur **champ d'aimantation**, ou **champ d'excitation magnétique** (officiellement, il faudrait l'appeler **champ magnétique**, cependant cela porte à confusion avec $\vec{B}$ qu'on devrait appeler **vecteur induction magnétique**)
- $\displaystyle \vec{M} = \frac{\mathrm{d} \vec{m}}{\mathrm{d} \tau}$ est le **vecteur aimantation** avec $\vec{m}$ le **moment magnétique**