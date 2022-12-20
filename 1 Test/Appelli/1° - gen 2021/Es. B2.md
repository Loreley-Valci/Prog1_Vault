#array 
Si consideri questa formula logica $\exists i \in {0,...,3}$  $a[a[i]] == 0$ ed il seguente frammento di programma C, supponendo che la dichiarazione ed inizializzazione dell'array a di 4 elementi avvenga correttamente nella porzione di codice mancante $[...]$.
```c
int b[4];
for(int i = 1; i <= 4; i++)
{
	b[i-1] = a[i-1];
	b[i-1] -= a[a[i-1]];
	if(b[i-1] == 0) return(1);
}
return(0);
```
- si fornisca un esempio dei valori del vettore a per cui il predicato dovrebbe essere falso;
- si fornisca un esempio dei valori del vettore a per cui il predicato dovrebbe essere vero;
- si riscriva la parte di codice mostrata usando tutti questi meccanismi:

	-> un ciclo while;
	–> eliminando il return da dentro il corpo del for;
	–> eliminando l’inutile utilizzo di indici strani dentro il ciclo.

Esecuzione:
```c

```