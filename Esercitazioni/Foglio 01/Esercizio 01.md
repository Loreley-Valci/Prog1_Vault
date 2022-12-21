2#FunzioneIterativa 
Scrivere un programma che, dato un intero inserito da tastiera, stampi i valori dei quadrati perfetti per tutti gli interi minori del numero inserito.

Esempio: assumiamo $𝑁 = 5$. Il programma deve stampare $𝑀$ , per→$2 𝑀 = 1,..., 𝑁 12, 22, 32, ..., 𝑁2$

Esecuzione:
```c
#include <stdio.h>

void main ()
{
    int n;
    printf("inserire il valore di n");
    scanf("%d", &n);
    printf("ti stamperò i quadrati perfetti fino a %d\n", n);

    int sq;
    for(int i=1; i<=n; i++)
    {
        sq =i*i;
        printf("il quadrato di %d è %d\n", i, sq);
    }

    int p=1;
    while(p<=n);
    {
        printf("il quadrato di d% è d%\n", p, p*p);
        p =p+1;
    }

    while(n>0)
    {
        printf("il quadrato di %d è %d\n", n,n*n);
        n =n-1;
    }
}
```

Memoria:
