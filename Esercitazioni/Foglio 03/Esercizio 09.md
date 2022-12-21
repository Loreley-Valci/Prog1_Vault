#sommatoria #serie 
Implementare una funzione che calcoli il termine $𝑛$-esimo della serie
$$
	S_n = \sum_{i=1}^{n}\frac{i*k^{i+1}}{3^i}
$$
Dove $𝑘$ è un parametro della funzione. Provare a capire per quali valori di $𝑘$ la serie converge.
Hint: Nella serie è presente un numero che può dare un indizio.

Esecuzione:
```c
#include <stdio.h>
#include <math.h>

double s_n(unsigned int n)
{
	double a_k = 1; // il primo termine della successione "interna"
	double s_k = a_k; // il primo termine della successione "somma", ed è uguale al primo elemento della successione interna
	printf("s_0 = %lf\n", s_k);
	for(int k = 1; k <= n; k++)
	{
		a_k = 1/pow((2*k + 1),2); // calcoliamo il nuovo elemento della successione interna
		s_k += a_k; // e lo sommiamo alla successione somma
		printf("s_%d = %lf\n", k, s_k);
	}
}

int main()
{
	unsigned int n;
	printf("Dammi il valore di n: ");
	scanf("%ud", &n);
	s_n(n); // utilizziamo un grande n per controllare che la serie converga al limite giusto
	printf("pi/8: %lf\n", pow(3.14159265358979323846,2) / 8);
}
```