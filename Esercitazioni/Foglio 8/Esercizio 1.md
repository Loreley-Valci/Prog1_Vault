#array #elementi_non_ripetuti #malloc
Si scriva una funzione che dato un array $𝑎$ di dimensione $𝑛$, allochi un array che contiene gli elementi di $𝑎$ senza duplicati. La funzione deve ritornare il puntatore all’array.

Esecuzione:
```c
#include <stdio.h>
#include <stdlib.h>

int quanti_diversi(int * a, int n)
{
	int quanti_diversi = 0;
	for(int i = 0; i < n; i++)
	{
		int diverso = 1;
		for(int j = i - 1; j >= 0; j--)
		{
			if(a[j] == a[i])
				diverso = 0;
		}
		if(diverso == 1)
			quanti_diversi++;
	}
	return quanti_diversi;
}

int * senza_duplicati(int * a, int n)
{
	int q = quanti_diversi(a,n);
	int * b = malloc(sizeof(int) * q);
	int k = 0;
	for(int i = 0; i < n; i++)
	{
		int diverso = 1;
		for(int j = i - 1; j >= 0; j--)
		{
			if(a[j] == a[i])
				diverso = 0;
		}
		if(diverso == 1)
		{
			b[k] = a[i];
			k++;
		}
	}
	return b;
}

int main(void)
{
	int a[] = {1,2,-5,9,-3,2,2,9};
	int n = 7;
	int * b = senza_duplicati(a,n);
	int q = quanti_diversi(a,n);
	printf("Prima:\n");
	
	for(int i = 0; i < n; i++)
		printf("%d, ",a[i]);
	printf("\nDopo:\n");
	
	for(int i = 0; i < q; i++)
		printf("%d, ",b[i]);
	printf("\n");
	return 0;
}
```