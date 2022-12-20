#array #sommatoria #elementi_ordinati 
Si consideri un array $A$ di elemti $a_0, ..., a_{n-1}$ positivi, e la formula
$$
	\sum^k_{i=0}a_i \le w < \sum^{k+1}_{i=0}a_i
$$
dove $w>0$ e $k<n-1$
A. Si scriva una funzione $estrattore$ che, partengono da $A$ e $w$
	- ordini $A$, con un metodo a scelta dello studente;
	- determini, dall'array ordinato, se esiste $k$ che soddisfa l'equazione;
	- se esiste tale $k$, allora restituisca un nuovo array $A_k$ contenente solamente i $k$ elementi ordinati $a_0,....,a_k$;
	- se non esiste tale $k$, allora restituisca l'array $A$ ordinat0.

B. Dato $A=[1\mid3\mid8\mid9]$, si diano:
	- un esempio di $w$ per cui tale $k$ esiste;
	- un esempio di $w$ per cui tale $k$ non esiste

Esecuzione:
