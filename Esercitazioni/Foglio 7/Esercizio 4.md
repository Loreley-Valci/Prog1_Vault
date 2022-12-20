#sommatoria #array 
Si scriva una funzione che dati due array 𝑎 e 𝑏 di dimensione rispettivamente 𝑛 ed 𝑚, verifichi il seguente predicato
$$
	\exists \space 𝑖 \in [0, 𝑛) \mid a[i] = \sum^m_{j=0} 𝑏[𝑗]
$$

Esecuzione:
```c
#include <stdio.h>

void init_array(int a[], int n)
{
	for (int i = 0; i < n; i++)
	{
		printf("a[%d] = ", i);
		scanf("%d", &a[i]);
	}
}

// funzione per calcolare la somma degli elementi in un array
int somma(int a[], int dim)
{
	int s = 0;
	for (int i = 0; i < dim; i++)
		s += a[i];
	return s;
}

int check(int a[], int n, int b[], int m)
{
	int i = 0;
	int trovato = 0;
	int somma_b = somma(b, m);
	// controllo fino a che non trovo un elemento che soddisfi la proposizione
	// al più controllo tutti gli elementi di a
	while (i < n && !trovato)
	{
		if (a[i] == somma_b) // se trovo un elemento in a uguale alla somma degli elementi in b
			trovato = 1; // aggiorno trovato
		i++; // aggiorno il contatore
	}
	return trovato;
}

void main()
{
	int n = 5;
	int m = 3;
	int a[5];
	int b[3];
	
	init_array(a, n);
	init_array(b, m);
	int verifica = check(a, n, b, m);
	
	if (verifica == 1)
	{
		printf("In a esiste un elemento uguale alla somma degli elementi di b\n");
	}
	
	if (verifica == 0)
	{
		printf("In a NON esiste un elemento uguale alla somma degli elementi di b\n");
	}
}
```