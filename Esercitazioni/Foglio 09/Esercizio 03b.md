#lista #malloc 
Si scriva una funzione che date le teste di due liste $π$ e $π$ e un numero $π \in β€$, unisca le due liste nelle seguenti modalitΓ :
- Se $π \le 0$, la lista $π$ deve essere aggiunta in coda alla lista $π$.
- Se $0 < π < π_a$, dove $π_a$ Γ¨ la dimensione della lista $π$, la lista $π$ deve essere aggiunta dopo il $π$-esimo elemento di $π$. Il resto della lista $π$ deve essere aggiunta in coda alla lista $π$.
- Se $π \ge π_a$ , la lista π deve essere aggiunta in coda alla lista $π$.
La funzione deve ritornare la testa della nuova lista.

Esecuzione:
```c
#include <stdio.h>
#include <stdlib.h>

struct elemento
{
	int info;
	struct elemento * next;
};

typedef struct elemento elementoLista;
typedef elementoLista * lista;

elementoLista * add(elementoLista * coda, int n)
{
	elementoLista * nuovo = malloc(sizeof(elementoLista));
	nuovo -> info = n;
	nuovo -> next = NULL;
	coda -> next = nuovo;
	return nuovo;
}

lista create_list()
{
	int n = 0;
	lista testa = NULL;
	printf("Inserisci un numero: ");
	scanf("%d",&n);
	
	if(n == -1)
		return testa;
	elementoLista * nuovo = malloc(sizeof(elementoLista));
	nuovo -> info = n;
	nuovo -> next = NULL;
	testa = nuovo;
	elementoLista * coda = nuovo;
	printf("Inserisci un numero: ");
	scanf("%d",&n);
	while(n != -1)
	{
		/*nuovo = malloc(sizeof(elementoLista));
		nuovo -> info = n;
		nuovo -> next = NULL;
		coda -> next = nuovo;
		coda = nuovo;*/
		coda = add(coda, n);
		printf("Inserisci un numero: ");
		scanf("%d",&n);
	}
	return testa;
}

void print_list(lista a)
{
	if(a == NULL)
		return;
	printf("%d\n",a->info);
	print_list(a->next);
}

int list_length(lista a)
{
	if(a == NULL)
		return 0;
	return 1 + list_length(a->next);
}

elementoLista * merge(lista a, lista b, int j)
{
	if(j <= 0)
	{
		int lunghezza_b = list_length(b);
		elementoLista * coda_di_b = b;
		
		for(int i = 0; i < lunghezza_b - 1; i++)
			coda_di_b = coda_di_b -> next;
		coda_di_b -> next = a;
		return b;
	}
	int lunghezza_a = list_length(a);
	
	if(j >= lunghezza_a)
	{
		elementoLista * coda_di_a = a;
		
		for(int i = 0; i < lunghezza_a - 1; i++)
		coda_di_a = coda_di_a -> next;
		coda_di_a -> next = b;
		return a;
	}
	elementoLista * p = a;
	
	for(int i = 0; i < j - 1; i++)
		p = p -> next;
	elementoLista * resto_di_a = p -> next;
	p -> next = b;
	int lunghezza_b = list_length(b);
	
	for(int i = 0; i < lunghezza_b; i++)
		p = p -> next;
	p -> next = resto_di_a;
	return a;
}

int main(void)
{
	int k = 2;
	printf("Lista a:\n");
	
	lista a = create_list();
	printf("Lista b:\n");
	
	lista b = create_list();
	printf("Lista fusione con k = %d:\n",k);
	print_list(merge(a,b,k));
}
```