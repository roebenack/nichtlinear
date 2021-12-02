---
title: Beobachtbarkeitsabbildung und -martrix
layout: page
mathjax: true
---

Sei $\mathcal{M}\subseteq\mathbb{R}^n$ offen. 
Durch das Vektorfeld $f:\mathcal{M}\to\mathbb{R}^n$ und das Skalarfeld $h:\mathcal{M}\to\mathbb{R}$ wird ein nichtlienares System

$$
 \dot{x}=f(x),\quad y=h(x)
$$

beschrieben. Die *Beobachtbarkeitsabbildung* hat die Form

$$
 q(x)=
 \begin{pmatrix}
 h(x)\\
 L_fh(x)\\
 \cdots\\
 L_f^{n-1}h(x)
 \end{pmatrix}.
$$

Die zugehörige Jocobimatrix

$$
Q_B(x)=q^\prime(x)
$$

ist die *Beobachtbarkeitsmatrix*.

## Berechnung mit Maxima

Das Vektorfeld $f$ und der Vektor $x$ sind jeweils als Liste zu übergeben.

```maxima
ObservabilityMap(f,h,x):=block([i,n],
    n:length(x),
    makelist(LieScalar(f,h,x,i),i,0,n-1)
    )$

ObservabilityMatrix(f,h,x):=jacobian(ObservabilityMap(f,h,x),x)$
```

Aufruf zur Berechnung der Beobachtkarkeitsabbildung:

```
q=ObservabilityMap(f,h,x);
```
Aufruf zur Berechnung der Beobachtbarkeitsmatrix:

```
Q=ObservabilityMatrix(f,h,x);
```

---

Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 288, Algorithmus 6.8**.