---
Fecha_creación: 2024-05-31
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
## Definiendo funciones en Python

Las funciones son bloques de código que permiten reutilizar código y <span style="background:#fff88f">modularizar</span> los programas. Encapsulan una tarea o operación específica y se pueden llamar desde cualquier parte del programa.

### Declarando y llamando a una función

Para definir una función en Python, se usa la palabra clave `def` seguida del nombre de la función y paréntesis. Los paréntesis pueden contener parámetros, que son valores de entrada que la función necesita para realizar su tarea.


```Python
def nombre_funcion(parámetros):    # Cuerpo de la función
```

Una vez que se define una función, se puede llamar usando su nombre y paréntesis. Si la función tiene parámetros, se deben pasar los valores requeridos al llamarla.


```Python
nombre_funcion(valores_parámetros)
```

### Función sin parámetros
Una función puede existir sin ningún parámetro. En tales casos, los paréntesis están simplemente vacíos.


```Python
def saludar():    
	print("¡Hola!")saludar()
```

### Función que devuelve un valor - Parte 1

Las funciones pueden devolver valores usando la instrucción `return`. El valor devuelto por una función se puede almacenar en una variable o usarse directamente.


```Python
def cuadrado(número):    
	resultado = número * número    
	resultado_valor_cuadrado = cuadrado(5)print(valor_cuadrado)
	return resultado_valor_cuadrado
```

### Función con parámetros

Las funciones pueden tener parámetros para aceptar valores de entrada. Estos parámetros se enumeran dentro de los paréntesis en la definición de la función.


```python
def saludar(nombre):    
	print(f"¡Hola, {nombre}!")saludar("Juan")
```

### Pasar argumentos con clave y valor

Al llamar a una función con varios parámetros, se pueden usar argumentos con clave para asociar explícitamente cada argumento con su parámetro correspondiente.

```python
def formatear_nombre(primer_nombre, apellido):    
	nombre_completo = f"{primer_nombre} {apellido}"    
	return nombre_completo
	
nombre_formateado = formatear_nombre(apellido="Doe", primer_nombre="Juan")
print(nombre_formateado)
```

### Función que devuelve un valor - Parte 2

Las funciones pueden devolver varios valores empaquetándolos en una tupla o lista.

Python

```python
def calcular_área_y_perímetro(ancho, altura):
	área = ancho * altura    
	perímetro = 2 * (ancho + altura)    
	return área, perímetro
	
área_y_perímetro = calcular_área_y_perímetro(ancho=10, altura=5)
print("Área:", área_y_perímetro[0])
print("Perímetro:", área_y_perímetro[1])
```

### Función con parámetros predeterminados

Las funciones pueden tener parámetros predeterminados, que proporcionan valores para los parámetros si no se pasan valores al llamar a la función.

Python

```python
def saludar(nombre="Invitado"):
	print(f"¡Hola, {nombre}!")saludar()saludar("Juan")
```

### Número arbitrario de argumentos

Las funciones pueden aceptar un número arbitrario de argumentos usando el parámetro asterisco (*). Esto permite una entrada dinámica sin definir un número fijo de parámetros.

Python

```python
def imprimir_todo(*args):
	for arg in args:
        print(arg)
        
imprimir_todo(1, 2, 3, "Hola")
```

### Número arbitrario de parámetros y parámetros predeterminados

Las funciones pueden tener una combinación de parámetros predeterminados y un número arbitrario de argumentos usando tanto el parámetro asterisco (*) como otros parámetros con valores predeterminados.

Python

```python
def imprimir_con_prefijo(prefijo, *args):
	for arg in args:
        print(f"{prefijo}: {arg}")
        
imprimir_con_prefijo("Artículo", 1, 2, 3, "Hola")
```

### Función como parámetro de otra función[​](https://docs.z2h.online/docs/Roadmaps/Python/Funciones#funci%C3%B3n-como-par%C3%A1metro-de-otra-funci%C3%B3n "Direct link to Función como parámetro de otra función")

Las funciones se pueden pasar como parámetros a otras funciones. Esto permite la programación de orden superior y la creación de código más dinámico y reutilizable.


```python
def aplicar_función(función, argumento):
	return función(argumento)
	
def cuadrado(número):
	return número * número
	
resultado = aplicar_función(cuadrado)
```

# Docstrings

Lo usamos para poder describir lo que hace la función que acabamos de crear 

Para acceder a nuestros Docstrings usamos 
```python
nombre_funciones.__doc__
```

![[Pasted image 20240608100410.png]]
