#memoria 
Si consideri questo programma
```c
int g(int x)
{
	return x*x;
}

float f(int x)
{
	if(x<g(x-2)) return (1.0);
	return(x*x-f(x-1));
}

void main()
{
	int x=4;
	x=f(x) //fine programma
}
```
- 1) Si spieghi, motivando la risposta, quanto vale $x$ alla fine del programma;
- 2) Si disegni la memoria del programma quando esse contiene il numero massimo di frames;
- 3) Si spieghi, motivando la risposta, se possimo trovare un valore di input di $f$ per cui il valore finale calcolato sarebbe esattamente $1.0$ .

Esecuzione: