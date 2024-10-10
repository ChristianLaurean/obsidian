---
Fecha_creación: 2024-06-08
Categorias: "[[Python]]"
tags:
  - Concepto
  - Programación
URL:
---
Es una función anónima o sin nombre. 

## sintaxis

```python
lambda argument : expresion

lambda x : sum(x) / len(x)# De esta forma nos da un tipo objeto lo mejor es hacer esto
(lambda x : sum(x) / len(x))([1,2,3])#con esto ya le pasamos la lista

promedio = lambda x : sum(x) / len(x)
promedio([1,2,4])


# tambien lo podemos usar con [[map]]

names_mayus = list(map(lambda x : x.upper()),names)
``` 

## Cuando deberiamos de usar una lambda?


- Cuando queramos hacer funciones sencillas 