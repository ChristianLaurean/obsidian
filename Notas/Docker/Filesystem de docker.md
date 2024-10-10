---
Fecha_creación: 2024-06-17
Categorias: "[[Docker]]"
tags:
  - Concepto
URL:
---
Cada instancia de [[Contenedor]] tiene su propio sistema de archivos que se basa en la [[imagen]] con la que se creo.

Se pueden hacer cambios en el sistema pero solo están vinculados a ese [[Contenedor]]

![[Pasted image 20240617094625.png]]

Para que los otros contenedores tengan puedan tener el mismo sistema podemos adjuntar archivos o directorios desde el sistema host hasta el contenedor

- Sirve para la persistencia de los datos por ejemplo
	- archivos de Configuraciones
	- archivos de bases de datos

# bind-mount

- El host no puede acceder a los archivos o directorios hasta que se cierre el contenedor que lo utiliza
Lo creamos 

```bash
-v <source>:<destino_contenedor>
```
si hacemos esto no podra ser visible

![[Pasted image 20240617095438.png]]
