#array #elementi_ordinati
Si scriva una funzione che dato un array $𝑎$ di dimensione $𝑛$ e un numero $𝑘$, riordini l’array in modo che soddisfi il predicato
$$
	\exists \space j \in [0,n) \mid \forall i \in [0,j] \space a[i] \leq k \land \forall i \in (j,n) \space a[i]>k
$$

Esecuzione:
```c
#include <stdio.h>

void swap(int * a, int * b)
{
	int tmp = *a;
	*a = *b;
	*b = tmp;
}

void partition(int a[], int n, int k)
{
	int i = 0;
	int j = n-1;
	while(i<j)
	{
		if(a[i] >= k)
		{
			swap(a+i, a+j);
			j--;
		}
		else
			i++;
	}
}

void main()
{
	int a[] = {1,3,9,-2,8,18};
	partition(a,6,7);
	for(int i = 0; i < 6; i++)
		printf("%d, ", a[i]);
	printf("\n");
}
```