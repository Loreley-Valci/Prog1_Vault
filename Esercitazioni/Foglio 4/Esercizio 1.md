#numero_primo 
Calcola ricorsivamente se un numero è primo o meno

Esecuzione:
```c
#include <stdio.h>

int is_prime(int n, int m)
{
	// n = 7, m = 6
	// se n % m = 0 => m divisore di n => n non è primo
	// altrimenti n % m = !0
	// allora m -> m - 1 = 6
	if (m == 1) // Condizione di base
		return 1; // Il numero è primo => restituisco 1
	if (n % m == 0) // m divisore di n => n non è primo
		return 0; // Il numero non è primo
	return is_prime(n, m - 1);
}

int main()
{
	int n;
	printf("Inserire un numero intero positivo: ");
	scanf("%d", &n);
	
	if (n == 1)
	printf("1 è primo\n", n);
	else
	{
		int m = n - 1;
		if (is_prime(n, m) == 1)
		printf("%d è primo\n", n);
		else
		printf("%d non è primo\n", n);
	}
	return 0;
}
```