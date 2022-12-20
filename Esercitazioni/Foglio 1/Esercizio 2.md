#MCD 
L’algoritmo di Euclide è un metodo per calcolare il massimo comune divisore (MCD) tra due interi $x$ ed $y$.
A parole, la procedura è la seguente:
- parte con due numeri in input, appunto $x>0$ ed $y>0$, interi;
- sottrae il numero più piccolo tra $x$ ed $y$ dal più grande;
- continua, ossia ripete, la sottrazione del punto precedente fino a che i due numeri $x>0$ ed $y>0$ non sono uguali.

Il valore trovato - ovvero quello che rende $x$ ed $y$ uguali, è il MCD.

Esecuzione:
```c
#include <stdio.h>

void main ()
{
    int x;
    printf("Dai un valore ad x: ");
    scanf("%d", &x);

    int y;
    printf("Dai un valore ad y: ");
    scanf("%d", &y);

    if (x<=0 || y<=0)
    {
        printf("Valore nullo: %d %d\n",x ,y);
    }
    else
    {
        while(x!=y) 
        {
           if(x>y)
               x=x-y;
            else
               y=y-x;
        }
        printf("MCD dei valori è:%d\n",x);
    }    
}
```

Memoria:
