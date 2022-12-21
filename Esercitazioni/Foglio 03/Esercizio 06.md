#successione 
Si implementi una funzione che calcola la seguente successione fino al termine $n$-esimo:
$$
  a_n = 
  \begin{cases}
  \frac{1}{2} & \text{se $n = 1$}\\
  \frac{a_{n-1}+1}{2} &\text{altrimenti}\\
  \end{cases}
$$
Verificare che il limite della successione è $1$.

Esecuzione:
```c
#include <stdio.h>

double a_n(unsigned int n)
{
	double a_i = 0.5; // valore di partenza
	printf("a_1 = %.7lf\n", a_i);
	for(int i = 2; i <= n; i++)
	{ // dobbiamo calcolare la successione fino ad arrivare al termine n-esimo
		a_i = (a_i + 1)/2; // il nuovo valore sarà calcolato secondo la formula
		printf("a_%d = %.7lf\n", i, a_i);
	}
	return a_i;
}

int main()
{
	int n;
	printf("Dammi il valore di n: ");
	scanf("%d", &n);
	a_n(n); // testiamo n molto grande per vedere se converge ad 1
}
```