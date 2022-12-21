#FunzioneRicorsiva #media_aritmetica #array 
Dato un insieme di $n$ valori $x_1, . . . , x_n$ definiamo la sequente formula per il calcolo ricorsivo della media $$ \begin{cases}	 \overset{\wedge}{x}_1 = x_1 \\  \overset{\wedge}{x}_n = \overset{\wedge}{x}_{n-1} + \frac{x_n - \overset{\wedge}{x}_{n-1}} {n} & \text{per $n>1$}\\	\end{cases}$$
dove $\overset{\wedge}{x}_n$ è la media calcolata quando vediamo l’$n$-esimo elemento, in funzione della media dell’elemento $(n − 1)$-esimo e cosi via.
Scrivere un programma C che dato in input un array di $n$ elementi con i numeri $x_i$, calcoli la loro media usando l’equazione proposta, implementata in maniera ricorsiva.

Suggerimento: Attenzione che l’elemento $i$-esimo di $x$ (cioe $x_i$) corrisponde alla cella $(i − 1)$-esima nel vettore con cui programmate la soluzione. Considerate questo anche per il valore di $n$ nella formula!

Esecuzione:
```c

```