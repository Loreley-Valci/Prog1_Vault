#lista #array 
In C, si vogliono definire liste linkate che possono memorizza un array di interi in ciascun loro elemento; si desidera inoltre permettere agli array di avere dimensione variabile, e.g., una lista potrebbe essere $$[{1,2,3}] -> [{9}] -> [{43, 5}] \space // array \space di \space 3, \space 1 \space e \space 2 \space elementi$$
Si usi il sequente template per definire la struct necessaria ad implementare la lista.
```c
// struttura
struct elemento
{
	// dato memorizzato
	...
	// puntatore
	struct elemento * next;
};

// tipi
typedef struct elemento ElementoDiLista;
typedef ElementoDiLista * ListaDiElementi;
```
Si definiscano, secondo la struct sopra definita, le funzioni
```c
int ntot(ListaDiElementi lista)
int largest(ListaDiElementi lista)
```
dove:
- $i) ntot$ restitutisce il numero totale degli elementi inseriti nella lista (somma del numero di elementi in ciascun array contentuto)
- $ii) largest$ che restituisce il numero massimo di elementi contenuti in un elemento delle lista.

Ad esempio (dopo la init)
```c
// supponendo si crei una lista di un singolo array con 4 elementi, usando
// un metodo "init"
ListaDiElementi list = init(4);

// si aggiunge un secondo elemento, stavolta con un array di 12 elementi
list->next = init(12);

// a questo punto avremmo
// - ntot(list) che restituisce 12 + 4 = 16
// - largest(list)che restituisce 12
```

Esecuzione:
```c

```