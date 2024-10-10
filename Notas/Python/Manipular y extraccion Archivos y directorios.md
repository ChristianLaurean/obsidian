---
Fecha_creación: 2024-05-31
Categorias: "[[Extracción]]"
tags:
  - Programación
URL:
---
# Manejo de archivos

En Python, el manejo de archivos se puede realizar utilizando el módulo `open()`. Este módulo proporciona una serie de funciones que se pueden utilizar para abrir, leer, escribir y actualizar archivos.

## Abrir archivos para leer

Para abrir un archivo para leer, se utiliza la siguiente sintaxis:


```python
archivo = open(ruta_archivo, "r")
```

Donde:

- `archivo` es la variable que se utilizará para almacenar el objeto de archivo.
- `ruta_archivo` es la ruta al archivo que se desea abrir.
- `"r"` indica que el archivo se abrirá en modo de lectura.

Por ejemplo, el siguiente código abre el archivo `archivo.txt` en modo de lectura:

```python
archivo = open("archivo.txt", "r")
```

Una vez que se ha abierto un archivo, se puede leer su contenido utilizando el método `read()` del objeto de archivo. Este método devuelve una cadena con el contenido del archivo.

Por ejemplo, el siguiente código lee el contenido del archivo `archivo.txt` y lo imprime en la consola:


```python
archivo = open("archivo.txt", "r")
contenido_archivo = archivo.read()
print(contenido_archivo)
```

## Abrir archivos para escribir y actualizar[​](https://docs.z2h.online/docs/Roadmaps/Python/Manejo%20de%20archivos#abrir-archivos-para-escribir-y-actualizar "Direct link to Abrir archivos para escribir y actualizar")

Para abrir un archivo para escribir o actualizar, se utiliza la siguiente sintaxis:

```python
archivo = open(ruta_archivo, "w")
```

Donde:

- `archivo` es la variable que se utilizará para almacenar el objeto de archivo.
- `ruta_archivo` es la ruta al archivo que se desea abrir.
- `"w"` indica que el archivo se abrirá en modo de escritura.

Si el archivo no existe, se creará uno nuevo. Si el archivo existe, se sobrescribirá su contenido.

Por ejemplo, el siguiente código abre el archivo `archivo.txt` en modo de escritura y escribe la cadena "Hola mundo!" en el archivo:


```python
archivo = open("archivo.txt", "w")
archivo.write("Hola mundo!")
archivo.close()
```

Para actualizar el contenido de un archivo existente, se puede utilizar el modo `"a"`. Este modo abre el archivo en modo de escritura, pero el cursor se coloca al final del archivo.

Por ejemplo, el siguiente código abre el archivo `archivo.txt` en modo de actualización y agrega la cadena "¡Hasta luego!" al final del archivo:



```python
archivo = open("archivo.txt", "a")
archivo.write("¡Hasta luego!")
archivo.close()
```
# Mover archivos

```python
import shutil
# Tambien se puede renombrar el archivo cuando lo mueves
shutil.move(path_nombre_directorio, directorio_destino)
```


# Copiar archivos

```python
import shutil
# Tambien se puede renombrar el archivo
shutil.copy(path_nombre_directorio + nombre, directorio_destino + nombre)
```

# Eliminar directorios 

```python
import shutil
# eliminar directorios
shutil.rmtree(path_directorio)

```


