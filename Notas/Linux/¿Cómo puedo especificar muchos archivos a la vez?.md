---
Fecha_creación: 2024-06-09
Categorias: "[[Linux]]"
tags:
  - Fundamentos
URL:
---
La mayoría de los comandos del shell funcionarán en varios archivos si les das varios nombres de archivo. Por ejemplo, puedes obtener la primera columna de todos los archivos de datos estacionales a la vez de la siguiente manera:


```bash
cut -d , -f 1 seasonal/winter.csv seasonal/spring.csv seasonal/summer.csv seasonal/autumn.csv
```

Pero escribir los nombres de muchos archivos una y otra vez es una mala idea: pierde el tiempo, y tarde o temprano omitirás un archivo o repetirás el nombre de un archivo. 
Para mejorar tu vida, el intérprete de [[Shell]] te permite utilizar **cartas comodín** para especificar una lista de archivos con una sola expresión. El comodín más común es `*`, que significa <font color="#2DC26B">"coincide con cero o más caracteres".</font> Utilízalo, podemos acortar el comando `cut` anterior a esto:

```
cut -d , -f 1 seasonal/*
```

o:

```
cut -d , -f 1 seasonal/*.csv
```

# Comodines

- `?` coincide con un único carácter, por lo que `201?.txt` coincidirá con `2017.txt` o `2018.txt`, pero no con `2017-01.txt`.
- `[...]` coincide con cualquiera de los caracteres dentro de los corchetes, por lo que `201[78].txt` coincide con `2017.txt` o `2018.txt`, pero no con `2016.txt`.
- `{...}` coincide con cualquiera de los patrones separados por comas que hay dentro de las llaves, por lo que `{*.txt, *.csv}` coincide con cualquier archivo cuyo nombre termine en `.txt` o `.csv`, pero no con archivos cuyo nombre termine en `.pdf`.