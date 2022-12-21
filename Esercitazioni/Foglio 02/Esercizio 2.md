#sommatoria #potenza 
Dati due interi positivi e da tastiera, calcolare la sommatoria:
$$
S(n,k) = \sum_{i=1}^{n}{k^i} = k + k^2 + ... + k^n
$$
e stampare a schermo il risultato.
Nota: ad esempio, con $n=2$ e $k=3$ allora $S(2,3) = 3+3^2 = 3+9 = 12$.

Esecuzione:
#FunzioneRicorsiva 
```c
#include<stdio.h>

void main()
{
    int n;
    printf("Valore di n: ");
    scanf("%d", &n);
    
    int k;
    printf("Valore di k: ");
    scanf("%d", &k);
    
    printf("Soluzione: %d\n", s(n,k));
}

int s(int n, int k)
{
    if (n==1)
        return k;
    else
        return p(n,k)+s(n-1, k);
}

int p(int n, int k)
{
    if (n==0)
        return 1;
    else
        return k*p(n-1, k);
}
```


#FunzioneIterativa
```c
#include<stdio.h>

void main()
{
    int n;
    printf("Valore di n: ");
    scanf("%d", &n);

    int k;
    printf("Valore di k: ");
    scanf("%d", &k);

    int s=0;
    
    for (int i=1; i<=n; i++)
    {
        int k_i=1;
        
        for (int z=1; z<=i; z++)
        {
            k_i=k_i*k;
        } 

        s=s+k_i;
    }
    
    printf("Soluzione: %d\n", s);
}
```