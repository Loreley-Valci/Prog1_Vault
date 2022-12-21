#potenza 
Scrivere un programma che riceva in ingresso due numeri interi $a$ e $b$ $(b > 0)$ e restituisca il risultato della potenza $a^b = a*a*...*a$ ($b$ volte).

Esecuzione:
```c
#include<stdio.h>

void main()
{
    int x;
    printf("Valore di x: ");
    scanf("%d", &x);
    
    int n;
    printf("Valore di n: ");
    scanf("%d", &n);
    
    int y=1;
    
    for (int i=0; i<n; i++)
    {
        y=y*x;
        printf("L'esponente è: %d\n", y);
    }
}
```
