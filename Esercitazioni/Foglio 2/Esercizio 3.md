#positivo_negativo #pari_dispari #valore_assoluto 
Letti due interi e da tastiera, determinare e stampare le seguenti informazioni:
- se $b$ è un numero positivo o negativo,
- se $a$ è un numero pari o dispari,
- il valore di $a+b$,
- quale scelta dei segni nell'espressione ($\pm$a) + ($\pm$b) porta al risultato massimo ed il suo valore.

Esecuzione:
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