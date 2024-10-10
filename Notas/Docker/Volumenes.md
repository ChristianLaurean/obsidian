---
Fecha_creación: 2024-06-17
Categorias: "[[Docker]]"
tags:
  - Comandos_docker
URL:
---


Es un método que nos permite almacenar datos en docker que no esta relacionado con las [[imagen]] del [[Contenedor]] y del sistema de archivos del host.
- Se peude compartir los volumenes con varios [[Contenedor]]
![[Pasted image 20240617100420.png]]

### se crean

```bash
docker volume create <volumenes>

```

## Para usar el volumen con nuestro contenedor usamos

```bash
docker run  <v <name_volumnes>:destino_del_volumen
```
![[Pasted image 20240617101112.png]]
#### Ver lista de volumnes que tenemos

```bash
docker volume ls

docker volume list
```

#### Para ver información del volumen

```bash
docker volume inspect
```

## Eliminar un volumnes

```bash
docker volume rm
```