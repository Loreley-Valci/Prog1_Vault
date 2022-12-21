#FunzioneIterativa 
Si scriva un programma C che calcola, per un dato $n \ge 0$ in input, la seguente successione numerica: $$ \begin{cases}  a_o = 1 \\  a_1 = 2 \\  a_n = \frac{(n+3*(a_{n-2}-2))}{a_{n-1}} & \text{con $n \ge 2$ se $n$ è pari}\\  a_n = \frac{(n+3*(a_{n-1}-2))}{a_{n-2}} & \text{con $n \ge 3$ se $n$ è dispari}\\  \end{cases}$$
in modo esclusivamente iterativo (ciclo for).

Esempio di calcolo:
- a2 = (2 + 3(a0 − 2))/a1 = −0.5
- a3 = (3 + 3(a2 − 2))/a1 = −2.25
- a4 = .... = 1.5555555

Suggerimento: Fate attenzione ai tipi delle variabili dichiarate!

Esecuzione:
```c

```