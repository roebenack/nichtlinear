---
title: Lie-Ableitung eines Skalarfeldes
layout: page
mathjax: true
---

Sei $\mathcal{M}\subseteq\mathbb{R}^n$ offen. Die [Lie-Ableitung](https://de.wikipedia.org/wiki/Lie-Ableitung) eines Skalarfeldes $h:\mathcal{M}\to\mathbb{R}$ in Richtung des Vektorfeldes $f:\mathcal{M}\to\mathbb{R}$ ist definiert durch

$$
 L_fh(x)=h^\prime(x) \, f(x).
$$

Mehrfache Lie-Ableitungen sind rekursiv durch

$$
L_f^{k+1} h(x)=\frac{\partial L_f^kh(x)}{\partial x} f(x)
\quad\text{mit}\quad
L_f^0h(x)=h(x)
$$

definiert.

## Berechnung mit Maxima

Das Vektorfeld $f$ und der Vektor $x$ sind als Liste zu übergeben. Der Aufruf ist mit 3 und 4 Argumenten möglich.

```maxima
LieScalar([l]):=block([f,h,x,k,Lfh],
    if (length(l)<3) or (length(l)>4) then 
       error ("Aufruf mit 3 oder 4 Argumenten."),
    f:l[1], /* Vektorfeld */
    h:l[2], /* Skalarfeld */
    x:l[3], /* Variable   */
    if length(l)=3 then k:1 else k:l[4],
    if not(nonnegintegerp(k)) then 
       error ("Ordnung k muss natürliche Zahl sein."),
    if k=0 then return(h)
    else 
        Lfh:jacobian([h],x).f,
        return(LieScalar(f,Lfh,x,k-1))
)$
```

Aufruf für Lie-Ableitung $L_fh(x)$:

```
LieScalar(f,h,x)
```

Aufruf für Lie-Ableitung $L_f^kh(x)$ der Ordnung $k$:

```
LieScalar(f,h,x,k)
```

Anwendung: [Beispiel 3.3](../kap_3/beispiel3_03.md)

---

Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 47, Algorithmus 3.1**.