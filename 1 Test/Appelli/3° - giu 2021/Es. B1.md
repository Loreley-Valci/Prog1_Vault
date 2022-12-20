#lista #array #FunzioneRicorsiva 
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
ListaDiElementi init(int n)
void print(ListaDiElementi lista)
```
dove:
- $i) init$ costruisce una lista di un singolo elemento, il quale contiene un array di $n > 0$ elementi;
- $ii) print$ stampa ricorsivamente la lista, mostrando ad esempio (dopo la init)
```c
ListaDiElementi list = init(4);

print_list(list);
// -> n = 4 | 0, 0, 0, 0,

list->next = init(12);

print_list(list);
// -> n = 4 | 0, 0, 0, 0,
// -> n = 12 | 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, %
```

Suggerimento: Se gli array hanno dimensione variabile, la gestione della memoria deve essere esplicita.

Esecuzione:
```c

```