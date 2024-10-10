---
Fecha_creación: 2024-07-14
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---

## ¿Qué es un módulo?

Un módulo es un archivo Python que contiene código reutilizable, como funciones, clases y variables. Los módulos permiten organizar el código de manera modular y eficiente, promoviendo la reutilización y evitando la duplicación de código.

## Crear un módulo

Para crear un módulo, simplemente guarde el código Python deseado en un archivo con la extensión .py. Por ejemplo, si desea crear un módulo llamado `funciones_utiles.py`, guarde el siguiente código en un archivo con ese nombre:



```python
# Función para saludar a una persona
def saludar(nombre):
    print(f"¡Hola, {nombre}!")

# Función para sumar dos números
def sumar(a, b):
    return a + b

# Función para multiplicar dos números
def multiplicar(a, b):
    return a * b

```

Este módulo contiene tres funciones: `saludar`, `sumar` y `multiplicar`.

## Importar un módulo

Para importar un módulo en otro archivo Python, utilice la instrucción `import`. Por ejemplo, para importar el módulo `funciones_utiles.py` en un archivo llamado `principal.py`, utilice la siguiente instrucción:



```python
import funciones_utiles
```

Esta instrucción importará el módulo completo, incluyendo todas las funciones definidas dentro del mismo.

## Importar funciones específicas de un módulo

También es posible importar solo funciones específicas de un módulo. Para ello, utilice la instrucción `from` seguida del nombre del módulo y una lista entre paréntesis de las funciones a importar. Por ejemplo, para importar las funciones `saludar` y `sumar` del módulo `funciones_utiles.py`, utilice la siguiente instrucción:


```python
from funciones_utiles import saludar, sumar
```

## Importar y renombrar funciones de un módulo

En ocasiones, es útil importar funciones de un módulo y asignarles nombres diferentes para evitar conflictos con nombres existentes en el programa principal. Para ello, utilice la instrucción `import` seguida del nombre del módulo y una lista entre paréntesis donde se especifique el nombre original de la función y el nombre nuevo que se le asignará. Por ejemplo, para importar la función `saludar` del módulo `funciones_utiles.py` y renombrarla como `imprimir_saludo`, utilice la siguiente instrucción:



```Python
import funciones_utiles as fu
imprimir_saludo = fu.saludar
```

## Importar módulos incorporados

Python proporciona una amplia gama de módulos incorporados que ofrecen funcionalidades generales, como acceso a archivos y directorios, operaciones matemáticas, manipulaciones de cadenas y generación de números aleatorios.

## Módulo OS

El módulo `os` proporciona funciones para interactuar con el sistema operativo, como crear directorios, eliminar archivos, obtener información del sistema y ejecutar comandos del sistema.

Por ejemplo, para crear un directorio llamado `nuevo_directorio` en el directorio actual, puede utilizar la siguiente función:



```python
import os
os.mkdir("nuevo_directorio")
```

Para eliminar el archivo `archivo.txt` del directorio actual, puede utilizar la siguiente función:


```Python
import os
os.remove("archivo.txt")
```

Para obtener la ruta del directorio actual, puede utilizar la siguiente función:


```Python
import os
ruta_actual = os.getcwd()
```

Para obtener la lista de archivos y directorios en el directorio actual, puede utilizar la siguiente función:


```Python
import os
lista_archivos = os.listdir()
```

Para ejecutar el comando `ls` en la terminal, puede utilizar la siguiente función:



```Python
import os
os.system("ls")
```

## Módulo Sys[​](https://docs.z2h.online/docs/Roadmaps/Python/M%C3%B3dulos#m%C3%B3dulo-sys "Direct link to Módulo Sys")

El módulo `sys` proporciona acceso a información del sistema y funciones para interactuar con el intérprete de Python, como obtener la ruta del script actual, acceder argumentos de la línea de comandos y salir del intérprete.

Por ejemplo, para obtener la ruta del script actual, puede utilizar la siguiente función:


```Python
import sys
ruta_script = sys.argv[0]
```

Para acceder al primer argumento de la línea de comandos, puede utilizar la siguiente función:


```Python
import sys
argumento_1 = sys.argv[1]
```

Para salir del intérprete, puede utilizar la siguiente función:


```Python
import syssys.exit()
```

## Módulo Statistics

El módulo `statistics` proporciona funciones para calcular estadísticas básicas, como media, mediana, desviación estándar y varianza.

Por ejemplo, para calcular la media de una lista de números, puede utilizar la siguiente función:


```Python
import statistics
lista_numeros = [1, 2, 3, 4, 5]
media = statistics.mean(lista_numeros)
```

Para calcular la mediana de una lista de números, puede utilizar la siguiente función:



```Python
import statistics
lista_numeros = [1, 2, 3, 4, 5]
mediana = statistics.median(lista_numeros)
```

Para calcular la desviación estándar de una lista de números, puede utilizar la siguiente función:


```Python
import statistics
lista_numeros = [1, 2, 3, 4, 5]
desviacion_estandar = statistics.stdev(lista_numeros)
```

Para calcular la varianza de una lista de números, puede utilizar la siguiente función:


```Python
import statistics
lista_numeros = [1, 2, 3, 4, 5]
varianza = statistics.variance(lista_numeros)
```

#  **Módulo [[strings]]**

El módulo `string` proporciona funciones para manipular cadenas, como eliminar espacios en blanco, convertir a mayúsculas o minúsculas y buscar patrones dentro de cadenas.

Por ejemplo, para eliminar todos los espacios en blanco de una cadena, puede utilizar la siguiente función:



```python
import string
cadena = "  Hola, mundo!  "
cadena_sin_espacios = string.strip(cadena)
```

Para convertir una cadena a mayúsculas, puede utilizar la siguiente función:


```Python
import string
cadena = "hola, mundo!"
cadena_mayusculas = string.upper(cadena)
```

## **Módulo `random`**

El módulo `random` proporciona funciones para generar números aleatorios, como números enteros aleatorios, números decimales aleatorios y elementos aleatorios de una lista o secuencia.

Por ejemplo, para generar un número entero aleatorio entre 1 y 10, puede utilizar la siguiente función:


```Python
import random
numero_aleatorio = random.randint(1, 10)
```

Para generar un número decimal aleatorio entre 0 y 1, puede utilizar la siguiente función:


```Python
import random
numero_aleatorio = random.random()
```

Para generar un elemento aleatorio de una lista, puede utilizar la siguiente función:



```Python
import random
lista = [1, 2, 3, 4, 5]
elemento_aleatorio = random.choice(lista)
```

Estos son solo algunos ejemplos de cómo utilizar módulos en Python. Con un poco de práctica, podrás dominar el uso de módulos para crear código más eficiente y reutilizable.

