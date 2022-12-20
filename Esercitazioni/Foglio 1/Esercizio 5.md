#minimo_massimo 
Si scriva un programma per calcolare il valore massimo e minimo di un insieme di $n$ numeri inseriti da tastiera. Il programma deve prima leggere il valore di $n$ dall'utente, ed in seguito leggere una sequenza di $n>0$ numeri. A questo punto il programma deve stampare il massimo ed il minimo tra i numeri inseriti.

Esecuzione:
```c
#include<stdio.h>

void main()
{
    int y;
    printf("Quanti valori vuoi inserire? ");
    scanf("%d", &y);
    
    int mas;
    int min;
    
    for (int i=1; i<=y; i++)
    {
        int x;
        printf("Valore di x: ");
        scanf("%d", &x);
        
        if (i==1)
        {
            min=x;
            mas=x;
        }
        else
        {
            if (x<min)
                min=x;
            if (x>mas)
                mas=x;
        }    
    }
    printf("il massimo è: %d\nil minimo è: %d\n", mas, min);
}
```
