#sommatoria #array 
Si scriva una funzione che dato un array $๐$ di dimensione $๐$, calcoli
$$
	{\sum}_{i \in I} a[i]
$$
dove 
$$
	I = \{๐ \in [0, ๐) \mid ๐[๐] \space \%2 == 0\}
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

int check_pari(int n)
{
	if (n % 2 == 0)
		return 1;
	return 0;
}

int sum_pari(int a[], int n)
{
	int somma = 0;
	for (int i = 0; i < n; i++)
	{
		if (check_pari(a[i]))
			somma += a[i];
	}
	return somma;
}

void main()
{
	int n = 5;
	int a[5];
	init_array(a, n);
	
	int somma = sum_pari(a, n);
	printf("La somma degli elementi pari รจ %d\n", somma);
}
```