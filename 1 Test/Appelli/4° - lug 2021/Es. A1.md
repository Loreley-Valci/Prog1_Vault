#FunzioneIterativa #numero_primo #FunzioneRicorsiva 
Si scriva una funzione iterativa $myfunction$ che prenda in input due interi positivi $x$ ed $y$, e restitutisca il numero $k$ di numeri primi compresi tra $x$ ed $y$ esclusi. 

Per esempio, se $x = 2$ ed $y = 5$ allora $k = 1$ essendo ${3}$ primo, mentre se $x = 2$ ed $y = 10$ allora $k = {3}$ essendo ${3, 5, 7}$ primi. Si richiede di usare una funzione ausiliaria primo che stabilisca ricorsivamente se un numero sia primo, o meno.

Suggerimento: primo deve essere ricorsiva, si suggerisce la definizione int primo$(int n, int i)$ che restituisce $1$ se $n$ è primo secondo $i$. Il calcolo prevede di valutare se $i$ sia un divisore di $n$, ed eventualmente proseguire per ricorsione su $i-1$. Si ponga attenzione alla condizione di terminazione. Successivamente, si scriva $myfunction$ usando primo, e generando i numeri nell’intervallo $(x, y)$ con gli estremi come richiesto.

Esecuzione:
```c

```