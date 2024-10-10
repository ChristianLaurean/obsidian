---
Fecha_creación: 2024-06-09
Categorias: "[[Linux]]"
tags:
  - Fundamentos
URL:
---
La Shell de linux es una aplicación del [[¿Qué es un Sistema Operativo? |Sistema Operativo]] que interpreta comandos.

###### Tipos de shell
- [[Bash]]
- [[Zsh]]

## ¿Como se ejecuta un comando?

1. Primero el Usuario piensa en que comando va a necesitar
2. Después introduce el comando en la [[Shell]] 
3. La shell lo interpreta, si el comando es valido, la shell lo traduce en una serie de llamadas al sistema operativo pueda entender.
4. El sistema operativo y el Kernel reciben estas llamadas de la shell
5. EL kernel traduce las llamadas al sistema de instrucciones del [[Hardware]]
6. EL [[Hardware]] Ejecuta las instrucciones 
7. Una vez se ejecutara completamente se duvuelven los resultados primero al kernel, despues al sistema operativo y al ultimo a la shell

En resumen, la secuencia es:

- Usuario → Shell → Sistema Operativo → Kernel → Hardware → Kernel → Sistema Operativo → Shell → Usuario.

![[Pasted image 20240609091129.png]]


