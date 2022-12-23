#FunzioneRicorsiva #potenza
Si scriva una funzione che riceva in ingresso due
numeri interi $a$ e $b  (b > 0)$ e restituisca il risultato della potenza $a^b$, in modo
iterativo e ricorsivo. Si crei una funzione di test che testa tutte le possibili
coppie di valore nell’intervallo $\left[1,5\right]$.

```c
#include<stdio.h>

int p(int a, int b)
{
    if (b==0)
        return 1;
    else
        return a*p(a, b-1);
}

void main ()
{
    int a;
    printf("Valore a: ");
    scanf("%d", &a);

    int b;
    printf("Valore b: ");
    scanf("%d", &b);

    printf("soluzione: %d\n", p(a, b));
}
```