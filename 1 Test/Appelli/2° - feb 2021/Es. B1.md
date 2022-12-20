#memoria #memoria_dinamica 
Si consideri questo frammento di codice C
```c
int main(void)
{
	int i = 6;
	int *p = &i;
	int a[3] = {0, -1, 4}; // P1
	
	int *s = a;
	
	int v = *(s+a[0]); // P2
	
	v = v + *(s+2) + *p; // P3
}
```
Si disegni lo stato del programma (ambiente, memoria, heap) al punto P1, P2 ed al punto P3 (fine del main).

Esecuzione:
```c

```