---
Fecha_creación: 2024-05-31
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
# Tipos de errores de Python


En Python, los errores se pueden clasificar en tres tipos principales:

- **Errores de sintaxis:** Estos errores ocurren cuando el código no está escrito de acuerdo con las reglas de sintaxis de Python. Por ejemplo, un error de sintaxis podría ser una falta de un punto y coma al final de una declaración.
    
- **Errores de semántica:** Estos errores ocurren cuando el código está escrito de acuerdo con las reglas de sintaxis, pero no tiene sentido. Por ejemplo, un error de semántica podría ser una declaración que intenta dividir por cero.
    
- **Errores de ejecución:** Estos errores ocurren cuando el código se ejecuta y no puede completarse correctamente. Por ejemplo, un error de ejecución podría ser un error de memoria o una excepción.
    

## Errores de sintaxis

Los errores de sintaxis se pueden identificar fácilmente por el compilador o intérprete de Python. Cuando se produce un error de sintaxis, el compilador o intérprete mostrará un mensaje de error que indica la ubicación del error y el tipo de error.

Por ejemplo, el siguiente código producirá un error de sintaxis:

```python
def mi_funcion() 
	print("Hola mundo!")
```

Este código producirá el siguiente mensaje de error:

```python
SyntaxError: expected ':' after 'def'
```

Los errores de sintaxis pueden ocurrir por una variedad de razones, como:

- **Uso incorrecto de los caracteres de puntuación**
- **Uso incorrecto de las palabras clave de Python**
- **Errores de ortografía**
- **Errores de indentación**

## Errores de semántica

Los errores de semántica pueden ser más difíciles de identificar que los errores de sintaxis. Estos errores a menudo se deben a una comprensión incorrecta de las reglas de Python o a errores lógicos en el código.

Por ejemplo, el siguiente código producirá un error de semántica:


```python
def mi_funcion(a, b):
	return a / bmi_funcion(5, 0)
```

Este código producirá el siguiente mensaje de error:

```
ZeroDivisionError: division by zero
```

Los errores de semántica pueden ocurrir por una variedad de razones, como:

- **Uso incorrecto de los tipos de datos**
- **Uso incorrecto de las operaciones matemáticas**
- **Uso incorrecto de las funciones**
- **Errores de lógica**

## Errores de ejecución

Los errores de ejecución pueden ocurrir por una variedad de razones, como errores de memoria, errores de tipo o errores de lógica.

Por ejemplo, el siguiente código producirá un error de ejecución:


```python
a = [1, 2, 3]
try:  
	a[5]
except IndexError:  
	print("El índice está fuera de rango")
```

Este código producirá el siguiente mensaje de error:

```
IndexError: list index out of range
```

Los errores de ejecución pueden ocurrir por una variedad de razones, como:

- **Acceso a una variable o elemento de lista fuera de rango**
- **Asignación de un valor de un tipo incorrecto a una variable**
- **Llamada a una función que no existe**
- **Errores en las operaciones matemáticas**

## Cómo evitar errores

La mejor manera de evitar errores es aprender las reglas de sintaxis y semántica de Python. También es importante revisar cuidadosamente el código antes de ejecutarlo.

Aquí hay algunos consejos para evitar errores:

- **Utilice un editor de código con resaltado de sintaxis.** Un editor de código con resaltado de sintaxis puede ayudar a identificar errores de sintaxis.
- **Use un compilador o intérprete que muestre mensajes de error útiles.** Un compilador o intérprete que muestra mensajes de error útiles puede ayudar a identificar errores de sintaxis y semántica.
- **Revise cuidadosamente el código antes de ejecutarlo.** Revise el código en busca de errores de lógica y errores gramaticales.

## Conclusión[​](https://docs.z2h.online/docs/Roadmaps/Python/Tipos%20de%20errores%20de%20Python#conclusi%C3%B3n "Direct link to Conclusión")

Los errores son una parte inevitable de la programación. Sin embargo, aprendiendo las reglas de sintaxis y semántica de Python y revisando cuidadosamente el código antes de ejecutarlo, puede ayudar a evitar errores.

**Extensión**

Además de los consejos mencionados anteriormente, aquí hay algunos consejos adicionales para evitar errores:

- **Use comentarios para explicar su código.** Los comentarios pueden ayudar a explicar el propósito de su código y pueden facilitar la comprensión de su código en el futuro.
- **Use pruebas para validar su código.** Las pruebas pueden ayudar a identificar errores en su código antes de que se produzcan en producción.

### Los errores mas comunes 

- TypeError: Sucede cuando le pasamos un tipo de datos que no es compatible con el programa
- ValueError: Esto sucede cuando tenemos un valor que no esta en el rango aceptable por ejemplo intentar cambiar un `str` a entero.

# Manejo de excepciones

## ¿Qué es el manejo de excepciones?
El manejo de excepciones es una forma de lidiar con los errores de ejecución. Cuando se produce una excepción, el flujo del programa se transfiere a un bloque `try`-`except`. El bloque `try` contiene el código que se puede ejecutar con seguridad. El bloque `except` contiene el código que se ejecuta si se produce una excepción.

## Cómo manejar excepciones[

Para manejar una excepción, se utiliza la siguiente sintaxis:


```python
try:  
# Código que puede producir una excepción
except <Excepción>:  
# Código que se ejecuta si se produce la excepción
```

Por ejemplo, el siguiente código muestra cómo manejar una excepción de índice fuera de rango:

```python
try:  
a = [1, 2, 3]
	print(a[5])
except IndexError:  
	print("El índice está fuera de rango")
```

Este código imprimirá el siguiente mensaje:

```
El índice está fuera de rango
```

## Tipos de excepciones[​](https://docs.z2h.online/docs/Roadmaps/Python/Manejo%20de%20excepciones#tipos-de-excepciones "Direct link to Tipos de excepciones")

En Python, existen muchos tipos diferentes de excepciones. Algunos de los tipos de excepciones más comunes son:

- **IndexError:** Se produce cuando se intenta acceder a un elemento de una lista o matriz fuera de rango.
- **KeyError:** Se produce cuando se intenta acceder a una clave en un diccionario que no existe.
- **ValueError:** Se produce cuando se proporciona un valor incorrecto a una función o método.
- **TypeError:** Se produce cuando se usa un tipo de datos incorrecto en una operación.
- **ZeroDivisionError:** Se produce cuando se intenta dividir por cero.

## Excepciones personalizadas

También es posible crear excepciones personalizadas. Para crear una excepción personalizada, se utiliza la siguiente sintaxis:



```python
class MiExcepcion(Exception):  
	pass
```

Por ejemplo, el siguiente código crea una excepción personalizada llamada `MiExcepcion`:


```python
class MiExcepcion(Exception):  
	pass
	try:  
		raise MiExcepcion("Esto es una excepción personalizada") 
	except MiExcepcion as e:  
		print(e)
```

Este código imprimirá el siguiente mensaje:

```
Esto es una excepción personalizada
```

`try` Intenta ejecutar el cogido
`except` Si pasa algo malo, mejor haz otra cosa
`finaly` No importa si hay un error, ejecuta esto

```Python
try:
	codigo_queremos_probar
except:
	#Codigo_ejecutar si no hay error
else: 
	# Ejecutar si no hay error
finally:
	#Codigo que se va a ejecutar todos modos
```

Necesitamos que se pare el procesamiento de datos cuando un archivo sea 0 para eso usamos `raise`

```python
if dasda =! adsad:
	raise NameError('Mensaje que quieras')
# Lo podemos usar en una función y despues usar Try: Except
# ---------------
```


