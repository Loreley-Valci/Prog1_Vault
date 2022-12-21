#memoria 
Si consideri questo programma C
```c
// funzione ausiliaria
int f(int x)
{
	return(x+6); // A
}

int x = 6;
int y = x + 1; // B

y = f(y);
int * z = y;

z = f(*z - y) // C
```
Si rappresenti la memoria del programma ai punto A, B e C. Si noti che A viene eseguito 2 volte