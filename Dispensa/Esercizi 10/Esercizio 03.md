
Si scriva una funzione che, ricevuti in ingresso le
coordinate $p_1 = (x_1, y_1)$ ed $p_2 = (x_2, y_2)$ di due punti del piano cartesiano, restituisca la loro distanza euclidea:
$$
	d(p_1,p_2)=\sqrt{(x_1-x_2)^2+(y_1-y_2)^2}
$$
Nota: la funzione radice quadrata (sqrt) in C viene fornita dalla librera math.h, che va quindi importata come segue:
```c
_#include_ _<stdio.h> // input output_ _#include_ _<math.h>  // sqrt_

double distanza(double x1, double y1, double x2, double y2)
{
	// codice vostro
	...
}
....
```

Esecuzione:
```c

```