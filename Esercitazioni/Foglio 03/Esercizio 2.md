#RadicaQuadrata 
Si scriva una funzione che, ricevuti in ingresso le coordinate $p_1 = (𝑥_1, 𝑦_1)$ ed  $p_2 = (𝑥_2, 𝑦_2)$  di due punti del piano cartesiano, restituisca la loro distanza uclidea
$𝑑(𝑝_1, 𝑝_2) = \sqrt{(𝑥_1 − 𝑥_2)^2 + (𝑦_1 − 𝑦_2)^2}$.
Nota: la funzione radice quadrata (sqrt) in C viene fornita dalla libreria math.h

Esecuzione:
```c
#include <math.h>
#include <stdio.h>

double distanza(double x, double y, double x1, double y1)
{
//variabili di appoggio
	double diff1, diff2, sum;
	//diff1 conterrà (x1-x)^2
	diff1 = x1 - x;
	diff1 = diff1*diff1;
	//diff2 conterrà (y1-y)^2
	diff2 = y1 - y;
	diff2 = diff2*diff2;
	//sum conterrà (x1-x)^2 + (y1-y)^2
	sum = diff1 + diff2;
	//calcolo distanza
	double dist = sqrt(sum);
	//ritorno la distanza
	return dist;
	
	/* soluzione più snella usando la funzione pow della libreria math, che calcola la potenza: pow(a,b) = a^b
	double dist = sqrt(pow(x1-x,2)+pow(y1-y,2));
	return dist; */
}

int main()
{
	//definisco coordinate esempio
	printf("Inserire le coordinate (x1,y1) e (x2,y2) per cui si vuole calcolare la distanza: \n");
	double x, y, x1, y1;
	printf("x1: ");
	scanf("%lf", &x);
	
	printf("y1: ");
	scanf("%lf", &y);
	
	printf("x2: ");
	scanf("%lf", &x1);
	
	printf("x2: ");
	scanf("%lf", &y1);
	
	//chiamo la funzione
	double dist = distanza(x, y, x1, y1);
	//stampo il risultato
	printf("distanza tra (%lf, %lf) e (%lf, %lf) = %lf\n", x, y, x1, y1, dist);
	
	return(0);
}
```