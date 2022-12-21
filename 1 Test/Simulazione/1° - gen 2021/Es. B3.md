#py #classi 
Si consideri la seguente classe Python
```python
class SistemaPagamento:

	def calcola_pagamento(self, impiegati):

		print('Calcolo pagamento')
		print('===================')

		for impiegato in impiegati:
			print("Payroll:", impiegato.id, ' - ', impiegato.name)
			print("Totale:" impiegato.calcola_pagamento(), "\n")
```
In questo esercizio si deve:
- Creare una classe Impiegato che fornisce l’interfaccia di base per gli oggetti per cui il metodo $calcola_pagamento$ di $SistemaPagamento$ viene definito;
- Definire un metodo per il calcolo dello stipendio che distingue tra diversi tipi di impiegato. Si considerino:
	- Gli amministrativi (Amministrativi), che hanno un pagamento costante settimanale;
	- Alcuni impiegati (ImpiegatiOre) che sono pagati ad ore, con una tariffa ed un numero di ore lavorate che sono specifici per ciascun impiegato; 
	- Gli impiegati della compagnia (ImpiegatiCommissione) sono pagati con un salario fisso incrementato di una commissione che varia tra gli impiegati.

Stabilire la corretta gerarchia di eriditarieta per la classi sviluppate, e si crei un semplice programma che usa le suddette classi.

Esecuzione: