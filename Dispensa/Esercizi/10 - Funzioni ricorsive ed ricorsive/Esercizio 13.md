#fibonacci 
Si consideri la _successione di Fibonacci_ $$ F_n = \begin{cases} 1 & \text{se $n = 1$} \\ 1 & \text{se $n = 2$} \\ F_{n-1} + F_{n-2} & \text{altrimenti} \\ \end{cases}$$definita per $n > 0$ intero.
- Si implementi la definizione iterativa per il calcolo di $F_n$;
- Si implementi la definizione ricorsiva per il calcolo di $F_n$;
- Si crei un programma che testa le due versioni per i valori di input che vanno da 1 a 10 (incluso).
- Si testino entrambe le funzioni per $n = 100$, e si provi a spiegare il comportamento osservato.

Esempio: di output (su un sotto-insieme di valori).
	Fibonacci   ricorsivo/iterativo    1: 1/1
	Fibonacci   ricorsivo/iterativo    2: 1/1
	Fibonacci   ricorsivo/iterativo    3: 2/2

Esecuzione: