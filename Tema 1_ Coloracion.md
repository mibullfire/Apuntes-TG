# Número Cromático y Número de Intependencia

## Demostraciones

Si un parámetro $P$ tiene una condición: $P(G) = k$. Hay que demostrar que:
$$P(G) \leq k$$
$$P(G) \geq k$$

Tenemos pues, dos cotas, una superior y una inferior. Si el intervalo que forman lo hacemos lo suficientemente pequeño, dará el caso donde se cumplirá la igualdad.

## Coloración de Vértices

Dado un grafo

El menor valor de $k$ de forma que existe una *k-vértice-coloración* del grafo $G$ se llama número cromático $\chi(G)$.

### Propiedades del número Cromático

- $\chi(G) = 1$ si y sólo si el grafo es trivial (no tiene aristas).
- $\chi(G) = 2$ si y sólo si es bipartito.
- $1 \leq \chi(G) \leq n$, con $n$ el número de vértices de $G$.
- Si $G'$ es un subgrafo de $G$, $\chi(G') \leq \chi(G)$.
- Si $G_1, G_2, \ldots, G_c$ son las componentes conexas del grafo $G$:
    $$\chi(G) = \max\{\chi(G_1), \chi(G_2), \ldots, \chi(G_c)\}$$

**Teorema (Brooke):** Sea $G$ un grafo conexo con grado máximo $\Delta$. Entonces:

- $\chi(G) \leq 1 + \Delta$
- $\chi(G) \leq \Delta$ si y sólo si $G$ no es ni completo ni un ciclo impar.

### Cálculo del Número Cromático

- Cotas Superiores: con algoritmo Voraz o cotas conocidas.
- Cotas Inferiores: búsqueda de subgrafos con número cromético conocido, o usando la lógica deductiva.

## Número de Independencia

Un conjunto de vértices de un grafo $G$, se dice independiente si no exiten adyacencias entre ellos (el subgrafo inducido por ellos es trivial).

Dado un grafo $G=(V,A)$, se llama número de independencia de $G$, $α(G)$, al mayor cardinal de un conjunto independiente de vértices de $G$.

### Propiedades del Número de Independencia

- $α(G) =1$ si y sólo si el grafo es completo.
- $α(G) =n$ si y sólo si es el grafo trivial de n vértices.
- $1 ≤ α(G) ≤ n$, con n el número de vértices de $G$.
- Si $G’$ es un subgrafo recubridor de $G$, $α(G’) ≥α(G)$.
- Si $G1, G2, ... , Gc$ son subgrafos de $G$ tales que en su unión es un subgrafo recubridor de $G$, entonces:
$$α(G) ≤ α(G1)+α(G2)+ ...+ α(Gc)$$

`Nota`: Esta propiedad nos proporciona un método para encontrar una cota superior útil en el cálculo del número de independencia.

### Cálculo del Número de Independencia

- Acotaciones inferiores: encontrando un conjunto independiente maximal de vértices a
través de un algoritmo voraz.
- Acotaciones superiores: construyendo un conjunto de subgrafos cuya unión sea un
subgrafo recubridor o por lógica deductiva.

## Relación entre el Número Cromático y el Número de Independencia

Una k-coloración de un grafo G es partición del grafo en k conjuntos independientes.

$$\chi(G)\geq\alpha(\neg{G})$$

Existe un conjunto independiente de vértices (S) máximo tal que $|S| = \alpha(\neg G)$.

S forma un clique en G, y por tanto $K_{S} \subseteq G$.

![1.0](/Images/1.0.png)

Por tanto:
$$\alpha (\neg G)=|S| = \chi(K_{S}) \geq \chi(G)$$

Si *G* tiene n vértices:
$$\frac{n}{\alpha(G)} \leq \chi(G) \leq n - \alpha(G) +1$$

`Demostración de`: $\frac{n}{\alpha(G)} \leq \chi(G)$:

![1.1](/Images/1.1.png)

Por tanto:
$$n = \sum_{i=1}^{\chi(G)} |V_i| \leq \sum_{i=1}^{\chi(G)} \alpha(G) = \chi(G) \cdot \alpha(G)$$

Con esto demostramos la primera parte.

`Demostración de`: $\chi(G) \leq n - \alpha(G) +1$

*Con esta demostración puedo demostrar una coloración con ese número de colores*.

Buscamo una coloración de G que use $n-\alpha(G)+1$ color. Entonces deduciremos el enunciado.

`FIGURA 1.2`

**Teorema**: Sea un G un grafo con m aristas. Entonces:

$$\chi(G) \leq \frac{1}{2}+ \sqrt{2m+\frac{1}{4}}$$
