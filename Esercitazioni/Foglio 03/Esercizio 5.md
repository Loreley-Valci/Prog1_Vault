#base_binaria #base_decimale
Scrivere una funzione che, preso in input un numero intero in base binaria, lo converta a base decimale.
Hint: l’algoritmo per passare da base binaria a base decimale, dato un numero le cui cifre sono $𝑐_n, 𝑐_{n-1}, … , 𝑐_1, 𝑐_0$.
Espresso in base 2 è: $𝑐_0 ∗ 2^0 + 𝑐_1 ∗ 2^{n-1} + ⋯ + 𝑐_{n-1} ∗ 2^{n-1} + 𝑐_n ∗ 2^n$

Esecuzione:
```c
#include<stdio.h> //printf, scanf
#include<math.h> //pow

int convert_2_10(long int n)
{
	//var dove memorizzare l'input in base 10
	int dec = 0;
	int r; //resto
	int i = 0; //iterazione
	
	while(n!=0)
	{
		//resto della divisione per 10
		r = n % 10;
		//quoziente
		n /= 10; //n = n/10
		//aggiorno risultato
		dec += r * pow(2,i);
		//aggiorno iterazione
		++i;
	}
	//alla fine del while ho convertito l'input da base 2 a base 10
	return dec;
}

int main()
{
	//leggo il numero binario da tastiera
	long int n;
	printf("Inserire il numero in base 2: ");
	scanf("%ld", &n);
	
	//converto in base 10
	int dec = convert_2_10(n);
	//stampo risultato
	printf("L'equivalente in base 10 è: %d\n", dec);
	return(0);
}
```