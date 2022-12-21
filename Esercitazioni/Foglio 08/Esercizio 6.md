#array #sposta_di_posizione
Si scriva una funzione che dato un array $𝑎$ di dimensione $𝑛$ e un numero $𝑘 \in ℤ$, ruoti l’array di $𝑘$ posizioni a destra se $𝑘 > 0$ e di $𝑘$ a sinistra se $𝑘 < 0$.

Esempio: Se $𝑎=[0,2,5,1,10,7]$ e: 
- $𝑘= 3$ allora l’output sarà $𝑎=[1,10,7,0,2,5]$
- $𝑘= −2$ allora l’output sarà $𝑎=[5,1,10,7,0,2]$

Esecuzione:
```c
#include <stdio.h>

int absol(int a)
{
	if (a < 0)
		return a * -1;
	return a;
}

void print_array(int a[], int N)
{
	for (int i = 0; i < N; i++)
		printf("%d ", a[i]);
	printf("\n");
}

void rotate_right(int a[], int n, int k)
{
	int j = 1;
	int tmp;
	while (j <= absol(k))
	{
		tmp = a[n - 1]; // salviamo il corrente ultimo elemento
		for (int i = n - 1; i > 0; i--) // rotiamo di 1 verso destra ogni elemento
		{
			a[i] = a[i - 1];
		}
		a[0] = tmp;
		j++;
	}
}

void rotate_left(int a[], int n, int k)
{
	int j = 1;
	int tmp;
	while (j <= absol(k))
	{
		tmp = a[0]; // salviamo il corrente primo elemento
		for (int i = 0; i < n - 1; i++) // rotiamo di 1 verso sinistra ogni elemento
		{
			a[i] = a[i + 1];
		}
		a[n - 1] = tmp;
		j++;
	}
}

void rotate_by_k(int a[], int n, int k)
{
	if (k < 0)
		rotate_left(a, n, k);
	else
		rotate_right(a, n, k);
}

void main()
{
	int a[] = {0, 2, 5, 1, 10, 7};
	int n = 6;
	int k = -2;
	
	rotate_by_k(a, n, k);
	print_array(a, n);
}
```