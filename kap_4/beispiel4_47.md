---
layout: page
title: Beispiel 4.47
mathjax: true
---

## Inverses Pendel mit Gleichstrommotor

Das inverse Pendel mit Gleichstrommotor lässt sich durch das Zustandsraummodell

$$
\begin{array}{lcl}
\dot{x}_{1} & = & x_{2}\\
\dot{x}_{2} & = & \frac{mg\ell}{J}\sin x_{1}-\frac{d}{J}x_{2}+\frac{K}{J}x_{3}\\
\dot{x}_{3} & = & -\frac{K}{L}x_{2}-\frac{R}{L}x_{3}+\frac{1}{L}u
\end{array}
$$

beschreiben. Die letzte Zeile der inversen Steuerbarkeitsmatrix liefert ein exaktes Differential, aus welchem die Ausgangsabbildung berechnet wird.

### Maxima

<iframe src="Inverses_Pendel_Gleichstrommotor_EZ.html" width="100%" height="1500"></iframe>


Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 161**.

