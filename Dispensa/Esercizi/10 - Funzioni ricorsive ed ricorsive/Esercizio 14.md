
Si consideri la _sequenza di Hailstone_: si parta da un intero $n > 0$
- Si generi il prossimo numero m della sequenza come segue:
	- se $n$ è pari, allora $m = \frac{n}{2}$;
	- altrimenti, $m = 3n + 1$;
- Si ripeta fino a che non si genera $m = 1$;
- Si conti la lunghezza della sequenza generata.

Si utilizzino due funzioni - sequenza e lunghezza - per la definizione della suddetta sequenza a partire da un intero $n > 0$ ricevuto in input dall’utente.

Esecuzione: