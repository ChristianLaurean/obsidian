---
Fecha_creación: 2024-07-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - SQL
URL:
---

La `DELETE`instrucción SQL le ayuda a eliminar registros existentes de una base de datos. Sin embargo, tenga en cuenta que es una operación destructiva y puede borrar datos de su base de datos de forma permanente.

Con la declaración `DELETE` puedes realizar lo siguiente:

1. **Eliminar todas las filas:**
    
> [!danger] La `DELETE`declaración sin `WHERE`cláusula elimina todas las filas de una tabla. Esta operación es irreversible.


Ejemplo:
```sql
DELETE FROM table_name;
```

<span style="background:#b1ffff">Esta declaración SQL elimina todos los registros de `table_name`.</span>
    
2. **Eliminar filas específicas:**
    
    Cuando se combina con la `WHERE` cláusula, la instruccion `DELETE` SQL borra filas específicas que cumplen la condición.
    
    Ejemplo:
    
```sql
    DELETE FROM table_name WHERE condition;
```
    
<span style="background:#b1ffff">Esta instancia de la `DELETE`declaración elimina registros del `table_name`lugar donde `condition`coinciden las condiciones dadas.</span>
    

Es fundamental usarlo `DELETE`con precaución porque tiene el potencial de borrar ciertas filas importantes o vaciar la tabla por completo.

<span style="background:#ff4d4f">_Nota: La eliminación realizada con la instrucción "DELETE" es permanente y no se puede deshacer. Asegúrese siempre de tener una copia de seguridad antes de ejecutar una consulta DELETE, especialmente cuando se trata de una base de datos de producción._</span>

