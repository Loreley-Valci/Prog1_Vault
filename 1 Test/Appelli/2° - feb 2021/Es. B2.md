#FunzioneRicorsiva #array 
Si consideri questo frammento di programma C
```c
int f(int * a, int to)
{
	if (to == 0)
		return *a;
	else return *(a+to) + f(a, to-1);
}

int main(void)
{
	// carica vettore di N elementi (come con la nostra libreria)
	int N;
	double * x = read_double_array(argv[1], &N);
	
	int * y = (int *) malloc(size(int) * N); // N elementi
	
	for(int i = 0; i < N-1; i++)
	{
		y[i] = f(x, i);
	}
	return 0;
}
```
- Si definisca la formula calcolata dal programma per ciascun elemento dell’array $y$, cioè ($y[i] = ...$) e si fornisca un esempio di calcolo per un array di 4 elementi a scelta vostra;
- Si riscriva il programma eliminando la funzione ricorsiva $f$ ed usando solo due $for$ nel main.

Esecuzione:
```c

```