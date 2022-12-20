#valore_assoluto 
Si scriva una funzione che riceva in ingresso due numeri double $𝑥$ ed $𝑦$ e restituisca $1$ se e solo se i due numeri sono uguali a meno di un fattore $𝜖 = 10^{-9}$, ovvero $| 𝑥 − 𝑦| < 𝜖$ e $0$ in caso contrario.
Il valore di 𝜖 deve essere un parametro della funzione.

Esecuzione:
```c
#include <stdio.h> //printf, scanf
//calcolo il valore assoluto della differenza di due numeri
double valore_assoluto(double a)
{
//var per memorizzare il risultato
	double abs;
//se a è non-negativo
	if(a>=0)
	{
//il valore assouluto è a
		abs = a;
	}
//se a è negativo
	if(a<0)
	{
//il valore assoluto è -a
	abs = -a;
	}
	return abs;
}
  
int uguali(double a, double b, double epsilon) 
{
	//calcolo il valore assoluto della differenza
	double diff = valore_assoluto(a-b);
	//se sono uguali a meno di epsilon
	if(diff<epsilon)
	{
	//ritorno 1
		return 1;
	}
	//se distano più di epsilon
	else
	{
	//ritorno 0
		return 0;
	}
}

int main()
{
	//leggo variabili da tastiera
	double x, y, epsilon;
	printf("Inserire epsilon (e): ");
	scanf("%lf", &epsilon);
	
	printf("Inserire x: ");
	scanf("%lf", &x);
	
	printf("Inserire y: ");
	scanf("%lf", &y);
	  
	//chiamo la funzione
	int c = uguali(x, y, epsilon);
	if(c == 1)
	printf("I due numeri sono uguali con epsilon %f\n", psilon);
	
	else
	{
		printf("I due numeri sono diversi con epsilon %f\n", epsilon);
	}
	return(0);
}
```