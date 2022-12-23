#positivo_negativo #valore_assoluto
Si realizzi un programma che acquisisca da tastiera un numero $x$ e stampi un messaggio che indichi se tale numero sia positivo oppure negativo, e ne stampi il valore assoluto $\mid x \mid$. Si richiede di risolvere l’esercizio senza alcuna variabile di appoggio.

Esecuzione:
```c
#include<stdio.h>

void main()
{
    int x;
    printf("Valore di x: ");
    scanf("%d", &x);

    if (x>=0)
    {
        printf("è positivo, in valore assoluto è: %d\n",x);
    }
    else
    {
        x=-x;
        printf("è negativo, in valore assoluto è: %d\n",x);
    }
}
```
