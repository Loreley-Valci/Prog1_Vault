#lista #malloc 
Si scriva una funzione che data la testa di una lista di numeri interi $𝑎$ ritorni la testa della lista invertita, ossia i nodi sono collegati in ordine inverso, dall’ultimo al primo.

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
		/*nuovo = malloc(sizeof(elementoLista));
		nuovo -> info = n;
		nuovo -> next = NULL;
		coda -> next = nuovo;
		coda = nuovo;*/
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
  
int list_length(lista a)
{
	if (a == NULL)
		return 0;
	return 1 + list_length(a->next);
}

elementoLista *find_last(elementoLista *head)
{
	while (head->next != NULL)
		head = head->next;
	return head;
}

lista invert(elementoLista *head)
{
	elementoLista *pred = head;
	elementoLista *current = head->next;
	head = head->next;
	pred->next = NULL; // il primo nodo diventa l'ultimo
	
	while (head != NULL)
	{
		head = head->next;
		current->next = pred;
		// valutiamo i due elementi successivi
		pred = current;
		current = head;
	}
	head = pred; // l'ultimo nodo diventa il primo
	return head;
}

void main()
{
	lista a = create_list();
	printf("Lista originale.\n");
	print_list(a);
	
	printf("Lista invertita.\n");
	lista b = invert(a);
	print_list(b);
}
```