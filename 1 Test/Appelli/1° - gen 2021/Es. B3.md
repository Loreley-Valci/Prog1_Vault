#py #classi #sommatoria 
Ci viene richiesto di implementare, in Python, una gerarchia di classi per lavorare con le funzioni matematiche - generiche $f(x)$ - e ci viene richiesto di implementare un particolare algoritmo per queste funzioni. Come vincolo ci viene data la seguente classe Function, che dobbiamo usare obbligatoriamente.
```c
class Function:
	"function R -> R"
	def eval(self):
		pass
```
L’algoritmo deve calcolare il valore medio $\overset{\wedge}{f}$ di $f(x)$ su di un intervallo $[a, b]$, con $0 \le a < b$. La formula per $\overset{\wedge}{f}$ viene definita come segue:
$$
	\overset{\wedge}{f}=\frac{1}{N}\sum^{N-1}_{i=0}\space f(a+i\sigma)
$$
dove:
- $N$ sono i sotto-intervalli in cui viene diviso l’intervallo $[a, b]$
- i sotto-intervalli sono tutti della stessa dimensione $\sigma > 0$

Esempio: $[a = 1, b = 3]$, con $N = 2$ otteniamo $\sigma = 1$ ed $\overset{\wedge}{f} = 0.5 ** [f(1) + f(2)]$.
In questo esercizio si deve:
- modificare la classe Function per fornire una funzione $f\_hat(self, a, b)$ che calcoli $\overset{\wedge}{f}$;
- creare una sottoclasse della nuova Function che rappresenti la funzione $f(x) = x2 + 2x$;
- usare un oggetto della sottoclasse per il calcolo di $\overset{\wedge}{f}$ sull’intervallo $[0, 6]$ con $N = 3$.

Suggerimenti: Si noti che $a + i\sigma$ risulta essere la coordinata di inizo dell’ $i$-esimo sotto-intervallo.

Esecuzione:
```c

```