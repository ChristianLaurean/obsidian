---
Fecha_creación: 2024-06-14
Categorias: "[[Docker]]"
tags:
  - Concepto
URL:
---

Es una unidad de [[Software]] que contiene todo lo necesario para correr una aplicación de forma independiente.

- Estandarización
    - Nos permite portabildiad bajo cualquier entorno.
- Ligeros
    - Por que los contenedores que virtualizan por completo todo el S.O si no que solo hace uso de su [karnel](app://obsidian.md/karnel)
- Seguros
    - Contiene un entorno de aislamiento que permite que una aplicación solo haga uso de todo lo que esta adentro de ese contenedor.
##### Iniciar un contenedor desde una [[imagen]]

```bash
docker run <imagen_name>
```
## Acceder a un contenedor que esta corriendo

```bash
docker exec -it mi_postgres psql -U postgres
```
##### Ejecutar una imagen en segundo plano

```bash
docker run -d <imagen_name>
```
## Ejemplo creando un contenedor de postgresql


`-e` Para agregar variables de entorno 
`--name` nombre_contenedor
`-v` [[Volumenes]]
`-i` mantiene la entrada a estándar para que puedas interactuar con el contenedor
`-t` Asigna una terminal virtual del contenedor
`-it` 
```
docker run -it \
  -e POSTGRES_USER="root" \
  -e POSTGRES_PASSWORD="root" \
  -e POSTGRES_DB="ny_taxi" \
  -v $(pwd)/nyc-tlc-data:/var/lib/postgresql/data \
  -p 5432:5432 \
  postgres:13
```

# detener un contenedor 

```bash
docker stop code_contenedor_or_name
```

### crear un contenedor y que se elimine despues de ejecutarse

```bash
docker run --rm
```

## Eliminar un [[Contenedor]]

```
docker rm <container_id>
```

## Encender un contenedor apagado

```bash
docker start <name_conteiner>
```
