#sommatoria #potenza #FunzioneRicorsiva 
Si scriva un programma C che calcola, per un dato $n > 0$ in input, il valore
$$
  {s_n} = {2^n} \cdot {\sum_{i=1}^{n} i}
$$

Il calcolo della potenza e della sommatoria in $s_n$ deve utilizzare solamente funzioni ricorsive.
Esempio di calcolo: per $n = 3$ vale $s_n = 48$, per $n = 6$ vale $s_n = 1344$, etc.

Esecuzione:
```c
#include <stdio.h>

int somma(int n)
{
    if (n!=1)
        return n+somma(n-1);
    else
        return 1;    
}

int potenza(int n)
{
    if (n!=1)
        return 2*potenza(n-1);
    else
        return 2;
}

void main()
{
    int n;
    printf("inserire il valore di n: ");
    scanf("%d", &n);
    printf("sol: %d\n", potenza(n)*somma(n));
}
```
