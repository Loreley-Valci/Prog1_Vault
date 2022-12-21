#lista #elementi_ordinati #malloc 
Si scriva una funzione che data la testa di una lista di numeri interi ordinata $𝑎$ e un numero $𝑘 \in ℤ$, inserire un nuovo nodo con valore $𝑘$ in modo da mantenere la lista ancora ordinata.

Esecuzione:
```c
#include <stdio.h>
#include <stdlib.h>

struct elemento
{
	int info;
	struct elemento *next;
};
  
typedef struct elemento elementoLista;
typedef elementoLista *lista;

elementoLista *add(elementoLista *coda, int n)
{
	elementoLista *nuovo = malloc(sizeof(elementoLista));
	nuovo->info = n;
	nuovo->next = NULL;
	coda->next = nuovo;
	
	return nuovo;
}

lista create_list()
{
	int n = 0;
	lista testa = NULL;
	printf("Inserisci un numero: ");
	scanf("%d", &n);
	
	if (n == 123)
		return testa;
	
	elementoLista *nuovo = malloc(sizeof(elementoLista));
	nuovo->info = n;
	nuovo->next = NULL;
	testa = nuovo;
	elementoLista *coda = nuovo;
	printf("Inserisci un numero: ");
	scanf("%d", &n);
	
	while (n != -1)
	{
		coda = add(coda, n);
		printf("Inserisci un numero: ");
		scanf("%d", &n);
	}
	
	return testa;
}

void print_list(lista a)
{
	if (a == NULL)
		return;
	
	
	printf("%d\n", a->info);
	print_list(a->next);
}
  
lista add_ordered(lista l, int k)
{
	// elementoLista head = *l;
	// printf("%d\n", l->info);
	lista current = l;
	
	if(current->info >= k)
	{ // se devo aggiungere l'elemento in testa alla lista
		elementoLista *new_elem = malloc(sizeof(elementoLista));
		new_elem->info = k;
		new_elem->next = current;
		
		return new_elem;
	}
	while (current->next != NULL)
	{
		if (current->info < k && current->next->info >= k)
		{ // se devo aggiungerlo in mezzo
			elementoLista *new_elem = malloc(sizeof(elementoLista));
			new_elem->info = k;
			new_elem->next = current->next;
			current->next = new_elem;
			
			return l;
		}
		current = current->next;
		
		if(current->next == NULL)
		{ // se devo aggiungerlo alla fine
			add(current,k);
			return l;
		}
	}
	return l;
}

void main(void)
{
	int k = 5;
	lista L = create_list(); // assumo di creare una lista ordinata
	
	L = add_ordered(L, k);
	print_list(L);
}
```