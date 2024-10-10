---
Fecha_creación: 2024-07-14
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---

## Decoradores de Python

Los decoradores de Python son una herramienta que se utiliza para modificar el comportamiento de una función.

Los decoradores se pueden utilizar para realizar una variedad de tareas, como agregar funcionalidad adicional a una función, registrar el tiempo de ejecución de una función o realizar comprobaciones de seguridad.

## Creando decoradoresdores
Un decorador se define como una función que toma una función como parámetro y devuelve otra función. La siguiente función `decorar()` es un decorador que agrega una nueva línea al final de la salida de una función:


```python
def decorar(f):
	def wrapper(*args, **kwargs):
        resultado = f(*args, **kwargs)
        print("--")
        return resultado    
    return wrapper
```

Esta función se puede utilizar de la siguiente manera:
```python
@decorar
def saludar(nombre):
	print(f"Hola, {nombre}!")saludar("Juan")
```

Esta salida producirá el siguiente resultado:

```python
Hola, Juan!--
```

En este ejemplo, el decorador `decorar()` toma la función `saludar()` como parámetro.

