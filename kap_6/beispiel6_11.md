---
layout: page
title: Beispiel 6.11
mathjax: true
---

## Berechnung der Beobachterverstärkung  für die Eulersche Kreiselgleichungen

Die Rotation eines starren Körpers lässt sich mit den [eulerschen Kreiselgleichungen](https://de.wikipedia.org/wiki/Eulersche_Gleichungen_(Kreiseltheorie)) beschreiben. Mit geeigenter Skalierung bzw. Normierung kann man daraus das nichtlineare Zustandsraummodell

$$
\begin{array}{lcl}
\dot{x}_{1} & = & \lambda_{1}x_{2}x_{3}\\
\dot{x}_{2} & = & \lambda_{2}x_{1}x_{3}\\
\dot{x}_{3} & = & \lambda_{3}x_{1}x_{2}\\
y & = & x_{1}.
\end{array}
$$

ableiten, wobei die Winkelgeschwindigkeit der ersten Hauptachse als Ausgang $y$ zur Verfügung steht. unter Zuhilfenahme der Beobachtbarkeitsmatrix $Q(x)$ wird die Beobachterverstärkung $k(x)$ eines High-Gain-Beobachters berechnet.


### Maxima

<iframe src="Kreisel_High_Gain.html" width="100%" height="1200"></iframe>


Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 291-292**.

