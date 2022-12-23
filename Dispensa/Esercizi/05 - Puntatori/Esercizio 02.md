#memoria 
Si disegni la memoria del seguente codice:
```c
int main()
{
	int x = 0;
	int y = 5;
	
	incr(x, 5); _//aumenta x di 5_
	incr(y, 7); _//aumenta y di 7_
}

void incr(int* p, int q)
{     
	_/* dereferenziazione */_
	*p = *p + q;
}

_/* chiamata nel main */_
int main()
{
	int x = 0;
	int y = 5;
	_/* dal_ _momento che il primo argomento è un puntatore, occorre usare & */_
	incr(&x, 5); _//aumenta x di 5_
	incr(&y, 7); _//aumenta y di 7_
}
```
convincendosi della persistenza delle modifiche ad $x$ e $y$ nel main.

Esecuzione: