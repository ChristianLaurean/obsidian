---
Fecha_creación: 2024-06-17
Categorias: "[[Docker]]"
tags:
  - comandos_linux
URL:
---


Normalmente la comunicación se maneja exponiendo los puertos de contenedores al [[Host]] y actúa como una traducción entre ellos.

Los contenedores pueden tener sus propias [[IP]]

```bash
ifconfig <interface>
ip addr show docker0



ping -c 3 myhost
Para ver mi conectividad
```
Para ver las [[interface]] y [[IP]] asignadas

# Ver networks que tengo

```docker
docker networks -ls
```

# Crear una network 

```docker
docker network create <name_Network>
```


#### Para conectar la [[Network]] a un contenedor podemos hacer esto:

```docker
docker run -itd --network=<name_Network> --name <elquequieras>
```
