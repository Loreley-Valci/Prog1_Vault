#FunzioneRicorsiva #array 
Si consideri questo programma:
```c
int myFun(int arr[], int l, int r, int x)
{
	if (r >= l)
	{
		int mid = l + (r - l) / 2;
		if (arr[mid] == x)
			return(mid);
		if (arr[mid] > x)
			return(myFun(arr, l, mid - 1, x));
		return(myFun(arr, mid + 1, r, x));
	}
	return -1;
}

int main(void)
{
	int arr[] = { 2, 3, 4, 10, 40 };
	int n = 5;
	int x = 10;
	int result = myFun(arr, 0, n - 1, x);
}
```
Quale formula logica viene calcolata dalla funzione $myFun$? Si fornisca anche un esempio in cui $myFun$ restituisce $-1$ dopo almeno due chiamate ricorsive.