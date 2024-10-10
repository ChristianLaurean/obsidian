---
Fecha_creación: 2024-05-31
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
Las listas son una estructura de datos versátil y ampliamente utilizada en Python. Puedes pensar en ellas como una colección ordenada de elementos, donde cada elemento puede ser de cualquier tipo de dato.

A continuación, exploraremos varios temas relacionados con las listas en Python:

### Creación de una lista[​](https://docs.z2h.online/docs/Roadmaps/Python/Listas#creaci%C3%B3n-de-una-lista "Direct link to Creación de una lista")

Puedes crear una lista utilizando corchetes [] y separando los elementos con comas. Por ejemplo:

```python
mi_lista = [1, 2, 3, "Hola", True]
```

### Acceso a los elementos de la lista mediante la indexación positiva[​](https://docs.z2h.online/docs/Roadmaps/Python/Listas#acceso-a-los-elementos-de-la-lista-mediante-la-indexaci%C3%B3n-positiva "Direct link to Acceso a los elementos de la lista mediante la indexación positiva")

Puedes acceder a los elementos de una lista utilizando índices positivos. El primer elemento tiene índice 0, el segundo tiene índice 1, y así sucesivamente. Por ejemplo:

```python
mi_lista = [1, 2, 3]
print(mi_lista[0])  # Salida: 1
print(mi_lista[1])  # Salida: 2
```

### Acceso a los elementos de la lista mediante la indexación negativa[​](https://docs.z2h.online/docs/Roadmaps/Python/Listas#acceso-a-los-elementos-de-la-lista-mediante-la-indexaci%C3%B3n-negativa "Direct link to Acceso a los elementos de la lista mediante la indexación negativa")

También puedes acceder a los elementos de una lista utilizando índices negativos. El último elemento tiene índice -1, el penúltimo tiene índice -2, y así sucesivamente. Por ejemplo:

```python
mi_lista = [1, 2, 3]
print(mi_lista[-1])  # Salida: 3
print(mi_lista[-2])  # Salida: 2
```

### Desempaquetar elementos de la lista[​](https://docs.z2h.online/docs/Roadmaps/Python/Listas#desempaquetar-elementos-de-la-lista "Direct link to Desempaquetar elementos de la lista")

Puedes desempaquetar los elementos de una lista asignándolos a variables individuales. Por ejemplo:

```python
mi_lista = [1, 2, 3]
a, b, c = mi_lista
print(a)  # Salida: 1
print(b)  # Salida: 2
print(c)  # Salida: 3
```

### Cortar elementos de una lista[​](https://docs.z2h.online/docs/Roadmaps/Python/Listas#cortar-elementos-de-una-lista "Direct link to Cortar elementos de una lista")

Puedes obtener un subconjunto de elementos de una lista utilizando la sintaxis de corte. Por ejemplo:

```python
mi_lista = [1, 2, 3, 4, 5]
sub_lista = mi_lista[1:4]
print(sub_lista)  # Salida: [2, 3, 4]
```

### Modificación de listas

Las listas son mutables, lo que significa que puedes modificar sus elementos. Puedes asignar un nuevo valor a un elemento existente o cambiarlos mediante métodos como append(), extend(), insert(), etc.

### Comprobación de elementos en una lista

Puedes comprobar si un elemento está presente en una lista utilizando el operador in. Por ejemplo:

```python
mi_lista = [1, 2, 3]
print(2 in mi_lista)  # Salida: True
print(4 in mi_lista)  # Salida: False
```

### Adición de elementos a una lista

Puedes agregar elementos a una lista utilizando el método append() para agregar un elemento al final o extend() para agregar múltiples elementos al final. Por ejemplo:

```python
mi_lista = [1, 2, 3]
mi_lista.append(4)
print(mi_lista)  # Salida: [1, 2, 3, 4]

otra_lista = [5, 6]
mi_lista.extend(otra_lista)
print(mi_lista)  # Salida: [1, 2, 3, 4, 5, 6]
```

### Inserción de elementos en una lista

Puedes insertar un elemento en una posición específica de una lista utilizando el método insert(). Por ejemplo:

```python
mi_lista = [1, 2, 3]
mi_lista.insert(1, "Hola")
print(mi_lista)  # Salida: [1, "Hola", 2, 3]
```

### Eliminación de elementos de una lista

Puedes eliminar un elemento de una lista utilizando el método remove() pasando el valor del elemento a eliminar. Por ejemplo:

```python
mi_lista = [1, 2, 3]
mi_lista.remove(2)
print(mi_lista)  # Salida: [1, 3]
```

### Eliminación de elementos mediante Pop

Puedes eliminar un elemento de una lista utilizando el método pop() pasando el índice del elemento a eliminar. Por ejemplo:

```python
mi_lista = [1, 2, 3]
elemento_eliminado = mi_lista.pop(1)
print(elemento_eliminado)  # Salida: 2
print(mi_lista)  # Salida: [1, 3]
```

### Eliminación de elementos mediante Del

Puedes eliminar un elemento de una lista utilizando la declaración del y especificando el índice del elemento. Por ejemplo:


```python
mi_lista = [1, 2, 3]
del mi_lista[1]
print(mi_lista)  # Salida: [1, 3]
```

### Elementos de la lista de [[Comprehesion]]

Las listas de comprensión son una forma concisa de crear listas utilizando una única línea de código. Por ejemplo:

```python
cuadrados = [x**2 for x in range(5)]
print(cuadrados)  # Salida: [0, 1, 4, 9, 16]
```

### Copiar una lista

Puedes copiar una lista utilizando el método copy() o la sintaxis de rebanada [:]. Por ejemplo:

```python
mi_lista = [1, 2, 3]
copia_lista = mi_lista.copy()
print(copia_lista)  # Salida: [1, 2, 3]

otra_copia = mi_lista[:]
print(otra_copia)  # Salida: [1, 2, 3]
```

### Unirse a listas

Puedes unir dos listas utilizando el operador +. Por ejemplo:

```python
lista1 = [1, 2, 3]
lista2 = [4, 5, 6]
lista_unida = lista1 + lista2
print(lista_unida)  # Salida: [1, 2, 3, 4, 5, 6]
```

### Contar elementos en una lista

Puedes contar la cantidad de veces que aparece un elemento en una lista utilizando el método count(). Por ejemplo:

```python
mi_lista = [1, 2, 2, 3, 2]
conteo = mi_lista.count(2)
print(conteo)  # Salida: 3
```

### Encontrar el índice de un elemento

Puedes encontrar el índice de un elemento en una lista utilizando el método index(). Por ejemplo:

```python
mi_lista = [1, 2, 3]
indice = mi_lista.index(

2)
print(indice)  # Salida: 1
```

### Invertir una lista
Puedes invertir el orden de los elementos en una lista utilizando el método reverse(). Por ejemplo:

```python
mi_lista = [1, 2, 3]
mi_lista.reverse()
print(mi_lista)  # Salida: [3, 2, 1]
```

### Clasificación de elementos de la lista

Puedes ordenar los elementos en una lista utilizando el método sort(). Por ejemplo:

```python
mi_lista = [3, 1, 2]
mi_lista.sort()
print(mi_lista)  # Salida: [1, 2, 3]
```