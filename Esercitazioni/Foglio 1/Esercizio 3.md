#contadino_russo 
Consideriamo due numeri $n_1$ e $n_2$, per cui vogliamo calcolare il prodotto  $n_1*n_2$.
Seguendo l’algoritmo del contadino russo, si scrivono su un foglio, uno di fianco all’altro, i numeri da moltiplicare:
1. Si divide successivamente il primo numero per 2, arrotondando se necessario all’intero inferiore, fino a quando la divisione è uguale a 1.
2. Il secondo numero, invece, viene moltiplicato per 2 ad ogni passaggio.
3. Cancelliamo le righe dove a sinistra si trova un numero pari.
4. Sommiamo i numeri rimasti nella colonna di destra.
Implementare l’algoritmo in maniera iterativa.

Esecuzione:
```c
#include <stdio.h>

void main ()
{
    int m;
    printf("valore di m: ");
    scanf("%d", &m);
    
    int n;
    printf("valore di n: ");
    scanf("%d", &n);
    
    int p=0;
    
    while(m!=0)
    {
        if(m%2!=0)
        {
            p=p+n;
        }  
        m=m/2;
        n=n*2;
            
        printf("valore di p:%d\n", p);
        printf("valore di m:%d\n", m);
        printf("Valore di n:%d\n", n);
    }
    printf("Valore finale = %d\n", p);
}
```
