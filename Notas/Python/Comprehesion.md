---
Fecha_creación: 2024-06-01
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---

La comprensión de listas es una sintaxis de Python que permite crear listas de forma concisa y eficiente. Se basa en el uso de expresiones lambda, que son funciones anónimas que se pueden utilizar para realizar operaciones simples.

## Estructura básica[​](https://docs.z2h.online/docs/Roadmaps/Python/Comprensi%C3%B3n%20de%20listas#estructura-b%C3%A1sica "Direct link to Estructura básica")

La estructura básica de una comprensión de listas es la siguiente:

```python
[ expresión para cada elemento en secuencia ]
```
# list comprehesion 

```python
lista = [i for i in range(1,10) if i * 2 > 10 else 'no']

# Create a 5 x 5 matrix using a list of lists: matrix
matrix = [[col for col in range(5)] for row in range(5)]
print(matrix)
# Print the matrix
for row in matrix:
	print(row)
```

# dict comprehesion

```python
# Create a list of strings: fellowship

fellowship = ['frodo', 'samwise', 'merry', 'aragorn', 'legolas', 'boromir', 'gimli']
# Create dict comprehension: new_fellowship
new_fellowship = {member:len(member) for member in fellowship} 
# Print the new dictionary

print(new_fellowship)
```

# Comprensión de listas frente a [[generadores]]

```python
# Create generator object: result

result = (num for num in range(31))

# Print the first 5 values
print(next(result))
print(next(result))
print(next(result))
print(next(result))
print(next(result))


# Print the rest of the values
for value in result:
	print(value)
```

