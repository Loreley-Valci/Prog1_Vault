#precedente_successivo
Si scriva un programma che legga un valore intero e visualizzi il valore intero precedente e il successivo.

Esecuzione:
```c
#include<stdio.h>

void main()
{
    int x;
    printf("Valore di x: ");
    scanf("%d", &x);

    int s=x+1;
    printf("Il valore superiore è: %d\n", s);

    int p=x-1;
    printf("Il valore precedente è: %d\n", p);
}
```

Memoria:
   $\rho$                   $\sigma$
x | l0              l0 | 10
s | l1              l1 | 11
p | l2              l2 | 9
