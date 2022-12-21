#memoria 
Si disegni la memoria di questo programma ogni volta che si passa dai punti $A, B$ e $C$.
```c
int f(int p, int s)
{
	while(p<s)
	{
		s++;
		p=p+2
	}
	//A
	return (p);
}

void maib ()
{
	int p=7;
	
	for(int i=0; i<3; i++)
	{
		int p=f(i,p); //B
	}
	//C
}
```

Esecuzione: