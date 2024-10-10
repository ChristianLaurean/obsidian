---
Fecha_creación: 2024-06-14
Categorias: "[[Docker]]"
tags:
  - Concepto
URL:
---
Es un paquete con intrucciones inmutable que contiene todo lo necesario para un [[Contenedor]].


##### comando para ver todas mis imagenes
```docker
docker images
```

##### eliminar una imagen

```bash
docker image rm <img_name>
```

###### Elimina todas las imagenes y contenedores detenido


```bash
docker container prune -f
docker image prune -a
```.