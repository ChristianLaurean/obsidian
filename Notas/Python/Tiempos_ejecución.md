---
Fecha_creación: 2024-08-09
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
```python
time=%timeit -o -r2 -n10 # comando o codigo, nos da un promedio de estadisticas de tiempo
# Ejecuta el codigo varias veces para estimar el tiempo de ejecución
# -o para guardar el tiempo en una variable
#-r num_ejecuciones
# -n Numero de bucles
time.timings # Ver todas las ejecuciones
time.best # Mejor ejecucuón
time.worst # peor ejecución
#Ver la diferencia
diff = (var.average - var_2.average) * (10**9)
```

# perfilado 

Es una tecnica para descubrir cuánto tiempo y con que frecuencia se ejecutan varias partes del programa

Debemos de intarlar `pip install line_profiler`

<font color="#ffff00">Cargamos el paquete a python</font>

```python
%load_ext line_profiler

# lo usamos asi para cada funcion 
# -f para perfilar una función
%lprun -f convert_units convert_units(heroes,hts,wts)
```


Nos retorna una tabla con resúmenes estadísticos : 
![[Pasted image 20240809104801.png]]

Timer unit: Temporizador en microsegundos usando una notación científica
Hist: Numero de veces que se ejecuto la linea
Time: Cantidad total de tiempo que tardo en ejecutarse cada linea
Per Hit: Cantidad promedio que se tarda en ejecutar cada linea
% Time: Muestra el porcentaje de tiempo dedicado a una [[task]]

# # Perfilado de código para uso de [[Memoria Ram]]

Es parecido que `line_profiler` 

`pip install memory_profiler`

```python
%load_ext memory_profiler

%mprun -f convert_units convert_units(heroes,hts,wts)
```

- Desventaja solo se puede usar en funciones definidas en archivos físicos no en la cesión IPython.
![[Pasted image 20240809113217.png]]

- Mem usage: es la memoria utilizada después de que se haya ejecutado esa linea
- Increment: la diferencia de memoria de la linea actual con respecto a la anterior.
- MiB: Mebibytes