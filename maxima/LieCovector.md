---
title: Lie-Ableitung eines Kovektorfeldes
layout: page
mathjax: true
---

Sei $\mathcal{M}\subseteq\mathbb{R}^n$ offen. Die [Lie-Ableitung](https://de.wikipedia.org/wiki/Lie-Ableitung) eines Kovektorfeldes $\omega:\mathcal{M}\to(\mathbb{R}^n)^*$ in Richtung des Vektorfeldes $f:\mathcal{M}\to\mathbb{R}$ ist definiert durch

$$
 L_f\omega(x)=
 \omega(x) f^\prime(x) +
 f^T(x)
 \left(
  \frac{\partial \omega^T(x)}{\partial x}
 \right)^T.
$$

Mehrfache Lie-Ableitungen sind rekursiv durch

$$
L_f^{k+1} \omega(x)= 
L_F \left(L_f^k\omega\right)(x)
\quad\text{mit}\quad
L_f^0\omega(x)=\omega(x)
$$

definiert.

## Berechnung mit Maxima

Das Vektorfeld $f$, das Kovektorfeld $\omega$ und der Vektor $x$ sind als Liste zu übergeben. Der Aufruf ist mit 3 und 4 Argumenten möglich.

```maxima
LieCovector([l]):=block([f,w,x,k,Df,Dw,Lfw],
    if (length(l)<3) or (length(l)>4) then 
       error ("Aufruf mit 3 oder 4 Argumenten."),
    f:l[1],
    w:l[2],
    x:l[3],
    if length(l)=3 then k:1 else k:l[4],
    if not(nonnegintegerp(k)) then 
       error ("Ordnung k muss natürliche Zahl sein."),
    if k=0 then return(w)
    else 
        Df:jacobian(f,x),
        Dw:jacobian(w,x),
        Lfw:list_matrix_entries(w.Df+f.transpose(Dw)),
        return(LieCovector(f,Lfw,x,k-1))
)$
```

Aufruf für Lie-Ableitung $L_f\omega(x)$:

```
LieCovector(f,w,x)
```

Aufruf für Lie-Ableitung $L_f^k\omega(x)$ der Ordnung $k$:

```
LieCovector(f,w,x,k)
```

---

Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 64, Algorithmus 3.3**.