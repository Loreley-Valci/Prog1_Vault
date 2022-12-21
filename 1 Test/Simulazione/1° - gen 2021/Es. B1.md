#memoria #FunzioneRicorsiva 
Si consideri questo frammento di codice C
```c
#include <stdio.h>

int f(int x, int a)
{
	int b = a;
	// P*
	if(x <= b)
		return(a);
	else
		return(b + f(x - 2, a + 1));
}

int main(void)
{
	int x = 10; // P1 - prima della chiamata di "f"
	int y = f(x, 0); // P2 - dopo la chiamata di "f"
	printf("%d", y);
}
```
Si disegni la memoria del programma al punto P1, ai punti P* (cioe durante ogni chiamata ricorsiva di $f$), ed al punto P2 (fine della chiamata). Stabilire il valore calcolato dalla chiamata con l’ultima $printf$.

Nota nel disegno della memoria si puo’ omettere il disegno di $[f, fun]$.

Esecuzione: