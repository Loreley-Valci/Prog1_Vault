#array #elementi_ordinati 
Si scriva una funzione che dati due array ordinati $𝑎$ e $𝑏$ di dimensione rispettivamente $𝑛$ ed $𝑚$, li fonda in un unico array ordinato di dimensione $𝑛+𝑚$. La funzione deve ritornare il puntatore al suddetto array.

Esecuzione:
```c
#include <stdio.h>
#include <stdlib.h>

int * merge(int a[], int b[], int n, int m)
{
	int * c = (int *) malloc(sizeof(int) * (n+m));
	int x = 0;
	int y = 0;
	while(x < n || y < m)
	{
		if(x < n && a[x] <= b[y])
		{
			*(c+x+y) = a[x];
			x++;
		}
		
		else
		{
			c[x+y] = b[y];
			y++;
		}
	}
	return c;
}

void main()
{
	int a[] = {1,2,5,6,7};
	int b[] = {0,3,4,8,9};
	
	printf("Array a:\n");
	for(int i = 0; i < 5; i++)
		printf("%d, ",a[i]);
	
	printf("\nArray b:\n");
	for(int i = 0; i < 5; i++)
		printf("%d, ",b[i]);
	
	printf("\nFusione:\n");
	int * c = merge(a,b,5,5);
	for(int i = 0; i < 10; i++)
		printf("%d, ",c[i]);
	printf("\n");
	free(c);
}
```