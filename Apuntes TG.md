# Apuntes TG - Miguel Toro
## Nociones Básicas MD (1)
### Tipos de Grafos
Hay distintos tipos de grafos:
- `Grafo Completo ($k_n$)`: todos los vértices están conectados con todos los vértices.
- `Grafo Camino ($C_n$)`: hay un único ciclo que conecta a todos los vértices.
- `Grafo Bipartito ($k_{m,n}$)`: hay dos grupos de vértices, donde cada vértice de un grupo está conectado a todos los del grupo opuesto, pero no se conectan entre los del mismo grupo.
- `Grafo Rueda ($W_n$)`: hay un vértice en medio y el resto están alrededor de él. El del medio conecta con todos, y el resto entre los de su lado.

### Apuntes Básicos
- El número de valencia máximo de un grafo es su número de vértices menos uno.
- El grafo complementario a uno dado, es aquel que tiene las aristas que no tiene el otro, y viceversa.

### Ley del Apretón de Manos
Podemos saber el número de aristas aplicando LAM. Con esta ley sabemos que el número de aristas viene representado por el número de valencia de todos los vértices entre dos.

Por ejemplo, para un grafo completo:

$|A_{k_n}| = \frac{nº vértices \cdot nºvalencia}{2} =\frac{n \cdot (n-1)}{2}$

Siendo $n$ el número de vértices del grafo.

Nota: los vértices pueden tener distintas valencias, en ese caso habría que ir agrupándolos en la multiplicación.

### Matrices de Adyacencia
Las matrices de adyacencia representan un único grafo. Gracias a ellas podemos saber que vértices son adyacentes a cuales. Han de ser cuadradas, puesto que por filas y columnas se representan todos los vértices. Un 1 representa la unión de esos dos vértices por una arista, un 0 la ausencia de arista. Un número superior indica la aparición de varias aristas (multigrafo), o de peso en las mismas.

Las matrices han de tener su diagonal con ceros, ya que un vértice no se puede conectar a si mismo. Si las matrices son simétricas indican que el grafo no está dirigido, y si son asimétricas indican digrafos.

### Listas de Grafos
La lista de un grafo puede representar varios grafos distintos, e indican las valencias que tienen cada grafo.

Por ejemplo, la siguiente lista:

$(4, 4, 4, 4, 4)$

Indica un grafo completo de orden 5.

Cosas a tener en cuenta:
- Una lista no puede tener el número máximo y mínimo de vértices simultáneamente.
- No puede haber un vértice con el mismo o mayor número de elementos de la lista. Puesto que el valor máximo de valencia es del orden $n-1$.
- La suma de los elementos de la lista ha de ser par.

#### Havel-Hakini
Para comprobar que una lista sea de un grafo, podemos aplicar el algoritmo de Havel. Funciona de la siguiente manera:

Siendo el primer elemento de la lista $d$, debemos eliminarlo y restar $1$ a los siguientes $d$ elementos. Y así sucesivamente hasta conseguir una lista completamente de $0$. De lo contrario, la lista no pertenece a un grafo.

### Conexión en Grafos
Un grafo es `conexo` si tiene una única componente conexa. Todos los vértices de un grafo conexo están unidos entre sí.

### Distancias de un Grafo Simple
La distancia entre dos vértices de un grafo es el número de aristas entre el camino más corto por el que se unen.

La `excentricidad` de un vértice es la mayor distancia de v al resto de vértices del grafo.
- Diámetro: la mayor excentricidad.
- Radio: la menor excentricidad.