#py #classi 
Data la seguente classe che rappresenta tutte le funzioni $𝑓 ∶ ℝ → ℝ$

```python
class Funzione:
	def eval(self,x): # funzione che restituisce f(x)
		pass
```

Aggiungere a questa classe il metodo calcola_integrale(self,a,b,M) che permette di calcolare l’approssimazione di $\int_{a}^{b}{f(x) \; dx}$ tramite il metodo dei rettangoli, ossia:
$$
	\int_{a}^{b}{f(x) \; dx} \approx h \sum^{M-1}_{i=0} f(a+i*h)
$$
Dove $$ h=\frac{b-a}{M}$$Calcolare poi l’approssimazione dei seguenti integrali:
- $\int_{1}^{0}{x^2-2x \; dx}$
- $\int_{-\frac{\pi}{2}}^{\pi}{e^{2x} \; dx}$
- $\int_{-2}^{2}{\frac{x}{1+x^2} \; dx}$

![[Esercitazioni/Foglio 10/Esercizio 2.img1.jpg]]
Scrivendo le corrette sotto-classi di Funzione (sotto-classi che fanno l’override di eval() a seconda della funzione che stanno implementando).

Esecuzione:
```python
import math

class Funzione:
  def eval(self,x):
    pass

  def calcola_integrale(self,a,b,M):
    h = (b-a)/M
    sum = 0
    for i in range(M):
      sum = sum + self.eval(a + i * h)
    return h * sum
    # Oppure:
    # return h * sum([self.eval(a + i * h) for i in range(M)])

class Parabola(Funzione):
  def eval(self,x):
    return x**2 -2*x
    
class Esponenziale(Funzione):
  def eval(self,x):
    return math.exp(2 * x)

class Razionale(Funzione):
  def eval(self,x):
    return x / (1 + x ** 2)

funzione1 = Parabola()
integrale1 = funzione1.calcola_integrale(0,1,500)
print("Primo integrale: ",integrale1)

funzione2 = Esponenziale()
integrale2 = funzione2.calcola_integrale(-math.pi/2,math.pi,500)
print("Secondo integrale: ",integrale2)

funzione3 = Razionale()
integrale3 = funzione3.calcola_integrale(-2,2,500)
print("Terzo integrale: ",integrale3)

print("Convergenza del secondo integrale aumentando i rettangoli:")
integrals = [funzione2.calcola_integrale(-math.pi/2,math.pi,x) for x in range(10,10000,100)]
for i in integrals:
  print(i)
```
