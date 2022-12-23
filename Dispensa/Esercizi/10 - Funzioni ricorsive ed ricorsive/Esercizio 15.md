#base_decimale #base_binaria 
Vogliamo convertire un numero da una base numerica all’altra. L’algoritmo per convertire un intero $n > 0$ da base decimale a base binaria è il seguente:
1. Calcolare la divisione intera $n' = \frac{n}{2}$ con resto $r'$;
2. $r'$ è la cifra più a destra nella rappresentazione binaria di $n$, chiamiamolo $c_0$;
3. Si divide ancora $n'' = \frac{n'}{2}$ con resto $r''$ ed otteniamo la seconda cifra $r'' = c1$;
4. Si ripete il procedimento fino a quando il risultato della divisione è uguale a $0$, ottenendo la rappresentazione binaria di $n$ concatenando le cifre $c_i$ come $c_k c_{k−1} · · · c_0$.

Mentre l’algoritmo inverso si basa sul fatto che che

n = c020 + c121 + . . . c_k_2_k_