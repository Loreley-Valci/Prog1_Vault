#sommatoria #serie 
Programma che calcola ricorsivamente la serie dell'esercizio 9 presente nel foglio esercizi 3


Esecuzione:
```c
#include <stdio.h>

double my_pow_it(double a, int b)
{ // calcola a^b iterativamente
	double pow = 1;
	for(int i = 0; i < b; i++)
		pow *= a;
	return a;
}  

double my_pow_ric(double a, int b)
{ // calcola a^b ricorsivamente
	if(b == 1) // caso base
		return a;
	return a * my_pow_ric(a,b-1);
}

double s_n(int n, double k)
{ // calcola ricorsivamente s_n
	if(n == 1) // caso base
		return k*k / 3;
	double num = n * my_pow_ric(k,n+1); // numeratore
	double a_n = num / my_pow_ric(3,n); // elemento n-esimo della successione interna
		return a_n + s_n(n-1,k);
}

int main()
{
	double k;
	int n;
	printf("Dammi k: ");
	scanf("%lf",&k);
	
	printf("Dammi n: ");
	scanf("%d",&n);
	
	double sum = s_n(n,k);
	printf("s_%d = %lf\n", n, sum);
}
```