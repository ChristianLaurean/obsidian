---
Fecha_creación: 2024-08-26
Categorias: "[[Python]]"
tags:
  - Entorno
URL:
---
**¿Qué es Poetry?**  
Poetry es una herramienta para la gestión de dependencias y la configuración de entornos virtuales en Python, que también permite gestionar versiones, publicar paquetes, y más.


#### **Instalación de Poetry**

- **Requisitos Previos**  
    Asegúrate de tener Python 3.7 o superior instalado.
    
- **Instalación**  
    Puedes instalar Poetry usando el siguiente comando en tu terminal:
	    `pip install poetry`
	    
- **Verificación**  
	Verifica que Poetry esté correctamente instalado ejecutando:
		`poetry --version`

#### **Creación de un Proyecto con Poetry**

- **Inicializar un Proyecto**  
    Para crear un nuevo proyecto con Poetry, navega a la carpeta donde quieras crear el proyecto y ejecuta:

	`poetry init` 
	o
    `poetry new nombre_proyecto`
    
    Esto creará una estructura básica de proyecto con un archivo `pyproject.toml` y otros archivos esenciales.
### Instalar dependencias

- `poetry add pandas` 
#### Quitar Dependencias

`poetry remove pandas`

#### instalar un proyecto que tengamos en poetry

`poetry install` 

##### iniciar el interno 

`poetry shell` 