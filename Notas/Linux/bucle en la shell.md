---
Fecha_creación: 2024-06-09
Categorias: "[[Linux]]"
tags:
  - comandos_linux
URL:
---
```bash
for filetype in gif jpg png; do echo $filetype; done
```


1. La estructura es `for`…variable… `in`…lista… `; do`…cuerpo… `; done`
2. La lista de cosas que debe procesar el bucle (en nuestro caso, las palabras `gif`, `jpg`, y `png`).
3. La variable que lleva la cuenta de lo que el bucle está procesando en ese momento (en nuestro caso, `filetype`).
4. El cuerpo del bucle que realiza el proceso (en nuestro caso, `echo $filetype`).

### ver todo lo que esta dentro del directorio

```bash
for filetype in sirectory/*; do echo $filetype; done
```

# ¿Cómo puedo ejecutar muchos comandos en un solo bucle?

```bash
for file in seasonal/*.csv; do head -n 2 $file | tail -n 1; done
```
