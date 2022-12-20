#fibonacci

```c
#include <stdio.h>

void main ()
{
    int n;
    printf("valore di n: ");
    scanf("%d", &n);

    //caso base
	    int F0=0;
	    int F1=1;
	    printf("F(0)=%d\n", F0);
	    printf("F(1)=%d\n", F1);

    //caso generale
	    int Fi,Fi1=F1,Fi2=F0;
	    for(int i=2; i<=n; i++);
	    {
	        Fi=Fi1+Fi2;
	        Fi2=Fi1;
	        Fi1=Fi;
	
	        printf("F=(%d)\n",Fi ,Fi2);
	    }
}
```
