#minimo_massimo 
Si scriva una funzione che riceva in ingresso tre numeri interi $π₯$, $π¦$ e π§ ne restituisca il minimo. Si crei una funzione di test che prenda in input due dei tre numeri dallβutente, $π₯$ e $π¦$, e testi la tripletta $(π₯, π¦, π€)$ con $w \in [1, \max(x, y)]$.
Nota: per testare la tripletta si intende testare ogni possibile tripla di valori ottenuta fissando $π₯$ ed $π¦$, e variando $π€$.

Esecuzione:
```c
#include <stdio.h>

int minimo_tra_tre(int x, int y, int z)
{
    int min;
    if (x<=y)
    {
        min=x;
    }
    else
    {
        min=y;
    }
    if (min>z)
    {
        min=z;
    }
    return min;
}

void test(int x, int y)
{
    int max;
    if(x>=y)
    {
        max=x;
    }
    else
    {
        max=y;
    }
    for(int i=1; i<=max; i++)
    {
    printf("Tripletta(%d, %d, %d) -minimo -> %d",x,y,i, minimo_tra_tre(x,y,i));
    }
}

void main()
{
    int x,y;
    printf("Inserisci x: ");
    scanf("%d", &x);
    printf("Inserisci y: ");
    scanf("%d", &y);
    
    test(x,y);
    return 0;
}
```
