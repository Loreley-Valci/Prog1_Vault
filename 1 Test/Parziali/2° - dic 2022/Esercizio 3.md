#lista #array
Si consideri la definizione di liste linkate vista a lezione, e si risolvano le seguenti operazioni:

A. La lista deve poter memorizzare, invece di singoli interi $(int info)$, un array di valori in ciascun elemento, con una dimensione variabile per ogni elemento della lista;

B. si crei una funzione $initialise$ che:
	- prenda in input $n\ge1$ e $z\le1$;
	- crei una lista di $n$ elementi, dove l'elemento $x$-esimo contiene l'array dei primi $x$ numeri maggiori strettamente di $z$.

Per esempio: per $z=10$ ed $n=3$ vale $$ initialise(3, \space 10)=[11] --> [11\mid 12] --> [11 \mid 12 \mid 13]$$
C. Si disegni la memoria vera dopo aver eseguito $initialise(3, 10)$ in un vostro programma.

Esecuzione: