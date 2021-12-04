---
title: Maxima-Routinen
layout: page
permalink: maxima
mathjax: true
---

Die wichtigsten Routinen zur Analyse und Regelung nichtlinearer Systeme wurden in einer Biblothek für das Open-Source-Computer-Algebra-System [Maxima](https://maxima.sourceforge.io/) zusammengefasst: [nl.mac](nl.mac) 

Nach dem Herunterladen kann man diese Bibliothek folgendermaßen in Maxima-Programme einbetten:

```maxima
load("nl.mac")
```

|Routinen|Seite(n)|Algorithmus|
|---|---|---|
|[Lie-Ableitung eines Skalarfeldes](LieScalar.md)|S. 47|Algorithmus 3.1|
|[Lie-Ableitung eines Vektorfeldes](LieBracket.md)|S. 56|Algorithmus 3.2|
|[Lie-Ableitung eines Kovektorfeldes](LieCovector.md)|S. 64|Algorithmus 3.3
|[Test einer Distribution auf Involutivität](Involutivep.md)|S. 84|Algorithmus 3.4|
|[Involutiver Abschluss einer Distribution](InvolutiveClosure.md)|S. 94|Algorithmus 3.5|
|[Relativer Grad](RelativeDegree.md)|S. 116|Algorithmus 4.6|
|[Steuerbarkeitsmatrix](ControllabilityMatrix.md)|S. 153|Algorithmus 4.7|
|[Beobachtbarkeitsabbildung und -matrix](ObservabilityMatrix.md)|S. 288|Algorithmus 6.8|

Zum Einstieg in dieses Computer-Algebra-System [Maxima](https://maxima.sourceforge.io/) bzw. [wxMaxima](http://wxmaxima-developers.github.io/wxmaxima/index.html) ist folgendes Buch empfehlenswert:

> Wilhelm Haager:   
> [*Computeralgebra mit Maxima
Grundlagen der Anwendung und Programmierung*](https://www.hanser-elibrary.com/isbn/9783446448681).   
> Carl Hanser Verlag GmbH & Co. KG, 2. Auflage, 2019. ISBN: 978-3-446-44868-1
