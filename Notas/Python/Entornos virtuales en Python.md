---
Fecha_creación: 2024-07-14
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
## Introducción

Los entornos virtuales en Python son una forma de aislar las dependencias de los proyectos de Python. Esto puede ser útil por varias razones, como:

- Permitir que diferentes proyectos utilicen diferentes versiones de las mismas bibliotecas.
- Evitar que las dependencias de un proyecto interfieran con las dependencias de otros proyectos.
- Facilitar la instalación y la gestión de las dependencias de los proyectos.

## Cómo crear un entorno virtual

Para crear un entorno virtual en Python, podemos utilizar el módulo `venv`. El siguiente código crea un entorno virtual llamado `mi_entorno_virtual` en el directorio actual:


```bash
python3 -m venv mi_entorno_virtual
```

Este comando creará un directorio llamado `mi_entorno_virtual`. Dentro de este directorio, se crearán dos archivos importantes:

- `bin/activate`. Este archivo es un script que activa el entorno virtual.
- `pyvenv.cfg`. Este archivo contiene la configuración del entorno virtual.

## Cómo activar un entorno virtual
Para activar un entorno virtual, debemos ejecutar el script `activate`. El siguiente comando activará el entorno virtual `mi_entorno_virtual`:

```bash
source mi_entorno_virtual/bin/activate
```

Una vez que el entorno virtual esté activado, veremos que el nombre del entorno virtual se muestra en la línea de comandos.

## Cómo instalar dependencias en un entorno virtual

Para instalar dependencias en un entorno virtual, podemos utilizar el comando `pip`. El siguiente comando instalará la biblioteca `numpy` en el entorno virtual `mi_entorno_virtual`:

```bash
pip install numpy
```

## Cómo desactivar un entorno virtual[​](https://docs.z2h.online/docs/Roadmaps/Python/Entorno%20virtual#c%C3%B3mo-desactivar-un-entorno-virtual "Direct link to Cómo desactivar un entorno virtual")

Para desactivar un entorno virtual, debemos ejecutar el comando `deactivate`. El siguiente comando desactivará el entorno virtual `mi_entorno_virtual`:

```bash
deactivate
```

## Ejemplos[​](https://docs.z2h.online/docs/Roadmaps/Python/Entorno%20virtual#ejemplos "Direct link to Ejemplos")

**Ejemplo 1**

El siguiente ejemplo crea un entorno virtual llamado `mi_entorno_virtual`, instala la biblioteca `numpy` en el entorno virtual y luego muestra la versión de `numpy` instalada:

Python

```python
# Creamos el entorno virtual
python3 -m venv mi_entorno_virtual
# Activamos el entorno virtual
source mi_entorno_virtual/bin/activate
# Instalamos numpy
pip install numpy
# Mostramos la versión de numpy instalada
import numpy
print(numpy.__version__)#
Desactivamos el entorno virtual
deactivate
```

Este código imprimirá la siguiente salida:

```
1.22.3
```



# instalar pgcli

```bash
sudo apt update
sudo apt-get install libpq-dev

pip install pgcli
```

