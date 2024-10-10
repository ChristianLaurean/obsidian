---
Fecha_creación: 2024-05-31
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
# Tuplas

Las tuplas son estructuras de datos en Python que nos permiten almacenar múltiples elementos de manera ordenada. A diferencia de las [[Listas]], las tuplas son <font color="#c00000">inmutables</font>, lo que significa que no se pueden modificar después de su creación. Aprenderemos cómo crear y acceder a los elementos de una tupla.

##### Propiedades y ventajas de las tuplas en comparación con las listas

Las tuplas tienen algunas propiedades y ventajas distintivas en comparación con las listas en Python. Exploraremos estas características y entenderemos en qué situaciones las tuplas pueden ser más convenientes que las listas. Algunos puntos a considerar son:

- Inmutabilidad de las tuplas y cómo garantiza la integridad de los datos.
- Eficiencia en el uso de memoria debido a su inmutabilidad.
- Utilidad de las tuplas en contextos donde no se necesitan modificaciones.
- Uso de tuplas como claves en diccionarios debido a su inmutabilidad.

¡Aprenderemos cómo aprovechar las tuplas como una estructura de datos poderosa y entenderemos sus ventajas en comparación con las listas en Python!

Ejemplo de creación de una tupla:

```python
mi_tupla = (1, 2, 3, 4, 5)
```

Ejemplo de acceso a elementos de una tupla:

```python
primer_elemento = mi_tupla[0]
segundo_elemento = mi_tupla[1]
```

```python
# Crear una tupla
mi_tupla = (1, "Hola", True, 3.14)
print(mi_tupla)

# Acceder a elementos
tupla = (10, 20, 30, 40, 50)
print(tupla[2])  # Acceder al tercer elemento (índice 2)
print(tupla[-1])  # Acceder al último elemento utilizando índice negativo

# Concatenar tuplas
tupla1 = (1, 2, 3)
tupla2 = (4, 5, 6)
tupla_concatenada = tupla1 + tupla2
print(tupla_concatenada)

# Desempaquetar tuplas
persona = ("Juan", 25, "Argentina")
nombre, edad, pais = persona
print(nombre)
print(edad)
print(pais)

# Comprobar la existencia de un elemento
frutas = ("Manzana", "Banana", "Naranja")
if "Manzana" in frutas:
    print("La fruta está presente")
else:
    print("La fruta no está presente")

# Iterar sobre una tupla
numeros = (1, 2, 3, 4, 5)
for numero in numeros:
    print(numero)

# Calcular la longitud de una tupla
tupla = (10, 20, 30, 40, 50)
longitud = len(tupla)
print("La longitud de la tupla es:", longitud)

# Comparar tuplas
tupla1 = (1, 2, 3)
tupla2 = (4, 5, 6)

if tupla1 == tupla2:
    print("Las tuplas son iguales")
elif tupla1 < tupla2:
    print("La tupla1 es menor que la tupla2")
else:
    print("La tupla1 es mayor que la tupla2")

# Convertir una lista en una tupla
lista = [1, 2, 3, 4, 5]
tupla = tuple(lista)
print(tupla)

# Slicing de tuplas
tupla = (10, 20, 30, 40, 50)
porcion = tupla[1:4]
print(porcion)

# Contar elementos en una tupla
tupla = (1, 2, 2, 3, 3, 3, 4, 4, 4, 4)
contador = tupla.count(3)
print("El elemento 3 aparece", contador, "veces")

# Encontrar el índice de un elemento
tupla = ("Manzana", "Banana", "Naranja")
indice = tupla.index("Banana")
print("El índice de 'Banana' es:", indice)
```