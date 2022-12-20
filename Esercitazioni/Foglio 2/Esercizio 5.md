#valori_fattoriali 
Dati due interi positivi $n$ e $k$ da tastiera, calcolare il coefficiente binomiale di $n$ su $k$.
Nota: Il coefficiente binomiale $C(n,k)$ di $n$ su $k$, anche indicato con $\binom{n}{k}$ , è dato da:
$$
  C(n,k) = \binom{n}{k} = \frac{n!}{k!(n-k)!}
$$
Se $n \geq k$, mettere se $n<k$ definiamo $C(n,k) = 0$.
Ad esempio, con $n=3$ e $k=2$, si ottiene $C(3,2) = 6/2 =3$.

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
