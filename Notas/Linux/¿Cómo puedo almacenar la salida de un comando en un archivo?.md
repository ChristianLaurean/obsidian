---
Fecha_creación: 2024-06-09
Categorias: "[[Linux]]"
tags:
  - Fundamentos
URL:
---
# redirección 

Nos sirve para guardar la salida de cualquier comando que quiera.

El signo mayor que `>` indica al intérprete de comandos que redirija la salida de `head` a un archivo
```bash
head -n 5 seasonal/summer.csv > top.csv
```


> [!danger] Utilizar la redirección para combinar comandos tiene dos inconvenientes:
> 1. Deja un montón de archivos intermedios por ahí (como `top.csv`).
>2. Los comandos para producir tu resultado final están dispersos en varias líneas de la historia.


```bash
head -n 5 seasonal/summer.csv | tail -n 3
# | utiliza la salida del comando de la izq como entrada para el comando de la derecha
```