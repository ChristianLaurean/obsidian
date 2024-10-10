---
Fecha_creación: 2024-07-04
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Manipulación_datos
URL:
---
# Subconsultas correlacionadas

Las subconsultas correlacionadas son subconsultas que hacen <span style="background:#d3f8b6">referencia a una o más columnas de la consulta principal</span>. Las subconsultas correlacionadas dependen de la información en la consulta principal para ejecutarse y, por lo tanto, no pueden ejecutarse por sí solas.

Las subconsultas correlacionadas <span style="background:#ff4d4f">se evalúan en SQL una vez por fila de datos recuperados</span>, un proceso que toma mucho más poder de computación y tiempo que una simple subconsulta.

## Sintaxis 

```sql
SELECT column_name [, column_name...]
FROM   table1 [, table2...]
WHERE  column_name OPERATOR
  (SELECT column_name [, column_name...]
   FROM table_name
   WHERE condition [table1.column_name = table2.column_name...]);
```

## Ejemplo

Por ejemplo, si desea obtener los empleados cuyos salarios son superiores a los salarios promedio de su departamento, puede consultarlos con una subconsulta correlacionada de la siguiente manera:

```sql
SELECT e1.employee_name, e1.salary
FROM employee e1
WHERE salary > 
   (SELECT AVG(salary)
   FROM employee e2
   WHERE e1.department = e2.department);
```

En el ejemplo anterior, la subconsulta correlacionada (la consulta interna) calcula el salario promedio de cada departamento. Luego, la consulta externa compara el salario de cada empleado con el salario promedio de su respectivo departamento. Devuelve los empleados cuyos salarios son superiores al promedio de su departamento. La subconsulta correlacionada se ejecuta una vez por cada fila seleccionada por la consulta externa.

Tenga en cuenta también que `e1`y `e2`son los alias de la `employee`tabla, de modo que podemos utilizarlos tanto en la consulta interna como en la consulta externa. Aquí, `e2.department`en la consulta interna proviene de la consulta externa `e1.department`.

Por lo tanto, una subconsulta correlacionada es una subconsulta que depende de la consulta SQL externa para obtener sus valores. Esto significa que la subconsulta se ejecuta una vez por cada fila de la consulta externa, lo que suele generar un procesamiento considerable y, por lo tanto, resultados más lentos.


