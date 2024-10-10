---
Fecha_creación: 2024-06-15
Categorias: "[[Docker]]"
tags:
  - Comandos_docker
URL:
---

Un Dockerfile es un archivo de texto plano que contiene una serie de instrucciones utilizadas por Docker para construir de manera automatizada una imagen Docker

- Docker ejecuta su contenido de arriaba para abajo 
- La primera linea siempre sera el `FROM`

# Dockerfile archivo
### `FROM`

Indica desde que imagen comenzamos a construir 

`FROM postgres:15.5`

# `RUN`

- Nos permite ejecutar cualquier comando de la [[Shell]] mientras se construye la [[imagen]]
Ejemplo

![[Pasted image 20240615093249.png]]

# Agregar archivos a nuestras imagenes

`COPY <path_archivo_nombre_archivo> <path_ruta_destino>

![[Pasted image 20240615094557.png]]

> [!warning] si no especificamos el nombre de archivo en la ruta de origen, entonces en lugar de un solo archivo se trae todo incluidas subcarpetas

# agregar comandos anidados

![[Pasted image 20240615095245.png]]

## Que comandos queremos que inicie despues de crear la img

`CMD <shell_command>` acepta un solo parametro

Ejemplo


![[Pasted image 20240615103323.png]]

### remplazar el comando `CMD` cuando creamos un contenedor

`docker run -it <img> <shell_comman>
### Crear la imagen

```bash
docker build path_donde_se_encuentra_el_Dockerfile
# o si el dockerfile esta en nueestro folder

docker build .
```

## Agregar un nombre a nuestra imagen

```bash
docker build -t <nombre_img:version> .
```
