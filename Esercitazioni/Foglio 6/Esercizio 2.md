#sommatoria #potenza #array
Esercizio 12.1 della dispensa

Si scriva una funzione che prenda in input un array di interi e restituisca la varianza
$$
  S_n = \frac{\sum (x_i - µ)^2} {n}
$$
degli $n$ lementi in esso contenuti; nella formula $x_i$ è l’elemento i-esimo dell’array mentre $µ$ è la media degli elementi dell’array.

Richiesta: La segnatura della funziona sarà: $float var(int a[], int n)$

Esecuzione:
```c
double media(int a[], int n)
{
	double somma = 0;
	for (int i = 0; i < n; i++)
		somma += a[i]; // somma = somma + a[i]
	return (somma / n);
}

double pow2(double n)
{
	return n * n;
}

double varianza(int a[], int n)
{
	double m = media(a, n);
	double num = 0;
	for (int i = 0; i < n; i++)
		num += pow2(a[i] - m);
	return (num / n);
}

// funzione ausiliaria per stampare i valori di un array
void print_array(int a[], int N)
{
	for (int i = 0; i < N; i++)
	printf("a[%d] = %d\n", i, a[i]);
	printf("\n");
}

void main()
{
	int n = 5;
	int a[5] = {1, 2, 3, 4, 5};
	print_array(a, n);
	
	double var = varianza(a, n);
	printf("La varianza dell'array è %f\n", var);
}
```

Oppure

```c
#include <stdio.h>
double media(int *a, int l)
{
	double s = 0;
	for (int i = 0; i < l; i++)
	{
		s += *(a + i);
	}
	return s / l;
}

double pow2(double n)
{
	return n * n;
}

double varianza(int *a, int l)
{
	double av = media(a, l);
	double s = 0;
	for (int i = 0; i < l; i++)
	{
		s += pow2(*(a + i) - av);
	}
	return s / l;
}

// funzione ausiliaria per stampare i valori di un array
void print_array(int a[], int N)
{
	for (int i = 0; i < N; i++)
	printf("a[%d] = %d\n", i, a[i]);
	printf("\n");
}

void main()
{
	int n = 5;
	int a[5] = {1, 2, 3, 4, 5};
	print_array(a, n);
	double var = varianza(a, n);
	printf("La varianza dell'array è %f\n", var);
}
```