---
Fecha_creación: 2024-06-14
Categorias: "[[Docker]]"
tags:
  - Concepto
URL:
---

Es una plataforma de código abierto que gestiona [[Contenedor]] y [[imagen |imagenes]]

## ¿Como funciona docker por dentro?

1. **Docker Daemon**:
    
    - Primero, Docker verifica que el servicio `dockerd` (Docker Daemon) esté corriendo. Este daemon es responsable de administrar y ejecutar contenedores Docker en tu sistema.

2. **Descarga de la Imagen**:
    
    - Si la imagen `hello-world` no está presente localmente en tu sistema, Docker procederá a descargarla desde Docker Hub (el registro de imágenes Docker públicas) u otro registro de imágenes configurado.

3. **Creación y Ejecución del Contenedor**:
    
    - Una vez que Docker tiene la imagen `hello-world` disponible localmente (o después de descargarla), procede a crear un contenedor basado en esta [[imagen]].

    - El contenedor creado a partir de `hello-world` es extremadamente simple y está diseñado únicamente para mostrar un mensaje de prueba para verificar que Docker está funcionando correctamente.


4. **Mensaje de Salida**:
    
    - El contenedor `hello-world` muestra un mensaje en la salida estándar (stdout) del terminal. Este mensaje generalmente incluye información básica sobre Docker y confirma que el proceso de ejecución de contenedores funciona correctamente en tu entorno.

![[Pasted image 20240715102021.png]]