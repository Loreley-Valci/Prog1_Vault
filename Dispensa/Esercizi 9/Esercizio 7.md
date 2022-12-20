
Determinare il valore visualizzato dalle seguenti porzioni di codice nel caso in cui $num = 4$ e per i seguenti valori della variabile conta: $conta = 5, conta = 0$ e $conta = 1$.

Esecuzione:
```c
_// Programma 1_

	**int** conta, num;
	
	scanf("%d", &conta); 
	scanf("%d", &num);
	
	**while** (conta != 0) 
	{
			num = num * 10; 
			conta = conta - 1;
	}
	
	printf("%d**\n**", num);


_// Programma 2_

	**int** conta, num;
	
	scanf("%d", &conta); 
	scanf("%d", &num);
	
	**while** (conta >  0) 
	{ 
		num = num * 10; 
		conta = conta - 1;
	}
	
	printf("%d**\n**", num);
```
