---
layout: page
title: Beispiel 4.45
mathjax: true
---

## Inverses Pendel mit Trägheitsrad

Das inverse Pendel mit Trägheitsrad lässt sich durch das Zustandsraummodell

$$
\dot{x}=\underbrace{\left(\begin{array}{c}
x_{2}\\
\phantom{-}\frac{m_{0}}{J_{1}-I_{2}}\sin x_{1}\\
-\frac{m_{0}}{J_{1}-I_{2}}\sin x_{1}
\end{array}\right)}_{f(x)}+\underbrace{\left(\begin{array}{c}
0\\
-\frac{1}{J_{1}-I_{2}}\\
\frac{J_{1}}{I_{2}(J_{1}-I_{2})}
\end{array}\right)}_{g(x)}u
$$

beschreiben. Berechnet wird eine Differentialform, us der sich der Ausgang bestimmen lässt.


### Maxima

<iframe src="Inverses_Pendel_mit_Rad_EZ.html" width="100%" height="1350"></iframe>


Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 157-159**.

