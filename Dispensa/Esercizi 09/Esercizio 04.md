#memoria
Determinare che cosa fa il seguente frammento di programma, disegnandone la memoria in modo opportuno.
```c
int a, b, c;
scanf("%d", &a);
scanf("%d", &b);

if(a>b)
{
	c = a;
	a = b;
	b = c;
}

printf("%d\n", b);
```
Successivamente, scrivere un programma equivalente senza modificare $a$ e $b$.

Memoria:
   $\rho$                   $\sigma$
a | l0              l0 | 16
b | l1              l1 | 4
s | l2               l2 | 20
d | l3              l3 | 12
m | l4             l4 | 64

f | l5               l5 | 4
