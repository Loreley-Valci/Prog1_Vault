#classi 
Si considerino le seguenti classi
```python
class C1:
	def __init__(self):
		self.i = 1

class C2(C1):
	def __init__(self):
		super().__init__()
		self.i = 1
```
- Si riscriva la gerarchia di classi in modo che il costruttore di $C1$ prenda un parametro generico (generalizzando l’assegnamneto $i=1$), e si cambi di conseguenza $C2$.
- Si scriva un metodo quadrato che restituisca il valore del quadrato del numero memorizzato; si decida e motivi in quale classe tale metodo debba essere realizzato.

Esecuzione:
