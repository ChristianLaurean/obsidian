---
Fecha_creación: 2024-07-14
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---

## Condicionales en Python

Los condicionales en Python son una herramienta fundamental para controlar el flujo de ejecución de un programa. Permiten tomar decisiones en función de ciertas condiciones, lo que hace que los programas sean más versátiles y adaptables a diferentes situaciones.

### Condición If

La sentencia `if` es la forma más básica de condicional en Python. Se utiliza para evaluar una condición y ejecutar un bloque de código si dicha condición se cumple. La sintaxis básica de la sentencia `if` es la siguiente:


```python
if condición:	
	print("código a ejecutar si la condición es verdadera")
```

Por ejemplo, el siguiente código verifica si un número es par:

```python
numero = 10
if numero % 2 == 0:	
	print(f"El número {numero} es par.")
```

En este caso, la condición `numero % 2 == 0` evalúa si el resto de dividir `numero` entre 2 es 0. Si la condición es verdadera, se ejecuta el bloque de código dentro del `if`, que imprime el mensaje "El número 10 es par."

### If Else

La sentencia `else` se utiliza para ejecutar un bloque de código alternativo en caso de que la condición especificada en la sentencia `if` no se cumpla. La sintaxis de la sentencia `if-else` es la siguiente:


```python
if condición:	
	print("código a ejecutar si la condición es verdadera")
else:	
	print("código a ejecutar si la condición es falsa")
```

Por ejemplo, el siguiente código verifica si un número es positivo o negativo:


```python
numero = -5
if numero > 0:	
	print(f"El número {numero} es positivo.")
else:	
	print(f"El número {numero} es negativo o cero.")
```

En este caso, si el número es positivo, se ejecuta el bloque de código dentro del `if`, que imprime el mensaje "El número -5 es positivo." Si el número es negativo o cero, se ejecuta el bloque de código dentro del `else`, que imprime el mensaje "El número -5 es negativo o cero."

### If Elif Else

La sentencia `elif` se utiliza para agregar condiciones adicionales a una estructura `if-else`. Permite evaluar varias condiciones en secuencia y ejecutar el bloque de código correspondiente a la condición que se cumpla. La sintaxis de la sentencia `if-elif-else` es la siguiente:


```Python
if condición1:	
	print("código a ejecutar si se cumple la condición1el")
if condición2:	
	print("código a ejecutar si se cumple la condición2")
elif condición3:	
	print("código a ejecutar si se cumple la condición3")
else:
	print("código a ejecutar si no se cumplen ninguna de las condiciones")
```

Por ejemplo, el siguiente código clasifica un número en las categorías "positivo", "negativo" o "cero":

```python
numero = 0
if numero > 0:	
	print(f"El número {numero} es positivo.")
elif numero < 0:	
	print(f"El número {numero} es negativo.")
else:
	print(f"El número {numero} es cero.")
```

En este caso, si el número es positivo, se ejecuta el bloque de código dentro del primer `if`. Si el número es negativo, se ejecuta el bloque de código dentro del `elif`. Si el número es cero, se ejecuta el bloque de código dentro del `else`.

### Operadores Lógicos

Los operadores lógicos se utilizan para combinar condiciones y formar expresiones más complejas. Los operadores lógicos más comunes en Python son:

- `and`: Se utiliza para evaluar si ambas condiciones son verdaderas.
- `or`: Se utiliza para evaluar si al menos una de las condiciones es verdadera.
- `not`: Se utiliza para negar una condición, es decir, convierte una condición verdadera en falsa y viceversa.

Por ejemplo, el siguiente código verifica si un número es par y mayor que 10:


```python
numero = 12
if numero % 2 == 0 and numero > 10:	
	print(f"El número {numero} es par y mayor a 10.")
```

En este caso, se utiliza el operador `and` para combinar las condiciones `numero % 2 == 0` y `numero > 10`. Si ambas condiciones son verdaderas, se ejecuta el bloque de código dentro del `if`, que imprime el mensaje "El número 12 es par y mayor a 10."

