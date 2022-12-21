#intersezione #FunzioneIterativa 
Si scriva una funzione iterativa $overlap\_size$ che prenda in input 4 interi positivi $i, j, t, u$ tali per cui $i < j$, $t < u$ e $j \ge t$. I 4 interi definiscono due intervalli di numeri naturali $I=[i,j]$ e $J=[t,u]$ per cui si vuole calcolare la dimensione dell'insieme $$\overset{-}{I}=\mid\{x\in I,x \notin J\} \space \cup \space \{x\notin I,x \in J\} \mid $$
Per esempio: gli intervalli $[1,5]$ e $[3,12]$ hanno sovrapposizione $\overset{-}{I}=\{1,2\} \space \cup \space \{6,7,8,9,10,11,12\}$ e quindi dimensione $9$.

Il calcolo della dimensione deve essere fatto iterativamente utilizzando una funzione $is\_inside(x, y, z)$ che restituisce
$0$ se $x \in [y, z]$, e $−1$ altrimenti.

Esecuzione: