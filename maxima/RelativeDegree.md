---
title: Relativer Grad
layout: page
mathjax: true
---

Sei $\mathcal{M}\subseteq\mathbb{R}^n$ offen. 
Durch die Vektorfelder $f,g:\mathcal{M}\to\mathbb{R}^n$ und das Skalarfeld $h:\mathcal{M}\to\mathbb{R}$ wird ein eingangsaffines System

$$
 \dot{x}=f(x)+g(x)u,\quad y=h(x)
$$

beschrieben. Zu berechnen ist der relative Grad.

## Berechnung mit Maxima

Die Vektorfelder $f,g$ und der Vektor $x$ sind jeweils als Liste zu übergeben.

```maxima
RelativeDegree(f,g,h,x):=block([n,r:inf,lie],
    n:length(x),
    for k:1 thru n do (
        lie:ratsimp(LieScalar(g,h,x)),
        if not (lie=0)
        then (r:k, return(r)),
        h:LieScalar(f,h,x) 
    ),
    r
)$
```

Aufruf:

```
r=RelativeDegree(f,g,h,x);
```

Anwendung: [Beispiel 4.4](../kap_4/beispiel4_04.md)

---

Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 116, Algorithmus 4.6**.