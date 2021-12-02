---
title: Test einer Distribution auf Involutivität
layout: page
mathjax: true
---

Sei $\mathcal{M}\subseteq\mathbb{R}^n$ offen. 
Die von den Vektorfeldern $f_1,\ldots,f_r:\mathcal{M}\to\mathbb{R}^n$ aufgespannte Distribution

$$
 \Delta=\operatorname{span}
 \lbrace
  f_1,\ldots,f_r
 \rbrace
$$

wird auf Involutivität überprüft.

## Berechnung mit Maxima

Die die Distribution aufspannenden Vektorfelder sind als Liste zu übergeben,

```maxima
Involutivep(L,x):=block([F,G,i,j,r],
    r:length(L),
    F:apply('matrix,L),
    F:transpose(F),
    G:copy(F),  
    for i:1 thru r do 
        for j:i+1 thru r do block([f1,f2],
            f1:list_matrix_entries(col(F,i)),
            f2:list_matrix_entries(col(F,j)),
            G:addcol(G,LieBracket(f1,f2,x))
    ),
    is(rank(F)=rank(G))
)$
```

Aufruf:

```
Involutivep([f1,...,fr],x)
```

---

Klaus Röbenack:
[*Nichtlineare Regelungssysteme - Theorie und Anwendung der exakten Linearisierung.*](https://link.springer.com/book/10.1007/978-3-662-44091-9)   
Springer Vieweg, 2017, **S. 84, Algorithmus 3.4**.