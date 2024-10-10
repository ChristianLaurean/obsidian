---
Fecha_creación: 2024-05-31
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
Los conjuntos en Python son una estructura de datos que representa una colección no ordenada de elementos únicos. A diferencia de las [[Listas]] o [[Tuplas]], <span style="background:#fff88f">los conjuntos no permiten duplicados</span> y no tienen un orden definido. Esto significa que no puedes acceder a los elementos de un conjunto utilizando índices, y no puedes tener dos elementos iguales en un conjunto.

Los conjuntos son útiles cuando necesitas almacenar elementos únicos y realizar operaciones de conjuntos, como unión, intersección y diferencia.

A continuación, exploraremos cómo trabajar con conjuntos en Python.

# Conjuntos en Python: Operaciones Básicas

## Creando un conjunto

Puedes crear un conjunto utilizando llaves `{}` o utilizando la función `set()`. Por ejemplo:

```python
mi_conjunto = {1, 2, 3, 4, 5}
```

## Obtener la longitud del conjunto

Puedes obtener la cantidad de elementos en un conjunto utilizando la función `len()`. Por ejemplo:

```python
longitud = len(mi_conjunto)
```

## Acceder a elementos de un conjunto

Dado que los conjuntos no están ordenados y no tienen índices, no puedes acceder a elementos de forma directa.

## Comprobando un artículo

Puedes verificar si un elemento está presente en un conjunto utilizando el operador `in`. Por ejemplo:

```python
resultado = 3 in mi_conjunto
```

## Agregar elementos a un conjunto

Puedes agregar elementos a un conjunto utilizando el método `add()`. Por ejemplo:

```python
mi_conjunto.add(6)
```

## Eliminar elementos de un conjuntot link to Eliminar elementos de un conjunto")

Puedes eliminar un elemento de un conjunto utilizando el método `remove()` o `discard()`. Por ejemplo:

```python
mi_conjunto.remove(4)
```

## Borrar elementos de un conjunto

Puedes borrar todos los elementos de un conjunto utilizando el método `clear()`. Por ejemplo:

```python
mi_conjunto.clear()
```

## Eliminar un conjunto

Puedes eliminar un conjunto utilizando la palabra clave `del`. Por ejemplo:

```python
del mi_conjunto
```

## Conversión de lista a conjunto

Puedes convertir una lista en un conjunto utilizando la función `set()`. Por ejemplo:
```python
mi_lista = [1, 2, 3, 4, 5]
mi_conjunto = set(mi_lista)
```

## Unir conjuntos

Puedes unir dos conjuntos utilizando el método `union()` o el operador `|`. Por ejemplo:

```python
conjunto1 = {1, 2, 3}
conjunto2 = {3, 4, 5}
union_resultante = conjunto1.union(conjunto2)
```

## Encontrar elementos de intersección

Puedes encontrar los elementos comunes entre dos conjuntos utilizando el método `intersection()` o el operador `&`. Por ejemplo:

```python
interseccion_resultante = conjunto1.intersection(conjunto2)
```

## Comprobación de subconjunto y superconjunto

Puedes verificar si un conjunto es subconjunto o superconjunto de otro utilizando los métodos `issubset()` e `issuperset()`, respectivamente. Por ejemplo:

```python
es_subconjunto = conjunto1.issubset(conjunto2)
es_superconjunto = conjunto2.issuperset(conjunto1)
```

## Comprobar la diferencia entre dos conjuntos

Puedes encontrar la diferencia entre dos conjuntos utilizando el método `difference()` o el operador `-`. Por ejemplo:

```python
diferencia_resultante = conjunto1.difference(conjunto2)
```

## Encontrar la diferencia simétrica entre dos conjuntos

Puedes encontrar la diferencia simétrica entre dos conjuntos utilizando el método `symmetric_difference()` o el operador `^`. Por ejemplo:

```python
diferencia_simetrica = conjunto1.symmetric_difference(conjunto2)
```

## Unir conjuntos

Puedes agregar los elementos de un conjunto a otro utilizando el método `update()` o el operador `|=`. Por ejemplo:

```python
conjunto1.update(conjunto2)
```
# IN con sets es lo mas rapido

