#media_aritmetica
Si scriva un programma che legga due valori interi, calcoli la loro somma e la media aritmetica, e la stampi a schermo.

Esecuzione:
```c
#include<stdio.h>

void main()
{
    int x;
    printf("Valore di x: ");
    scanf("%d", &x);

    int y;
    printf("Valore di y: ");
    scanf("%d", &y);

    int s=x+y;
    printf("La somma dei valori è: %d\n", s);

    int m=s/2;
    printf("La media dei valori è: %d\n", m);
}
```

Memoria:
   $\rho$                   $\sigma$
x | l0              l0 | 5
y | l1              l1 | 3
s | l2              l2 | 8
m | l3            l3 | 4

