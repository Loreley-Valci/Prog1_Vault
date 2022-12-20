#sommatoria 
$$
  S_n = \sum_{i=1}^{n}\frac{i \cdot k^{i+1}}{3^i}
$$

Programma:
```c
#include<stdio.h>

int p(int k, int i)
{
    if (i==1)
        return k;
    else
        return k*p(k, i-1);
}

float d(int k, int i)
{
    float m;
    m=i*p(k,i+1);
    return m/p(3,i);
}

float s(int n, int k)
{
    if (n==1)
        return d(k, n);
    else
        return d(k,n)+s(n-1, k);
}

void main()
{
    int k;
    printf ("Valore della base: ");
    scanf("%d", &k);

    int n;
    printf("Valore di n: ");
    scanf("%d", &n);
    
    printf("la sommatoria vale:%.3f\n", s(n,k));
}
```
