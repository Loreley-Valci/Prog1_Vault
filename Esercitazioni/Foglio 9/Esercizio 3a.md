#lista #unione_liste #malloc 
Si scriva una funzione che date le teste di due liste $𝑎$ e $𝑏$ e un numero $𝑗 \in ℤ$, unisca le due liste nelle seguenti modalità: 
- Se $𝑗 \le 0$, la lista $𝑎$ deve essere aggiunta in coda alla lista $b$. 
- Se $𝑗 > 0$, la lista $𝑏$ deve essere aggiunta in coda alla lista $𝑎$.
La funzione deve ritornare la testa della nuova lista.

Esecuzione:
```c
#include <stdio.h>
#include <stdlib.h>

struct nodo
{
	int info;
	struct nodo * next;
};

typedef struct nodo elementoLista;
typedef elementoLista * lista;

lista crea_lista()
{
	lista a = NULL;
	int n;
	printf("Inserisci un numero: ");
	scanf("%d",&n);
	if(n == -1)
		return a;
	elementoLista * nuovo = malloc(sizeof(elementoLista));
	nuovo -> info = n;
	nuovo -> next = NULL;
	a = nuovo;
	elementoLista * coda;
	coda = nuovo;
	printf("Inserisci un numero: ");
	scanf("%d",&n);
	while(n != -1)
	{
		nuovo = malloc(sizeof(elementoLista));
		nuovo -> info = n;
		nuovo -> next = NULL;
		coda -> next = nuovo;
		coda = nuovo;
		printf("Inserisci un numero: ");
		scanf("%d",&n);
	}
	return a;
}

void stampa_lista(lista a)
{
	if(a == NULL)
		return;
	printf("%d\n",a -> info);
	stampa_lista(a->next);
}

lista unisci(lista a, lista b, int j)
{
	if(j <= 0)
	{
		lista testa_b = b;
		while(b -> next != NULL)
			b = b -> next;
		b -> next = a;
		return testa_b;
	}
	lista testa_a = a;
	while(a -> next != NULL)
		a = a -> next;
	a -> next = b;
	return testa_a;
}

void main()
{
	printf("Lista a:\n");
	lista a = crea_lista();
	printf("\nLista b: \n");
	lista b = crea_lista();
	int k = 2;
	printf("\nLista fusione con k = %d\n", k);
	stampa_lista(unisci(a,b,k));
}
```