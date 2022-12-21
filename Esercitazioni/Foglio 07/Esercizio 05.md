#array #sommatoria 
Un numero è triangolare se è uguale alla somma dei primi $n$ numeri naturali; per esempio, 10 è triangolare dal momento che è uguale alla somma dei primi 4 numeri naturali. Scrivere una funzione che dato un array $𝑎$ di dimensione $𝑛$, inserisca nell’array i primi $𝑛$ numeri  triangolari.
Fun fact: si chiamano triangolari dal momento che preso un insieme con una cardinalità uguale al numero in oggetto, è possibile disporre i suoi elementi su una griglia regolare, in modo da formare un triangolo equilatero o isoscele.

![[Esercitazioni/Foglio 07/Esercizio 05.img1.jpg]]

Esecuzione:
```c
#include <stdio.h>

void triang(int a[], int n)
{
	int tmp;
	for (int i = 0; i < n; i++)
	{
		tmp = 0;
		for (int j = 1; j <= i; j++)
			tmp += j;
		a[i] = tmp;
	}
}

void print_array(int a[], int N)
{
	for (int i = 0; i < N; i++)
		printf("%d ", a[i]);
	printf("\n");
}
  
void main()
{
	int n = 10;
	int a[10];
	
	triang(a, n);
	
	print_array(a, n);
}
```