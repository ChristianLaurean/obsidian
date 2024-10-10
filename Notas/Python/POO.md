---
Fecha_creación: 2024-07-16
Categorias: "[[Python]]"
tags:
  - Programación
URL: https://docs.z2h.online/docs/Roadmaps/Python/Clases%20y%20objetos
---
La programación orientada a objetos es una excelente manera de escribir [[Codigo Modular]] 


## ¿Qué son las clases y objetos?[​](https://docs.z2h.online/docs/Roadmaps/Python/Clases%20y%20objetos#qu%C3%A9-son-las-clases-y-objetos "Direct link to ¿Qué son las clases y objetos?")

En Python, las clases y los objetos son dos conceptos fundamentales de la programación orientada a objetos.

### **Clase**

Una clase es un tipo de dato que define las características y el comportamiento de un objeto.

### **Objeto**

Un objeto es una instancia de una clase.

## Creando una clase

Para crear una clase, se utiliza la palabra clave `class`.
<font color="#ffff00">Las clases nunca deben de tener guiones bajos</font>

```python
class MyClase:
	""" un ejemplo minimo de la clase
	:param value: 
	:ivar attribute:
	"""

```

Este código crea una clase llamada `Clase`.

## Creando un objeto

Para crear un objeto, se utiliza el operador `()`.


```python
objeto = Clase()
```

Este código crea un objeto llamado `objeto` de la clase `Clase`.

## Constructor de clases

El constructor de clases es un método especial que se ejecuta cuando se crea un objeto.

```python
class Clase:
	def __init__(self, nombre, edad):
	        self.nombre = nombre
	        self.edad = edad
	        
objeto = Clase("Juan", 30)
print(objeto.nombre)
```

Este código crea un objeto llamado `objeto` de la clase `Clase`. El constructor de la clase establece el nombre del objeto a "Juan" y la edad del objeto a 30.

###### importar mi clase a otro archivo

```python
from .my_class import MyClass
```

##### instanciando mi clase

```python
import mi_paquete

my_instance = mi_paquete.MyClass(value='aaaa')
# Queremos instanciar nuestra clase usando el metodo init
```

#### ¿Qué es el `_aaa`?
Es para poder decirle que es un metodo privado 

```python

```

## Métodos de objetos

Los métodos son funciones que se asocian a un objeto.

```python
class Clase:
	def __init__(self, nombre, edad):
	    self.nombre = nombre        
	    self.edad = edad    
	def saludar(self):        
		print("Hola, mi nombre es", self.nombre)
		
		
objeto = Clase("Juan", 30)
objeto.saludar()
```

Este código crea un objeto llamado `objeto` de la clase `Clase`. El método `saludar()` imprime el nombre del objeto.

## Métodos predeterminados de objetos

Los objetos tienen una serie de métodos predeterminados que se pueden utilizar para acceder a sus propiedades y métodos.


```python
class Clase:
	def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
        
objeto = Clase("Juan", 30)
print(objeto.nombre)
print(objeto.edad)
```

Este código imprime el nombre y la edad del objeto.

## Método para modificar los valores predeterminados de clase

Se puede utilizar el método `setattr()` para modificar los valores predeterminados de clase.

```python
class Clase:
	def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
        
Clase.nombre_clase = "Mi clase"
objeto = Clase("Juan", 30)
print(objeto.nombre_clase)
```

Este código imprime el nombre de la clase.

## Herencia
La herencia es una característica de la programación orientada a objetos que permite crear clases a partir de otras clases.

Python

```
class Animal:    def __init__(self, nombre):        self.nombre = nombre    def hablar(self):        print("Soy un animal y no sé hablar")class Perro(Animal):    def __init__(self, nombre, raza):        super().__init__(nombre)        self.raza = raza    def ladrar(self):        print("Guau!")objeto_perro = Perro("Perrito", "Pastor alemán")objeto_perro.hablar()objeto_perro.ladrar()
```

Este código crea una clase llamada `Animal`. La clase `Perro` hereda de la clase `Animal`. El método `ladrar()` se define en la clase `Perro`.

## Anulando el método principal

El método principal, también conocido como método `__init__()`, se ejecuta cuando se crea un objeto. Se puede anular el método principal para realizar acciones específicas cuando se crea un objeto.

Python

```
class Clase:    def __init__(self, nombre, edad):        self.nombre = nombre        self.edad = edad    def __init__(self):        print("Se ha creado un objeto de la clase Clase")objeto = Clase()
```

Este código imprime el mensaje "Se ha creado un objeto de la clase Clase" cuando se crea el objeto `objeto`.

### Ejemplo de herencia

Python

```
class Animal:    
```

