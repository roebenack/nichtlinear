---
layout: page
title: Beispiel 7.8
mathjax: true
---

## Rössler-System, Berechnung nach Krener und Isidori

Betrachtet wird das [Rössler-System](https://de.wikipedia.org/wiki/R%C3%B6ssler-Attraktor)

$$
\begin{array}{lcl}
\dot{x}_{1} & = & -x_{2}-x_{3}\\
\dot{x}_{2} & = & x_{1}+ax_{2}\\
\dot{x}_{3} & = & c+x_{3}(x_{1}-b)
\end{array}
$$

mit den Parametern $a,b,c>0$ und der Ausgangsgleichung

$$
y=x_3
$$

Für die Berechnung eines Normalform-Beobachters nach Krener und Isidori benötigt man das *Startvektorfeld* $v$ und die darauf aufbauenden Lie-Klammern:

$$
v(x)=\left(\begin{array}{r}
0\\
-1\\
0
\end{array}\right),\;\operatorname{ad}_{-f}v(x)=\left(\begin{array}{r}
1\\
-a\\
0
\end{array}\right),\;\operatorname{ad}_{-f}^{2}v(x)=\left(\begin{array}{c}
a\\
1-a^{2}\\
x_{3}
\end{array}\right).
$$

Diese Lie-Klammern werden in der Steuerbarkeitsmatrix zusammengefasst.

### Maxima

<iframe src="Roessler_Krener_Isidori.html" width="100%" height="2100"></iframe>


Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 325-336**.

