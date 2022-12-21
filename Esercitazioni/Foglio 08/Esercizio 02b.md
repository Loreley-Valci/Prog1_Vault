#array 
Si scriva una funzione che dato un array $𝑎$ di dimensione $𝑛$, verifichi se l’array soddisfa il predicato 
$$
	\exists \space j \in [0,n) \mid \forall i \in [o,j] \space a[i] \leq j \land  \forall i \in (j,n) \space a[i] > j
$$

Esecuzione:
```c
#include <stdio.h>

int verifica(int a[], int n)
{
	for(int j = 0; j < n; j++)
	{
		int verifica = 1;
		for(int i = 0; i <= j; i++)
			if(a[i] > j)
				verifica = 0;
		for(int i = j + 1; i < n; i++)
			if(a[i] <= j)
				verifica = 0;
		if(verifica == 1)
			return 1;
	}
	return 0;
}

void main()
{
	int a[] = {-4,-8,0,12,3};
	int n = 5;
	if(verifica(a,n) == 1)
		printf("L'array soddisfa il predicato :)\n");
	else
		printf("L'array non soddisfa il predicato :(\n");
}
```