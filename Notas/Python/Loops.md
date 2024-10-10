---
Fecha_creación: 2024-05-31
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
## Bucles en Python

Los bucles o loops en Python son una herramienta esencial para repetir un bloque de código un número determinado de veces o hasta que se cumpla una determinada condición. Permiten realizar tareas repetitivas de manera eficiente y organizada, ahorrando tiempo y esfuerzo en la programación.

### Bucle While

El bucle `while` se utiliza para ejecutar un bloque de código repetidamente mientras una condición específica se cumpla. La sintaxis básica del bucle `while` es la siguiente:



```python
while condición:    
	print("código a ejecutar mientras la condición sea verdadera")
```

Por ejemplo, el siguiente código imprime los números del 1 al 5:


```python
numero = 1
while numero <= 5:
	print(numero)    
	numero += 1
```

En este caso, la condición `numero <= 5` evalúa si el valor de la variable `numero` es menor o igual a 5. Mientras la condición sea verdadera, se ejecuta el bloque de código dentro del `while`, que imprime el valor de `numero` y luego lo incrementa en 1. El bucle se repite hasta que el valor de `numero` sea mayor que 5.

### Break y Continue - Parte 1

La sentencia `break` se utiliza para salir de un bucle antes de que finalice su ejecución normal. Es útil cuando se quiere detener el bucle en una condición específica o para evitar que se repita innecesariamente.

La sentencia `continue` se utiliza para omitir el resto de las iteraciones actuales del bucle y continuar con la siguiente iteración. Es útil cuando se quiere filtrar los elementos que no cumplan con una condición específica dentro del bucle.

Por ejemplo, el siguiente código imprime los números pares del 1 al 10, pero omite los números múltiplos de 3:


```python
numero = 1
while numero <= 10:
	if numero % 2 != 0 or numero % 3 == 0:
	        continue    
	print(numero)    
	numero += 1
```

En este caso, la primera condición `numero % 2 != 0` evalúa si el número es impar. Si es impar, se omite el resto de la iteración actual y se continúa con la siguiente. La segunda condición `numero % 3 == 0` evalúa si el número es múltiplo de 3. Si es múltiplo de 3, también se omite el resto de la iteración actual y se continúa con la siguiente. Si ambas condiciones son falsas, se imprime el valor de `numero` y luego se incrementa en 1. El bucle se repite hasta que el valor de `numero` sea mayor que 10.

### Bucle For

El bucle `for` se utiliza para iterar sobre una secuencia de elementos, como una lista o un rango de números. La sintaxis básica del bucle `for` es la siguiente:


```python
for elemento in secuencia:
	print("código a ejecutar para cada elemento de la secuencia")
```

Por ejemplo, el siguiente código imprime los elementos de una lista:


```python
lista = [1, 2, 3, 4, 5]
for numero in lista:    
	print(numero)
```

En este caso, el bucle itera sobre la lista [[Listas]], asignando cada elemento a la variable `numero` en cada iteración. El bloque de código dentro del `for` se ejecuta una vez para cada elemento de la lista, imprimiendo el valor de `numero` en cada iteración.

# Bucles mas efiecientes

Cuando tenemos procesos que no cambian dentro del bucle es mejor moverlos para arriba o abajo, sacarlos de bucle

