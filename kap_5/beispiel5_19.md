---
layout: page
title: Beispiel 5.19
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

beschreiben. Berechnet wird eine zustandsabhängige Reglerverstärkung $\sigma(x)$, welche einer Approximation erster Ordnung der exakten Eingangs-Zustands-Linearisierung entspricht.

### Maxima

<iframe src="Inverses_Pendel_Approx_1.html" width="100%" height="750"></iframe>


Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 260**.

