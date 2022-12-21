#positivo_negativo #pari_dispari #valore_assoluto 
Si scriva un programma che legga due numeri da tastiera, detti $a$ e $b$, e determini le seguenti informazioni, stampandole a video:
- se $b$ è un numero positivo o negativo;
- se $a$ è un numero pari o dispari;
- il valore di $a + b$;
- quale scelta dei segni dell’espressione $(\pm a) + (\pm b)$ porta al risultato massimo, e quale è questo valore.
Suggerimento: il valore massimo della somma di $a$ e $b$ si può ottenere sommando il valore assoluto di $a$ ed il valore assoluto di $b$.

Esecuzione:
```c
#include<stdio.h>

void main()
{
    int a;
    printf("Valore di a: ");
    scanf("%d", &a);

    int b;
    printf("Valore di b: ");
    scanf("%d", &b);
  
    if (b>=0)
    {
        printf("b è positivo\n");
    }
    else
    {
        printf("b è negativo\n");
    }

    if (a%2==0)
    {
        printf("a è pari\n");
    }
    else
    {
        printf("a è dispari\n");
    }

    int s=a+b;
    printf("La loro somma è: %d\n", s);

    if (a<0) 
    {
        a=-a;
    }
    if (b<0) 
    {
        b=-b;
    }
        
    int ns=a+b;
    printf("Il risultato massimo è: %d\n", ns);
}
```
