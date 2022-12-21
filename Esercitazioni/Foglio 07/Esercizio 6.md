#array #elementi_non_ordinati #elementi_non_ripetuti
Si scriva una funzione che dato un array $𝑎$ di dimensione $𝑛$ (con elementi non ordinati e non ripetuti) e un numero $𝑘 \in [1, 𝑛]$, ritorni l’elemento $𝑎[𝑖]$ che soddisfa il predicato
$$
	\exists \space a[i] \mid i \in [0,n) \land \mid S_i \mid == k
$$
dove
$$
	S_i =\{j \in [0,n) \mid a[j] \leq a[i]\}
$$
Nota: $\mid S_i \mid$ indica la cardinalità dell’insieme $S_i$.

Esecuzione:
```c
#include <stdio.h> 

int card_Si(float a[], int n, int i)
{
	int c = 0;
	
	for (int j = 0; j < n; j++)
	{
		if (a[j] <= a[i]) c++;
	}
	return c;
}

float my_fun(float a[], int n, int k)
{
	for (int i = 0; i < n; i++)
	{
		if (k == card_Si(a, n, i)) return a[i];
	}
	return 0;
}

void main()
{
	float a[10] = {0,1,2,3,4,5,6,7,8,9};
	
	printf("Res: %f\n", my_fun(a, 10, 8));
}
```