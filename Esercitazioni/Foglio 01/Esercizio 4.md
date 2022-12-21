#media_aritmetica  #sommatoria 
Si scriva un programma per calcolare la media aritmetica di una serie di numeri $x_1,...,x_n$, ovvero:
$$
  {\overline x} = {1 \over n} \cdot {\sum_{i=1}^{n} x_i}
$$

L’introduzione del valore $0$ indica il termine del caricamento dei dati.

Esecuzione:
```c
#include <stdio.h>

void main ()
{
    int x=1;
    float s=0;
    int c=0;
    
    while (x!=0)
    {
        printf("Valore di x: ");
        scanf("%d", &x);
        
        s=s+x;
        
        if (x!=0)
            c=c+1;
    }
    printf("La media è: %f\n", s/c);
}
```
