#successione 
Si implementi una funzione che calcola la seguente successione fino al termine $n$-esimo:
$$
  a_{n+1_p} = 
  \begin{cases}
  p & \text{se $n = 1$} \\
  \frac{1}{2}(a_{n,p}+\frac{p}{a_{n,p}}) & \text{se $n > 1$} \\
 \end{cases}
$$
Verificare che il limite della successione è $\sqrt{𝑝}$.

Esecuzione:
```c
#include <stdio.h>
#include <math.h>

double a_n(unsigned int n, double p)
{ // dobbiamo avere due parametri: p ed n
	double a_i = p; // il primo termine della successione
	printf("a_1 = %.7lf\n", a_i);
	for(int i = 2; i <= n; i++)
	{
		a_i = 0.5 * (a_i + p/a_i); // il nuovo valore della successione è calcolato seguendo la formula
		printf("a_%d = %.7lf\n", i, a_i);
	}
}

int main()
{
	double p;
	int n;
	printf("Dammi il valore di p: ");
	scanf("%lf", &p);
	
	printf("Dammi il valore di n: ");
	scanf("%d", &n);
	a_n(n,p); // testiamo a_n con n grande
	
	printf("Radice di p: %lf",sqrt(p)); // confrontiamo il risultato con la radice di p
}
```