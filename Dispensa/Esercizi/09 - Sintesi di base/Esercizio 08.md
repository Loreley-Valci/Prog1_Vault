#sommatoria #media_aritmetica 
Si scriva un programma per calcolare la media aritmetica di una serie di numeri $x_1, ..., x_n$ inseriti da tastiera, ovvero
$$
  {x_*} = {1 \over n} \cdot {\sum_{i=1}^{k} x_i}
$$
L’introduzione del valore 0 indica il termine del caricamento dei dati.

Esecuzione:
```c
#include<stdio.h>

void main()
{
    float somma=0;
    int conteggio=0;
    int x=-1;
    
    while (x!=0)
    {
        printf("Valore di x: ");
        scanf("%d", &x);

        if (x!=0)
        {
            somma=somma+x;
            conteggio=conteggio+1;
        }
    }
    printf("La media è: %f\n", somma/conteggio);
}
```
