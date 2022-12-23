#4operazioni
Si scriva un programma capace di compiere le 4 operazioni (somma, sottrazione, moltiplicazione e divisione) tra due numeri reali inseriti da tastiera. Dopo che sono stati inseriti i due numeri, detti a e b, il programma dovrà visualizzare i quattro valori $a + b, a − b, ab, a$. Si ipotizzi che $b \neq 0$.

Esecuzione:
```c
#include<stdio.h>

void main()
{
    int a;
    printf("Valore di a: ");
    scanf("%d", &a);

    int b;
    printf("Valore di b: ");
    scanf("%d", &b);
    
    float s=a+b;
    printf("La somma è: %2f\n", s);

    float d=a-b;
    printf("La sottrazione è: %2f\n", d);

    float m=a*b;
    printf("La moltiplicazione è: %2f\n", m);

    if (b!=0)
    {
        float f=a/b;
        printf("La divisione è: %2f\n", f);
    }
    else
    {
        printf("b=%d quindi non è divisibile\n", b);
    }
}
```

Memoria:
   $\rho$                   $\sigma$
a | l0              l0 | 16
b | l1              l1 | 4
s | l2               l2 | 20
d | l3              l3 | 12
m | l4             l4 | 64

f | l5               l5 | 4