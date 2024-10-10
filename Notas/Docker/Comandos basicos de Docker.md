---
Fecha_creación: 2024-06-14
Categorias: "[[Docker]]"
tags:
  - Comandos_docker
URL:
---
### Para ver los contenedores en ejecución 
```bash
docker ps -it <imagen_name>
```


##### nombrar un [[Contenedor]]

```bash
docker run --name <container-name> <img_name>
```

##### Buscar un contenedor

```bash
docker ps -f "name=<nombre_contenedor"
```

#### Obtener mas información de los contenedores

```bash
docker ps -a "name=<nombre_contenedor"
```

#### Logs

```bash
docker logs <conteiner_id>
## Losg en tiempo real que se esta ejecutando

docker logs -f <container_id>
```

#### Eliminar un contenedor
```bash
# el contenedor debe haberse parado antes
docker rm <conteiner_id>
```