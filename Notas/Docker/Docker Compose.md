---
Fecha_creación: 2024-06-17
Categorias: "[[Docker]]"
tags:
  - Comandos_docker
URL:
---
Es un archivo que podemos tener multiples [[Contenedor |contenedores]] y puede gestionar redes, [[Volumenes]]

`compose.yml`o `compose.yaml`
`docker-compose.yaml`


## ejemplo de un archivo
![[Pasted image 20240617111506.png]]

# iniciar una aplicación

```bash
docker compose up

docker compose -f <path_file> up

# ejecutar pero en backgroup
docker compose up -d
# mas antiguo
docker-compose up
```

### gestion del docker compose

Verificar el estado de una app

```bash
docker compose ls
```

### Cerrar o bajar el [[Docker Compose]]

```bash
docker compose down

docker compose -f <path_file> down

# mas antiguo
docker-compose down
```

# Crear un archivo

- Services: Enumera todos los contenedores necesarios para la aplicación
	- Contenedores y imágenes
```yml
services:
	posrgres:
	# nombre conteiner
		conteiner_name: postgres
		image: postgres:latest
		ports:
			- 5432:5432
```


	- 
- networks: Es opcional pero permite especificar las redes
- [[Volumenes]]: es opcional pero para definir el almacenamiento de los datos compartidos entre contenedores
- configs: Permite especificar detalles de configuración que otro modo requieren una nueva [[imagen]]
- secrets: permite al usuario configurar cualquier contraseña, tokens o [[APIS]]

# Dependencias

![[Pasted image 20240617115437.png]]

![[Pasted image 20240617115508.png]]