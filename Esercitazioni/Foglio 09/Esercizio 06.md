#lista #elementi_non_ripetuti #malloc 
Si scriva una funzione che data la testa di una lista di numeri interi $𝑎$, elimini i nodi con valore duplicato.

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

void rimuovi_dup(elementoLista *head)
{
	elementoLista *ptr1, *ptr2, *dup;
	ptr1 = head;
	// ptr1 e ptr2 sono due elementi della lista che vengono confrontati
	while (ptr1 != NULL && ptr1->next != NULL)
	{
		ptr2 = ptr1;
		// per ogni ptr1, controllo rispetto a ptr2, fino all'ultimo elemento
		while (ptr2->next != NULL)
		{
			// se trovo un duplicato
			if (ptr1->info == ptr2->next->info)
			{
				// lo rimuovo, ptr2->next è l'elemento duplicato
				dup = ptr2->next;
				// ptr2->next deve diventare l'elemento dopo dup
				ptr2->next = ptr2->next->next;
				// libero dup
				free(dup);
			}
			
			else
				// se non è un duplicato, vado avanti di un elemento
				ptr2 = ptr2->next;
		}
		// vado avanti anche con ptr1
		ptr1 = ptr1->next;
	}
}

void main()
{
	lista a = create_list();
	
	printf("Inserire i valori per creare una lista\n");
	print_list(a);
	rimuovi_dup(a);
	
	printf("Lista dopo aver rimosso i duplicati\n");
	print_list(a);
}
```