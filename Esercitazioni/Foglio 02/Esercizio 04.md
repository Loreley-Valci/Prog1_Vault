#fibonacci 
Letto un intero positivo da tastiera, stampare tutta la successione di Fibonacci fino all'elemento n-esimo compreso.
Nota: chiamando $F(i)=F_i$ l'elemento i-esimo della successione di Fibonacci allora:
$$ F_i = \begin{cases} 0 & \text{se $i = 0$} \\ 1 & \text{se $i = 1$} \\ F_{i-1} + F_{i-2} & \text{se $i > 1$} \\ \end{cases}$$

ad esempio, considerando $i=3$ , $F_3 = F_2+F_1 = (F_1+F_0)+F_1 = 2$.

Esecuzione:
```c
#include <stdio.h>

void main()
{
    int i;
    printf("Inserisci i: ");
    scanf("%d", &i);
    
    printf("i: %d\n", F(i));
}


int F(int i)
{
    if (i==0)
        return 0;
    else
    {
        if (i>1)
            return F(i-1)+F(i-2);
            
    return 1;
    }
}
```
