---
tags:
  - Électromagnétisme
---
# Equation de continuité
![[Pasted image 20240324215215.png]]
Sous forme intégrée, la conservation de la charge s'écrit$$\begin{align}
&\oint_{S}\rho \vec{v} \cdot \mathrm{d}\vec{S} = -\frac{\mathrm{d}Q}{\mathrm{d}t} \\ \Rightarrow &\oint_{S} \vec{J}\cdot \mathrm{d}\vec{S} = \iiint_{\Omega} \vec{\nabla}\cdot \vec{J} \mathrm{d} \tau = -\frac{\mathrm{d}Q}{\mathrm{d}t} \\
\Rightarrow &\frac{\mathrm{d}Q}{\mathrm{d}t} = \frac{\mathrm{d}}{\mathrm{d}t} \left(\iiint_{\Omega} \rho \mathrm{d} \tau \right) = \iiint_{\Omega} \frac{\partial \rho}{\partial t} \mathrm{d} \tau \\
\Rightarrow &\boxed{\vec{\nabla} \cdot \vec{J} + \frac{\partial \rho}{\partial t} = 0}
\end{align}$$

> [!NOTE] Discussion de l'équation de continuité 
> - Cas statique : $\displaystyle \frac{\partial \rho}{\partial t} = 0 \Rightarrow \vec{\nabla} \cdot \vec{J} = 0 \Rightarrow \vec{\nabla} \times \vec{B} = \mu_{0} \vec{J}$
> Ce qui fonctionne avec l'expression locale du théorème d'Ampère
> - Cas non statique : $\displaystyle \frac{\partial \rho}{\partial t} \neq 0 \Rightarrow \vec{\nabla}\cdot \vec{J} \neq 0 \Rightarrow \vec{\nabla} \times \vec{B} \neq \mu_{0}\vec{J}$
> Cependant on voit ici que cela ne fonctionne plus avec le théorème d'Ampère
