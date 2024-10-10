---
Fecha_creación: 2024-06-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - DML
URL:
---

La `UPDATE`sentencia SQL se utiliza para modificar los datos existentes en una base de datos. Esta sentencia es muy útil cuando se necesita cambiar los valores asignados a campos específicos en una fila o un conjunto de filas existentes.

La sintaxis general de la instrucción UPDATE es la siguiente:

```SQL
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

- `table_name`:El nombre de la tabla donde se realizará una actualización.
- `SET`:Esta cláusula especifica el nombre de la columna y el nuevo valor al que debe actualizarse.
- `column1, column2, ...`:Los nombres de las columnas de la tabla.
- `value1, value2, ...`:Los nuevos valores que desea registrar en la base de datos.
- `WHERE`:Esta cláusula especifica las condiciones que identifican qué filas actualizar.

## Ejemplo 
He aquí un ejemplo que puede arrojar algo de luz. Para una `Employees`  imaginaria:

|ID de empleado|Nombre|Posición|Salario|
|---|---|---|---|
|1|Jane|Gerente|50000|
|2|John|Oficinista|30000|
|3|Beto|Ingeniero|40000|

Si quieres aumentar el salario de BoTO en $5000, usarías:

```SQL
UPDATE Employees
SET Salary = 45000
WHERE EmployeeID = 3;
```

Esto cambiaría permanentemente los datos de la `Employees`tabla:

| ID de empleado | Nombre | Posición   | Salario |
| -------------- | ------ | ---------- | ------- |
| 1              | Jane   | Gerente    | 50000   |
| 2              | John   | Oficinista | 30000   |
| 3              | Beto   | Ingeniero  | 5000    |

>[!warning] Cuidado!
Tenga siempre cuidado con la `UPDATE` declaración; si olvida la `WHERE`cláusula, actualizará todas las filas de la tabla.


