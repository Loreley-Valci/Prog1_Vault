#lista #malloc 
- Si scriva una funzione che chieda all’utente un numero indefinito di numero interi e crei una lista con i numeri inseriti. L’inserimento termina quanto l’utente inserisce il numero −1 (che non viene incluso nella lista). La funzione deve ritornare la testa della lista. 
- Si scriva una funzione che data la testa di una lista di numeri interi $𝑎$, ne stampi il contenuto. 
Nota bene: d’ora in poi, per “testa di un lista” si intenderà il puntatore al primo elemento di una lista. Cioè, se un esercizio dice “data la testa di una lista”, intende “dato il puntatore al primo elemento di una lista”.

Esecuzione:
```c
#include<stdio.h>
#include<stdlib.h>

struct nodo
{
    int info;
    struct nodo * next;
};

typedef struct nodo elementoLista;
typedef elementoLista * lista;

lista crea_lista()
{
    lista a=NULL;
    int n;
    printf("Inserisci un numero: ");
    scanf("%d", &n);
    
    if(n == -1)
        return a;
        
    elementoLista * nuovo = malloc(sizeof(elementoLista));
    
    (*nuovo).info = n; //nuovo -> info = n queste due sono uguali
    nuovo -> next = NULL;
    
    a = nuovo;
    
    elementoLista * coda;
    coda = nuovo;
    
    printf("Inserisci un numero: ");
    scanf("%d", &n);
    
    while(n != -1)
    {
        nuovo = malloc(sizeof(elementoLista));
        nuovo -> info = n;
        nuovo -> next = NULL;
        coda -> next = nuovo;
        printf("Inserisci un numero: ");
        scanf("%d", &n);
    }
    return a;
}

//ricorsiva
void stampa_lista_ric(lista a)
{
    if(a == NULL)
        return;
    printf("%d\n", a -> info);
    stampa_lista_ric(a->next);
}

//iterativa
void stampa_lista_int(lista a)
{
    while(a != NULL)
    {
        printf("%d\n", a->info);
        a=a->next;
    }
}

void main()
{
    lista a = crea_lista();
    stampa_lista_int(a);
    stampa_lista_ric(a);
}
```