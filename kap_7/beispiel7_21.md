---
layout: page
title: Beispiel 7.21
mathjax: true
---

## Rössler-System, Berechnung nach Li und Tao

Betrachtet wird das [Rössler-System](https://de.wikipedia.org/wiki/R%C3%B6ssler-Attraktor)

$$
\begin{array}{lcl}
\dot{x}_{1} & = & -x_{2}-x_{3}\\
\dot{x}_{2} & = & x_{1}+ax_{2}\\
\dot{x}_{3} & = & c+x_{3}(x_{1}-b)
\end{array}
$$

mit den Parametern $a,b,c>0$ und der modifizierten Ausgangsgleichung

$$
y=\ln(x_3).
$$

Zunächst berechnet man die Beobachtbarkeitsmatrix $Q(x)$. Die letzte Spalte ihrer Inversen liefert das Startvektorfeld $v(x)$. In der Steuerbarkeitsmatrix sind mehrfache Lie-Klammern des Startvektorfeldes zusammengefasst. Daraus ergibt sich die Ableitung der Ausgangsaufschaltung. Über eine Integration erhält man direkt die Ausgangsaufschaltung

$$
\alpha(y)=\left(\begin{array}{c}
a\operatorname{e}^{y}+c\operatorname{e}^{-y}\\
-\operatorname{e}^{y}-ac\operatorname{e}^{-y}-y\\
c\operatorname{e}^{-y}+ay
\end{array}\right).
$$

### Maxima

<iframe src="Roessler_Li_Tao.html" width="100%" height="2300"></iframe>


Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 349-350**.

