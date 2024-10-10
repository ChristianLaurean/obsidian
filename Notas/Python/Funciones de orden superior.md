---
Fecha_creación: 2024-07-14
Categorias: "[[Productividad]]"
tags:
  - Programación
URL:
---
Una función de orden superior es una función que puede tomar otra función como parámetro o que puede devolver una función como valor de retorno.

## Función como parámetro

Una función puede tomar otra función como parámetro para realizar una operación. Por ejemplo, la siguiente función `doblar()` toma una función `f()` como parámetro y la llama, duplicando el valor devuelto:


```python
def doblar(f):
	def wrapper(x):
        return 2 * f(x)    
    return wrapper
```

Esta función se puede utilizar de la siguiente manera:


```python
def sumar(x):
	return x + 1
	
doblar_sumar = doblar(sumar)
print(doblar_sumar(5))
```

Esta salida producirá el siguiente resultado:

```
11
```

En este ejemplo, la función `doblar()` toma la función `sumar()` como parámetro. La función `doblar()` crea una nueva función anónima, `wrapper()`, que llama a la función `f()` (en este caso, `sumar()`) y duplica el valor devuelto. La función `doblar()` devuelve la función `wrapper()`.

## Función como valor de retorno

Una función también puede devolver otra función como valor de retorno. Por ejemplo, la siguiente función `crear_funcion()` crea una función que suma dos números:


```python
def crear_funcion():
	def sumar(x, y):
        return x + y
    return sumar
```

Esta función se puede utilizar de la siguiente manera:


```python
suma = crear_funcion()
print(suma(1, 2))
```

Esta salida producirá el siguiente resultado:

```
3
```

En este ejemplo, la función `crear_funcion()` devuelve una función anónima que suma dos números. La función `crear_funcion()` se puede utilizar para crear funciones de forma concisa y reutilizable.


## Cierres de Python

Los cierres de Python son funciones anónimas que conservan el acceso a las variables definidas en el ámbito en el que se crearon.

Los cierres se pueden utilizar para crear funciones de orden superior que pueden acceder a variables definidas fuera de la función. Por ejemplo, la siguiente función `doblar_variable()` toma una variable como parámetro y crea una función anónima que dobla el valor de la variable:


```python
def doblar_variable(x):
	def wrapper():
        return 2 * x
    return wrapper
```

Esta función se puede utilizar de la siguiente manera:


```python
x = 5
doblar_x = doblar_variable(x)
print(doblar_x())
```

Esta salida producirá el siguiente resultado:

```
10
```

En este ejemplo, la función `doblar_variable()` toma la variable `x` como parámetro. La función `doblar_variable()` crea una función anónima, `wrapper()`, que duplica el valor de la variable `x`. La función `doblar_variable()` devuelve la función `wrapper()`.

Cuando se llama a la función `wrapper()`, la función todavía tiene acceso a la variable `x`, incluso si `x` no está definida en el ámbito de la función `wrapper()`. Esto se debe a que la función `wrapper()` es un cierre.