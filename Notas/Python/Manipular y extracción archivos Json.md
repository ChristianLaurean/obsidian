---
Fecha_creación: 2024-05-31
Categorias: "[[Extracción]]"
tags:
  - Programación
URL:
---
# JSON

## Archivo con extensión json

Para leer un archivo JSON, se puede utilizar el módulo `json`. Este módulo proporciona una serie de funciones que se pueden utilizar para leer y escribir datos JSON.

La función `load()` del módulo `json` se puede utilizar para leer datos JSON de un archivo. Esta función devuelve un objeto JSON.

Por ejemplo, el siguiente código lee el contenido del archivo `archivo.json` y lo imprime en la consola:


```python
import json
archivo = open("archivo.json", "r")datos_json = json.load(archivo)print(datos_json)
```

Este código imprimirá el siguiente mensaje:

```
{  "nombre": "Juan",  "edad": 30,  "profesion": "Ingeniero de software"}
```

Para escribir un archivo JSON, se puede utilizar la función `dump()` del módulo `json`. Esta función escribe datos JSON en un archivo.

Por ejemplo, el siguiente código escribe el objeto JSON `datos_json` en el archivo `archivo.json`:

Python

```
import jsondatos_json = {  "nombre": "Juan",  "edad": 30,  "profesion": "Ingeniero de software"}archivo = open("archivo.json", "w")json.dump(datos_json, archivo)archivo.close()
```

Este código creará el archivo `archivo.json` con el siguiente contenido:

```
{  "nombre": "Juan",  "edad": 30,  "profesion": "Ingeniero de software"}
```

## Cambiar JSON a Diccionario[​](https://docs.z2h.online/docs/Roadmaps/Python/Manejo%20de%20archivos#cambiar-json-a-diccionario "Direct link to Cambiar JSON a Diccionario")

Para convertir un objeto JSON a un diccionario, se puede utilizar la función `loads()` del módulo `json`. Esta función devuelve un diccionario con los datos JSON.



>[!tip] Es un formato ligero para su almacenamiento de información 
>Con este nos podemos enviar como recibir información
>Podemos persistir información
>Es como un [[Diccionarios]]


## Convertir el objetos json a diccionario

```python
import json

json_file = {}
user = json.loads(json_file)# recibe el objeto json y lo convierte en diccionario
```

## Diccionario a un objeto json

```python
import json

dict_file = {
	'name':'chris',
	'email':'email@gma.cpm'
}

json_object = json.dumps(dict_file)# retorna un string
```

## Leer archivos con extensión .json

```python
import json

with open('file_json') as file:
	payload = json.load(file)# convertimos el objeto json a diccionario 
```

## Crear archivos Json

```python
import json

with open('file_json.json', w) as file:
	json.dump(lista_diccionario,file, indent=2)
```


