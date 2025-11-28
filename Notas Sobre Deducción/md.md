# Notas sobre Deducción
###### Clase 10/09/25
## Implicaciones
**A implica B**

A es condición suficiente para B.

B es condición necesaria para A.

**Si A, entonces B.**

### Ejemplos de Negación de Frases
###### Nota: estas frases no tienen por qué ser ciertas.
1. Todo árbol es bipartito.

    Existe un árbol que no es bipartito.

2. Si un grafo es bipartito, entonces tiene un vértice x de valencia $\lambda(x) \leq \frac{n}{2}$. Verdadero

    Existe un grafo bipartito que todas sus valencias son $\lambda(x) > \frac{n}{2}$

3. Si un grafo no tiene vértices de corte, entonces es Hamiltoniano. Falso

    Existe un grafo sin vértices de corte y no es Hamiltoniano.

4. Si un grafo no es plano tiene un número de vértices mayor o igual a 5.

    Existe un grafo no plano con menos de 5 vertices.

## Recíproco de ($A \Rightarrow B$): $B \Rightarrow A$
No guarda ninguna relación con la original. Esas dos cosas son lo mismo, y son dos propiedades que no se pueden separar.

**B implica A**

B es condición suficiente para A.

A es condición necesaria para B.

**Si B, entonces A.**

## Doble Implicación
**A implica B**

**B implica A**

A es condición necesaria y suficiente para B y viceversa.

B es una caracterización de A y viceversa.

## Contrarecíproco de ($A \Rightarrow B$): $\neg B \Rightarrow \neg A$
**No B implica No A**

No B es condición suficiente para no A.

No A es condición necesaria para no B.

Si no B, entonces no A.

## Notas Importantes
...
## Tipos de Demostración
- `Directo`:
En una afirmación (una implicación). A partir de A se va paso a paso aplicanto argumentos basados en verdades conocidas hasta llegar a B.
        
        ¿Todo Árbol es Bipartito?
        1. Un árbol es un grafo sin ciclos.
        2. Si no tiene ciclos no tiene ciclos impares.
        3. Si no tiene ciclos impares es bipartito

- `Reducción al Absurdo`: 
    Se trata de suponer que lo que quiero demostrar no es cierto y por tanto es cierto su negación, y siguiendo una secuencia de pasos lógicos llegaré a algo contradictorio que me indica que mi suposición inicial es falsa y por tanto cierto lo contrario que es lo que quería demostrar.

    Se basa en el hecho de que sólo hay una verdad entre una afirmación y su negación.

    Para demostrar que $A \Rightarrow B$ demuestro que es falsa su negación $\neg(A \Rightarrow B)$.

//

    Si un grafo es bipartito, entonces, ¿tiene un vértice x de valencia $\lambda(x) \leq \frac{n}{2}$?

    Existe un grafo bipartito que todas sus valencias son $\lambda(x) > \frac{n}{2}$

- Método de Inducción Simple:
    Sea *P* una propiedad relaciona con el número natural n, se demuestra que:
    - *p* es cierta para un primer caso.......

- Método del Contrarecíproco

- Método del Contraejemplo: