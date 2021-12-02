---
title: Lie-Ableitung eines Vektorfeldes
layout: page
mathjax: true
---

Sei $\mathcal{M}\subseteq\mathbb{R}^n$ offen. Die [Lie-Ableitung](https://de.wikipedia.org/wiki/Lie-Ableitung) eines Vektorfeldes $g:\mathcal{M}\to\mathbb{R}^n$ in Richtung des Vektorfeldes $f:\mathcal{M}\to\mathbb{R}$ wird auch als [Lie-Klammer](https://de.wikipedia.org/wiki/Lie-Klammer) der Vektorfelder $f,g:\mathcal{M}\to\mathbb{R}$ bezeichnet. Sie ist definiert durch

$$
 [f,g](x)= g^\prime(x)f(x)-f^\prime(x)g(x).
$$

Mehrfache Lie-Klammern sind rekursiv durch

$$
\operatorname{ad}^{k+1}_f g(x)=
[f,\operatorname{ad}^{k}_f g](x)
\quad\text{mit}\quad
\operatorname{ad}^0_f g(x)=g(x)
$$

definiert.

## Berechnung mit Maxima

Die Vektorfeld $f$ und $g$ sowie der Vektor $x$ sind als Liste zu übergeben. Der Aufruf ist mit 3 und 4 Argumenten möglich.

```maxima
LieBracket([l]):=block([f,g,x,k,Df,Dg,ad],
    if (length(l)<3) or (length(l)>4) then 
       error ("Aufruf mit 3 oder 4 Argumenten."),
    f:l[1],
    g:l[2],
    x:l[3],
    if length(l)=3 then k:1 else k:l[4],
    if not(nonnegintegerp(k)) then 
       error ("Ordnung k muss natürliche Zahl sein."),
    if k=0 then return(g)
    else 
        Df:jacobian(f,x),
        Dg:jacobian(g,x),
        ad:list_matrix_entries(Dg.f-Df.g),
        return(LieBracket(f,ad,x,k-1))
)$
```

Aufruf für Lie-Ableitung $L_fh(x)$:

```
LieBracket(f,g,x)
```

Aufruf für Lie-Ableitung $L_f^kh(x)$ der Ordnung $k$:

```
LieBracket(f,g,x,k)
```

---

Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 56, Algorithmus 3.2**.