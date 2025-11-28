# Grafos Críticos para el Color

Solos los grafos conexos son grafos críticos.

Una vez nos aseguremos de que el grafo es conexo, tenemos que ir quitandolas una a una, y comprobar si el número cromático se mantiene.
Si disminuye, es por que esa arista es crítica, y hay que volver a ponerla.
Si el número cromático se mantiene, esa arista es prescindible.

## Teorema

**Si un grafo $G$ es k-crítico entonces la valencia de sus vértices es mayor o igual que $k-1$.**

Hacemos una demostración por `Reducción al Absurdo`:
Si $G$ es k-crítico, entonces $\forall v \in V$, $s(v) \geq k-1$. Suponemos lo contrario:

$\exist G$ k-crítico y no ($\forall v \in V$, $s(v) \geq k-1$).

Que es lo mismo que decir:

$\exist G$ k-crítico y $\exist w \in V$, $s(v) \leq k-2$.


`Falta todo esto`

`Conclusión`: Todo grafo con número cromático k debe contener al menos k vértices de valencia mayor o igual que k-1.
