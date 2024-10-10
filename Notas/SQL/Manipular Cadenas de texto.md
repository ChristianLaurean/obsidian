---
Fecha_creación: 2024-07-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - avanzado
URL:
---



# REEMPLAZAR

Puede utilizar la `REPLACE()`función en SQL para sustituir todas las apariciones de una cadena especificada.

**Sinopsis**

`REPLACE(input_string, string_to_replace, replacement_string)`

**Parámetros**

- `input_string`:Esta es la cadena original en la que desea reemplazar algunos caracteres.
- `string_to_replace`:Esta es la cadena que se buscará en la cadena original.
- `replacement_string`:Esta es la cadena que reemplazará `string_to_replace`en la cadena original.

La `REPLACE()`función es útil cuando se trata de manipular y modificar datos de diversas maneras, particularmente cuando se utiliza en combinación con otras funciones de manipulación de datos SQL.

**Ejemplos**

Supongamos que tenemos la siguiente tabla `Employees`:

|ID emp|Nombre del empleado|
|---|---|
|1|Juan Pérez|
|2|fulano de tal|
|3|Jim Smith, el cerdito|
|4|Jennifer Doe Smith|

Aquí te explicamos cómo puedes utilizar la `REPLACE()`función:

```sql
SELECT EmpId, EmpName,
REPLACE(EmpName, 'Doe', 'Roe') as ModifiedName
FROM Employees;
```

Después de ejecutar el SQL anterior, recibiremos:

|ID emp|Nombre del empleado|Nombre modificado|
|---|---|---|
|1|Juan Pérez|Juan Roe|
|2|fulano de tal|Jane Roe|
|3|Jim Smith, el cerdito|Jim Smith Roe|
|4|Jennifer Doe Smith|Jennifer Roe Smith|

Puedes ver que todas las apariciones de 'Doe' se reemplazan con 'Roe'.

