#positivo_negativo #valore_assoluto 
Leggere da tastiera un generico numero e stampare un messaggio che indichi se è positivo o negativo. Dopodichè stampare il valore assoluto $\mid x \mid$. Risolvere l’esercizio senza alcuna variabile di appoggio.

Esecuzione:
```c
#include <stdio.h>

void main ()
{
    float x;
    printf("Inserire x: ");
    scanf("%f", &x);

    if (x>=0)
    {
        printf("%f è non negativo", x);
        printf("Valore assoluto: %f\n", x);
    }
    else 
    {
        printf("%f è negativo %f\n", -x);
        printf("Valore assoluto: %f\n", x);
    }
    return 0;
}
```
