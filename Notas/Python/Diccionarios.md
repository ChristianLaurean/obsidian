---
Fecha_creación: 2024-05-31
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
# Diccionarios

Un diccionario en Python es una estructura de datos que almacena pares clave-valor. Cada clave es única y se utiliza para acceder al valor asociado. Los diccionarios son muy versátiles y se utilizan comúnmente para mapear información. Aquí tienes un curso completo sobre diccionarios en Python:



### 1.2 Crear un diccionario

Puedes crear un diccionario utilizando llaves `{}` o la función `dict()`. Por ejemplo:

```python
mi_diccionario = {}
mi_diccionario = dict()
```

### 1.3 Añadir elementos

Puedes agregar elementos a un diccionario especificando una clave y un valor:

```python
mi_diccionario['clave'] = 'valor'
```

### 1.4 Acceder a elementos

Puedes acceder a un valor utilizando su clave:

```python
print(mi_diccionario['clave'])  # Imprimirá 'valor'
```

## Lección 2: Operaciones con diccionarios[​](https://docs.z2h.online/docs/Roadmaps/Python/Diccionarios#lecci%C3%B3n-2-operaciones-con-diccionarios "Direct link to Lección 2: Operaciones con diccionarios")

### 2.1 Modificar valores

Puedes modificar el valor asociado a una clave:

```python
mi_diccionario['clave'] = 'nuevo_valor'
```

### 2.2 Eliminar elementos

Puedes eliminar un elemento de un diccionario utilizando `del`:

```python
del mi_diccionario['clave']
```

### 2.3 Verificar la existencia de una clave

Puedes comprobar si una clave existe en un diccionario:

```python
if 'clave' in mi_diccionario:	
	print("La clave existe")
```

### 2.4 Obtener todas las claves y valores

Puedes obtener todas las claves y valores de un diccionario utilizando los métodos `keys()` y `values()`:

```python
claves = mi_diccionario.keys()valores = mi_diccionario.values()
```

### 2.5 Iterar sobre un diccionario

Puedes recorrer un diccionario utilizando bucles `for`:

```python
for clave in mi_diccionario:	
	valor = mi_diccionario[clave]	
	print(f'Clave: {clave}, Valor: {valor}')
```

## Lección 3: Métodos útiles

### 3.1 Método `get()`

El método `get()` te permite obtener un valor por clave de forma segura sin generar un error si la clave no existe:

```python
valor = mi_diccionario.get('clave', 'valor_por_defecto')
```

### 3.2 Método `update()`

El método `update()` te permite combinar dos diccionarios:

```python
mi_diccionario.update(otro_diccionario)
```

### 3.3 Método `pop()`

El método `pop()` elimina un elemento y devuelve su valor:

```python
valor = mi_diccionario.pop('clave')
```

## Lección 4: Diccionarios anidados[​](https://docs.z2h.online/docs/Roadmaps/Python/Diccionarios#lecci%C3%B3n-4-diccionarios-anidados "Direct link to Lección 4: Diccionarios anidados")

Puedes crear diccionarios anidados, donde un valor puede ser otro diccionario:

```python
mi_diccionario_anidado = {	
	'clave1': {		
		'subclave1': 'valor1',
		'subclave2': 'valor2'	
		},	
	'clave2': {		
		'subclave1': 'valor3',
		'subclave2': 'valor4'	
		}
}
```


## Lección 5: Comprehension de diccionarios

Puedes crear diccionarios utilizando comprehensions:

```python
mi_diccionario = {clave: valor for clave, valor in lista_de_pares}
```

## Lección 6: Uso de diccionarios en la práctica[​](https://docs.z2h.online/docs/Roadmaps/Python/Diccionarios#lecci%C3%B3n-6-uso-de-diccionarios-en-la-pr%C3%A1ctica "Direct link to Lección 6: Uso de diccionarios en la práctica")

Los diccionarios son ampliamente utilizados en Python para tareas como:

- Configuración de aplicaciones.
- Almacenar datos estructurados en bases de datos NoSQL.
- Representar JSON en aplicaciones web.
- Contar ocurrencias de elementos en una lista o secuencia.
- Mapear información en juegos y simulaciones.

¡Espero que este curso te ayude a comprender los diccionarios en Python y cómo usarlos eficazmente en tus proyectos!