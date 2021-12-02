---
title: Steuerbarkeitsmatrix
layout: page
mathjax: true
---

Sei $\mathcal{M}\subseteq\mathbb{R}^n$ offen. 
Durch die Vektorfelder $f,g:\mathcal{M}\to\mathbb{R}^n$ wird ein eingangsaffines System

$$
 \dot{x}=f(x)+g(x)u
$$

beschrieben. Zu berechnen ist die Steuerbarkeitsmatrix

$$
 Q_S(x)=
 \begin{pmatrix}
  g(x) &
  \operatorname{ad}_{-f} g(x) &
  \cdots &
  \operatorname{ad}_{-f}^{n-1} g(x)
 \end{pmatrix}.
$$

## Berechnung mit Maxima

Die Vektorfelder $f,g$ und der Vektor $x$ sind jeweils als Liste zu übergeben.

```maxima
ControllabilityMatrix(f,g,x):=block([i,n,L],
    n:length(x),
    if length(f)#n then
        error("Dimensionen von f und x müssen übereinstimmen."),
    if length(g)#n then
        error("Dimensionen von g und x müssen übereinstimmen."),
    L:makelist(LieBracket(-f,g,x,i),i,0,n-1),
    transpose(apply(matrix,L))
    )$
```

Aufruf:

```
Q=ControllabilityMatrix(f,g,x)
```

---

Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 153, Algorithmus 4.7**.