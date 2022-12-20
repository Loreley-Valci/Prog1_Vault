#memoria 
Si consideri questo programma C
```c
int x = 6;
int *y = &x;

for(int i = 2; i < *y; i++)
{
	# A
	if(i %2 != 0)
	{
		int x = -1;
		*y = x;
	}
	else
	{
		x = x + *y;
	}
}
```
Si rappresenti la memoria del programma al punto A per ciascun ciclo di esecuzione del $for$. La memoria finale di questo programma sarebbe equivalente inizializzando $i=3$ o $i=4$?

Esecuzione:
```c

```