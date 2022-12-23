#array #sommatoria #successione #FunzioneIterativa #FunzioneRicorsiva 
Si consideri la successione $$	F_0=1 \qquad F_1=100 \qquad F_n=nF_{n-1}-\frac{nF-{n-2}}{2} \qquad n\ge2$$
e la quantita $$F=\sum^N_{i=0}F-{x_i}$$calcolata a partire da un array $x$ di $N$ valori negativi $x_i, ..., x_N$.
Si scriva un programma C che dato $x$ calcoli $F$ iterativamente e ogni $F_i$ ricorsivamente. Per esempio, se $x = [1, 2, 0]$ allora $F = F_1 + F_2 + F_1$; $F_1$, $F_2$ ed $F_1$ sono ricorsive, il prodotto iterativo.

Suggerimento: Si consideri che $F_n$ sono numeri con la virgola (double).

Esecuzione: