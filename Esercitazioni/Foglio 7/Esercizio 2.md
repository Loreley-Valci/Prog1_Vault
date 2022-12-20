#array 
Si scriva una funzione che dato un array $𝑎$ di dimensione $𝑛$, verifichi il seguente predicato:
$$
	\forall 𝑖 \in [0, 𝑛) \nexists 𝑗 \in [0, 𝑛) \mid  𝑎[𝑗] == 𝑎[𝑖] \land 𝑗 \neq 𝑖 
$$

Esecuzione:
```c
#include <stdio.h>

void init_array(int a[], int n)
{
	for (int i = 0; i < n; i++)
	{
		printf("a[%d] = ", i);
		scanf("%d", &a[i]);
	}
}

int duplicati(int a[], int n)
{
	int flag = 0;
	int i = 0;
	int j;
	while (i < n && !flag)
	{
		j = i+1;
		while (j < n && !flag)
		{
			if (a[i] == a[j])
				flag = 1;
			j++;
		}
		i++;
	}
	return flag;
}

void main()
{
	int n = 5;
	int a[5];
	init_array(a, n);
	
	int res = duplicati(a, n);
	if (res == 0)
		printf("Nell'array 'a' non sono presenti duplicati.\n");
	
	if (res == 1)
		printf("Nell'array 'a' sono presenti duplicati.\n");
}
```