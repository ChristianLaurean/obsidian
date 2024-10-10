---
Fecha_creación: 2024-05-31
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
# Cadenas

Las cadenas, también conocidas como _strings_, son secuencias de caracteres encerrados entre comillas simples ('') o comillas dobles (""). Las cadenas son una parte fundamental de la programación, ya que nos permiten representar y manipular texto de manera eficiente.

En Python, las cadenas son objetos inmutables, lo que significa que no se pueden modificar después de haber sido creadas. Sin embargo, podemos realizar diversas operaciones y métodos en ellas para trabajar con ellas de diferentes formas.

A continuación, veremos algunos ejemplos que te ayudarán a comprender mejor cómo trabajar con cadenas en Python.

Recuerda que puedes hacer uso de operaciones como concatenación, indexación, rebanado, entre otras, para manipular cadenas de texto en Python. Pero poco a poco iras aprendiendo todo esto así que ten paciencia.

### Aquí tienes varios ejemplos de manipulación de cadenas en Python:

```python
# Ejemplo 1: Creación de una cadena
cadena1 = "Hola, mundo!"  # Una cadena entre comillas dobles
cadena2 = '¡Bienvenidos!'  # Una cadena entre comillas simples

# Ejemplo 2: Concatenación de cadenas
nombre = "Alice"
saludo = "¡Hola, " + nombre + "!"
print(saludo)  # Salida: ¡Hola, Alice!

# Ejemplo 3: Indexación de cadenas
fruta = "manzana"
print(fruta[0])  # Salida: m
print(fruta[-1])  # Salida: a

# Ejemplo 4: Rebanado de cadenas
mensaje = "Python es genial"
print(mensaje[0:6])  # Salida: Python
print(mensaje[7:])  # Salida: es genial

# Ejemplo 5: Longitud de una cadena
palabra = "Hello"
print(len(palabra))  # Salida: 5

# Ejemplo 6: Métodos de cadenas
texto = "Hola, mundo!"
print(texto.upper())  # Salida: HOLA, MUNDO!
print(texto.lower())  # Salida: hola, mundo!
print(texto.replace("Hola", "Adiós"))  # Salida: Adiós, mundo!

```

### Estos ejemplos te muestran algunas operaciones básicas que puedes realizar con cadenas en Python.

```python
# Ejemplo 1: Concatenación de cadenas
nombre = "Alice"
apellido = "Smith"
nombre_completo = nombre + " " + apellido
print(nombre_completo)  # Salida: Alice Smith

# Ejemplo 2: Acceso a caracteres individuales
mensaje = "Hola, mundo!"
primer_caracter = mensaje[0]
ultimo_caracter = mensaje[-1]
print(primer_caracter)  # Salida: H
print(ultimo_caracter)  # Salida: !

# Ejemplo 3: Rebanado de cadenas
texto = "Python es genial"
subcadena1 = texto[0:6]
subcadena2 = texto[7:]
print(subcadena1)  # Salida: Python
print(subcadena2)  # Salida: es genial

# Ejemplo 4: Longitud de una cadena
palabra = "Hello"
longitud = len(palabra)
print(longitud)  # Salida: 5

# Ejemplo 5: Métodos de cadenas
mensaje = "Hola, mundo!"
mayusculas = mensaje.upper()
minusculas = mensaje.lower()
reemplazo = mensaje.replace("Hola", "Adiós")
print(mayusculas)  # Salida: HOLA, MUNDO!
print(minusculas)  # Salida: hola, mundo!
print(reemplazo)  # Salida: Adiós, mundo!

# Ejercicio 1: Solicitar nombre y apellido al usuario y mostrarlo en mayúsculas
nombre = input("Ingresa tu nombre: ")
apellido = input("Ingresa tu apellido: ")
nombre_completo = nombre.upper() + " " + apellido.upper()
print("Nombre completo en mayúsculas:", nombre_completo)

# Ejercicio 2: Contar la cantidad de caracteres en una cadena
texto = input("Ingresa un texto: ")
cantidad_caracteres = len(texto)
print("Cantidad de caracteres:", cantidad_caracteres)

# Ejercicio 3: Reemplazar una palabra en una frase
frase = "Python es genial"
palabra_buscada = "genial"
palabra_reemplazo = "increíble"
frase_modificada = frase.replace(palabra_buscada, palabra_reemplazo)
print("Frase modificada:", frase_modificada)
```
