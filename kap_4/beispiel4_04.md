---
layout: page
title: Beispiel 4.4
mathjax: true
---

## Mobiler Roboter, Berechnung des relativen Grades

Der mobile Roboter fahre mit konstanter translatorischer Geschwindigkeit. Die Beeinflussung erfolgt nur über den Lenkwinkel $u$. Damit erhält man das kinematische Modell

$$
 \dot{x}=
 \begin{pmatrix}
  \sin x_3 \\ \cos x_3\\ 0
 \end{pmatrix} +
 \begin{pmatrix}
  0 \\ 0 \\ 1
 \end{pmatrix} u.
$$

Dazu betrachte man die Ausgangsabbildung

$$
h(x)=c_1x_1 + c_2x_2
$$

mit $c_1\neq0 \lor c_2\neq0$.
Berechnet wird der *relative Grad* $r=2$.

### Maxima

<iframe src="Roboter_rel_Grad.html" width="100%" height="1050"></iframe>


Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 118-119**.

