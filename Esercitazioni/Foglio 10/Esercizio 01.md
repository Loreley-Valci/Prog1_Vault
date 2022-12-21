#py #classi
Si creino tre classi:
- Triangolo
	- nel costruttore devono essere inizializzati i tre lati 
	- deve essere implementato un metodo che stampi a video se il triangolo è equilatero, isoscele o scaleno
- Rettangolo
	- nel costruttore devono essere inizializzati i due lati
	- deve essere implementato un metodo che stampi a video se il rettangolo è o meno un quadrato
- Cerchio
	- nel costruttore deve essere inizializzato il raggio

Tutte le classi devono implementare i metodi area() e perimetro(). Si implementi inoltre una funzione che data una lista di figure, ne calcoli l’area totale (la somma delle singole aree).
Hint: L’area di un triangolo dati i suoi lati si calcola con la formula di Erone:
$$
	p = \frac {a + b + c} {2}
$$
$$
	Area = \sqrt{p*(p-a)*(p-b)*(p-c)}
$$

Nota bene: Per utilizzare la radice quadrata in Python bisogna importare il modulo math (una volta) e utilizzare la funzione sqrt() così:
```python
import math
x = math.sqrt(2) # radice di 2
```

Esecuzione:
```python
from math import sqrt, pi

class FiguraGeometrica(object):
    def __init__(self, *args):
        self.lati = args
    
    def area(self):
        raise NotImplementedError()
    
    def perimetro(self):
        raise NotImplementedError()
    
    def __repr__(self):
        return "Figura sconosciuta %s" % str(self.lati)
    
class Triangolo(FiguraGeometrica):
    def __init__(self, l_a: int|float, l_b: int|float, l_c: int|float):
        super().__init__(l_a, l_b, l_c)
        
    def __repr__(self):
        return "Triangolo %s" % str(self.lati)
    
    def perimetro(self):
        return sum(self.lati)
    
    def area(self):
        p = self.perimetro / 2
        return sqrt(p * (p - self.lati[0]) * (p - self.lati[1]) * (p - self.lati[2]))
    
    def tipo_triangolo(self):
        if (self.lati[0] == self.lati[1] and self.lati[1] == self.lati[2]):
            return "equilatero"
        
        if (self.lati[0] == self.lati[1] or self.lati[1] == self.lati[2] or self.lati[0] == self.lati[2]):
            return "isoscele"
    
        return "scaleno"
    
class Rettangolo(FiguraGeometrica):
    def __init__(self, b: int|float, h: int|float):
        super.__init__(b, h)
        
    def __repr__(self):
        return "Rettangolo [b: %.3f, h: %.3f]" % self.lati
    
    def perimetro(self):
        return 2 * self.lati[0] + 2 * self.lati[1]
    
    def area(self):
        return self.lati[0] + self.lati[1]
    
    def base(self):
        return self.lati[0]
    
    def altezza(self):
        return self.lati[1]
    
    def tipo_rettangolo(self):
        if (self.lati[0] == self.lati[1]):
            return "quadrato"
        
        return None
    
class Raggio(FiguraGeometrica):
    def __init__(self, r):
        super.__init__(r)
        
    def __repr__(self):
        return "Cerchio [r: %.3f]" % self.lati[0]
    
    def perimetro(self):
        return self.lati[0] * 2 * pi
    
    def area(self):
        return self.lati[0]**2 * pi
    
    def raggio(self):
        return self.lati[0]
    
def AreaTot(self, *args):
    return sum([item.area() for item in args])
```