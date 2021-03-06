---
title: Involutiver Abschluss einer Distribution
layout: page
mathjax: true
---

Sei $\mathcal{M}\subseteq\mathbb{R}^n$ offen. 
Zu der von den Vektorfeldern $f_1,\ldots,f_r:\mathcal{M}\to\mathbb{R}^n$ aufgespannten Distribution

$$
 \Delta=\operatorname{span}
 \lbrace
  f_1,\ldots,f_r
 \rbrace
$$

wird der involutive Abschluss $\operatorname{inv}(\Delta)$ berechnet.

## Berechnung mit Maxima

Die die Distribution aufspannenden Vektorfelder sind als Liste zu übergeben,

```maxima
InvolutiveClosure(L,x):=block([flag,F,G,i,j,r,n],
    F:apply('matrix,L),
    F:transpose(F),
    flag:true,
    while flag do (
        flag:false,
        [n,r]:matrix_size(F),
        for i:1 thru r do 
            for j:i+1 thru r do block([f1,f2],
                f1:list_matrix_entries(col(F,i)),
                f2:list_matrix_entries(col(F,j)),
                G:addcol(F,LieBracket(f1,f2,x)),
                if rank(F)<rank(G) then (
                    F:copy(G),
                    flag:true
                )       
        )
    ),
    makelist(makelist(F[i,j],i,1,n),j,1,r)
)$
```

Aufruf:

```
InvolutiveClosure([f1,...,fr],x)
```

---

Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 94, Algorithmus 3.5**.
