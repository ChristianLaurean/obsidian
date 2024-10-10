---
Fecha_creación: 2024-06-15
Categorias: "[[Docker]]"
tags:
  - Comandos_docker
URL:
---
##### exportar imagen
```Docker
docker save -o image.tar <nombre_img:version>
```


###### Cargar el archivo imagen

```bash
docker load -i image.tar
```
