---
layout: page
title: Beispiel 6.28
mathjax: true
---

## Berechnung der Beobachterverstärkung mit der Moore-Penrose-Inversen

Wir betrachten das Beispielsystem

$$
\begin{array}{lcl}
\dot{x}_{1} & = & x_{3}-x_{2}^{3}\\
\dot{x}_{2} & = & -x_{2}-x_{3}^{2}u\\
\dot{x}_{3} & = & -x_{3}+x_{1}^{2}+u\\
y & = & x_{1}
\end{array}
$$

aus [Isidori 1995, S. 167]. Das System besitzt den relativen Grad $r=2$. Aus der reduzierten Beobachtbarkeitsmatrix wird die Beobachterverstärkung unter Nutzung der [Moore-Penrose-Inversen](https://de.wikipedia.org/wiki/Pseudoinverse) berechnet.


### Maxima

<iframe src="HG_Isidori2.html" width="100%" height="1200"></iframe>

Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 291-292**.

