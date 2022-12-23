#array #FunzioneRicorsiva #FunzioneIterativa 
Si consideri la successione $$	F_0=1 \qquad F_1=12 \qquad F_n=3*(F_{n-1}-F_{n-2})+(F_{n-2}-F_{n-1})(n-F_1) \qquad n\ge2$$
e la quantita $$F=\sum^N_{i=1}F-{x_i}$$calcolata a partire da un array $x$ di $N$ valori non negativi $x_1, x_2, . . ., x_N$.
Si scriva un programma C che dato $x$ calcoli $F$ iterativamente e ogni $F_i$ ricorsivamente. Per esempio, se $x = [1, 2, 0]$ allora $F = F_1 + F_2 + F_1$; $F_1$, $F_2$ ed $F_3$ sono ricorsive, il prodotto iterativo.

Suggerimento: Si consideri che Fn sono numeri con la virgola (double).

Esecuzione: