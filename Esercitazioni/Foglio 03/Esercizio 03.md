#valore_assoluto 
Si scriva una funzione che riceva in ingresso due numeri double $π₯$ ed $π¦$ e restituisca $1$ se e solo se i due numeri sono uguali a meno di un fattore $π = 10^{-9}$, ovvero $| π₯ β π¦| < π$ e $0$ in caso contrario.
Il valore di π deve essere un parametro della funzione.

Esecuzione:
```c
#include <stdio.h> //printf, scanf
//calcolo il valore assoluto della differenza di due numeri
double valore_assoluto(double a)
{
//var per memorizzare il risultato
	double abs;
//se a Γ¨ non-negativo
	if(a>=0)
	{
//il valore assouluto Γ¨ a
		abs = a;
	}
//se a Γ¨ negativo
	if(a<0)
	{
//il valore assoluto Γ¨ -a
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
	//se distano piΓΉ di epsilon
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