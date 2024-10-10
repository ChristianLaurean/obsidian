---
Fecha_creación: 2024-07-14
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
## PIP

El PIP es un administrador de paquetes para Python que se utiliza para instalar, desinstalar y administrar paquetes de software de Python.

## ¿Qué es el PIP?[​](https://docs.z2h.online/docs/Roadmaps/Python/Administrador%20de%20paquetes%20de%20Python#qu%C3%A9-es-el-pip "Direct link to ¿Qué es el PIP?")

El PIP es un programa de línea de comandos que se puede utilizar para instalar paquetes de Python a través de la Python Package Index: [https://pypi.org/](https://pypi.org/). El PIP es una herramienta esencial para cualquier desarrollador de Python, ya que permite instalar rápidamente y fácilmente paquetes de software de Python.

## Instalación de PIP

El PIP viene preinstalado con la mayoría de las distribuciones de Python. Si el PIP no está instalado en su sistema, puede instalarlo utilizando el siguiente comando:

```
python -m pip install --user pip
```

Este comando instalará el PIP en su directorio de usuario.

## Instalación de paquetes usando pip

Para instalar un paquete usando el PIP, utilice el siguiente comando:

```
pip install paquete
```

Por ejemplo, para instalar el paquete `numpy`, utilice el siguiente comando:

```
pip install numpy
```

Este comando instalará el paquete `numpy` en su sistema.

## Desinstalar paquetes

Para desinstalar un paquete usando el PIP, utilice el siguiente comando:

```
pip uninstall paquete
```

Por ejemplo, para desinstalar el paquete `numpy`, utilice el siguiente comando:

```
pip uninstall numpy
```

Este comando desinstalará el paquete `numpy` de su sistema.

## Lista de paquetes

Para ver una lista de todos los paquetes instalados en su sistema, utilice el siguiente comando:

```
pip list
```

Este comando imprimirá una lista de todos los paquetes instalados en su sistema.

## Mostrar paquete

Para obtener más información sobre un paquete específico, utilice el siguiente comando:

```
pip show paquete
```

Por ejemplo, para obtener más información sobre el paquete `numpy`, utilice el siguiente comando:

```
pip show numpy
```

Este comando imprimirá información sobre el paquete `numpy`, incluida su versión, dependencias y licencia.

## Congelación de PIP

Para congelar la versión de un paquete, utilice el siguiente comando:

```
pip freeze > archivo.txt
```

Este comando creará un archivo llamado `archivo.txt` que contiene una lista de todos los paquetes instalados en su sistema, junto con sus versiones.

## Leyendo desde URL

Para instalar un paquete desde una URL, utilice el siguiente comando:

```shell
pip install -U https://url/del/paquete.tar.gz
```

Por ejemplo, para instalar el paquete `numpy` desde la URL [https://pypi.org/project/numpy/](https://pypi.org/project/numpy/), utilice el siguiente comando:

```python
pip install -U https://pypi.org/project/numpy/
```

Este comando instalará el paquete `numpy` en su sistema.

## Creando un paquete

Para crear un paquete de Python, puede utilizar el módulo `setuptools`. El módulo `setuptools` proporciona una serie de funciones que se pueden utilizar para crear paquetes de Python.

Para obtener más información sobre cómo crear un paquete de Python, consulte la documentación de setuptools: 


