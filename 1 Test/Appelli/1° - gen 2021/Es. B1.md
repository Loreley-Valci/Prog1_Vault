#memoria 
Si consideri questo frammento di codice C
```c
int main(void)
{
	int i = 3;
	int a[5];
	int j = i + 1; // P1
	for(int i = 0; i < 4; i++)
	{
		a[i] = i;
		j = i + 1; //P2 (terza iterazione)
	}
	j = i - j + 1; // P3
}
```
Si disegni la memoria del programma al punto P1, P2 (specificatamente alla terza iterazione del ciclo), ed al punto P3 (fine del main).

Esecuzione:
```c

```