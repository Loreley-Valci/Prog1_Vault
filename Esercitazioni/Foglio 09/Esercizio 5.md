#lista #malloc 
Si scriva una funzione che data la testa di una lista di numeri interi $𝑎$ e un numero $𝑘 \in [0, 𝑛_a )$, dove $n_a$ è la dimensione della lista, ritorni la testa della sotto-lista a partire dall’elemento $𝑘$-esimo.

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

lista sublist(elementoLista *head, int k)
{
	int c = 0;
	while (c < k)
	{
		head = head->next;
		c++;
	}
	return head;
}

int main(void)
{
	lista a = create_list();
	int k = 3;
	lista sub = sublist(a, k);
	print_list(sub);
}
```