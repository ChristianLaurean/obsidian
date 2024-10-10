---
Fecha_creación: 2024-06-09
Categorias: "[[Linux]]"
tags:
  - Fundamentos
URL:
---

`cat` imprime el contenido en la [[Shell]] 

```bash
cat agarwal.txt
```

# ¿Cómo puedo ver el contenido de un archivo por partes?

`less` Te muestra una pagina a la vez y con la barra espaciadora pasar por pagina con la q no salimos.

```bash
less seasonal/spring.csv seasonal/summer.csv
# con :n pasamos de archivo
#:p para regresar al anterior archivo
# :q salir
```

# ¿Cómo puedo ver el inicio de un archivo?

`head` Podemos ver que datos tenemos al inicio

```bash
head seasonal/summer.csv
```

```
head -n 3 seasonal/summer.csv
```

# ¿Cómo puedo seleccionar columnas de un fichero?

`cut` es un separador
`-f` Los campos
`-d` delimitador
```bash
cut -f 2-5,8 -d , values.csv
Seleciona las columnas 2 a la 5 y la columna 8
```

```bash
cut -d ,-f1 , values.csv
```


# ¿Cómo puedo seleccionar líneas que contengan valores específicos?

- `head` y `tail` seleccionar filas
- `cut` selecciona columnas
- `grep` selecciona las líneas según lo que contengan

```bash
grep -v -n molar seasonal/spring.csv
```

- `-c`: imprime un recuento de las líneas coincidentes en lugar de las propias líneas
- `-h`: _no_ imprimir los nombres de los archivos al buscar varios archivos
- `-i`: ignora mayúsculas y minúsculas (por ejemplo, trata "Regresión" y "regresión" como coincidencias)
- `-l`: imprime los nombres de los archivos que contienen coincidencias, no las coincidencias
- `-n`: imprime los números de línea de las líneas coincidentes
- `-v`: invierte la coincidencia, es decir, muestra sólo las líneas que _no_ coinciden