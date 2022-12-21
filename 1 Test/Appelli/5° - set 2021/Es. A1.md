#intersezione #FunzioneIterativa 
Si scriva una funzione iterativa $overlap\_size$ che prenda in input 4 interi positivi $i, j, t, u$ tali per cui $i < j$, $t < u$ e $j \ge t$.
I 4 interi definiscono due intervalli di numeri naturali
$[i, j]$ e $[t, u]$ per cui si vuole calcolare la dimensione dell’intersezione $I = \mid[i, j] \cap [t, u]\mid$.

Per esempio, gli intervalli $[1, 5]$ e $[3, 12]$ hanno sovrapposizione $[3, 5] = {3, 4, 5}$ e quindi dimensione $3$.

Il calcolo della dimensione deve essere fatto iterativamente utilizzando una funzione $is\_inside(x, y, z)$ che restituisce $0$ se $x \in [y, z]$, e $−1$ altrimenti.

Esecuzione: