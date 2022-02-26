---
layout: page
title: Beispiel 7.23
mathjax: true
---

## Rössler-System, approximative Linearisierung nullter Ordnung

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

Berechnet wird eine Beobachterverstärkung $k_0(\hat{x})$, mit der eine approximative Linearisierung nullter Ordnung erzielt wird. Für die linearisierte Fehlerdynamik sei das charakteristische Polynom

$$
a_0+a_1s+a_2s^2+s^3
$$

vorgegeben. Mit der Beobachterverstärkung

$$
k_{0}(\hat{x})=\left(\begin{array}{c}
aa_{2}+a_{1}\\
(1-a^{2})a_{2}-aa_{1}-a_{0}\\
a_{2}\hat{x}_{3}
\end{array}\right)
$$

erzielt man eine Approximation nullter Ordnung. Das entspricht einem *High-Gain-Beobachter*, der jetzt allerdings über die Beobachternormalform entwurfen wurde.

### Maxima

<iframe src="Roessler_k0.html" width="100%" height="2100"></iframe>


Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 352**.

