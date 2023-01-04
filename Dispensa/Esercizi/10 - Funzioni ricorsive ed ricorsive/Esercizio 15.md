#base_decimale #base_binaria 
Vogliamo convertire un numero da una base numerica all’altra. L’algoritmo per convertire un intero $n > 0$ da base decimale a base binaria è il seguente:
	1. Calcolare la divisione intera $n' = \frac{n}{2}$ con resto $r'$;
	2. $r'$ è la cifra più a destra nella rappresentazione binaria di $n$, chiamiamolo $c_0$;
	3. Si divide ancora $n'' = \frac{n'}{2}$ con resto $r''$ ed otteniamo la seconda cifra $r'' = c1$;
	4. Si ripete il procedimento fino a quando il risultato della divisione è uguale a $0$, ottenendo la rappresentazione binaria di $n$ concatenando le cifre $c_i$ come $c_k c_{k−1} · · · c_0$.

Mentre l’algoritmo inverso si basa sul fatto che che $n = c_02^0 + c_12^1 + . . . c_k2^k$
- Scrivere una funzione che, preso in input un numero intero in base decimale, lo converta in base binaria;
- Scrivere la funzione di conversione inversa;
- Testare le funzioni cosi definite sui numeri da 1 a 100.

Esempio: di output (su un sotto-insieme di valori)
	b10 -> b2 -> b10   -   0 ->    0    -> 0
	b10 -> b2 -> b10   -   1 ->   01   -> 1
	b10 -> b2 -> b10   -   2 ->   10   -> 2
	b10 -> b2 -> b10   -   3 ->  011  -> 3
	b10 -> b2 -> b10   -   4 ->  100  -> 4

Nota: Non sapendo ancora come memorizzare sequenze di bits 0/1 di lunghezza arbitraria, si consideri che per convertire un numero $< 100$ in binario servono al più $log_2(100)$ bits.

Esecuzione: