---
Fecha_creación: 2024-07-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - DML
URL:
---
_DML_ es una subcategoría de `SQL`lo que significa _lenguaje de manipulación de datos_ . El propósito de DML es insertar, recuperar, actualizar y eliminar datos de la base de datos. Con esto, podemos realizar operaciones sobre registros existentes.

DML contiene cuatro comandos que son:

1. **[[INSERT]]** : este comando se utiliza para insertar nuevas filas (registros) en una tabla.

Ejemplo:

```sql
INSERT INTO table_name ( column1, column2, column3, ... )  
VALUES ( value1, value2, value3, ... )  
```

2. **[[SELECT]]** : este comando se utiliza para seleccionar datos de una base de datos. Los datos devueltos se almacenan en una tabla de resultados, denominada conjunto de resultados.

Ejemplo:

```SQL
SELECT column1, column2, ... 
FROM table_name
```

3. **[[UPDATE]]** : este comando se utiliza para modificar las filas existentes en una tabla.

Ejemplo:

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

4. **[[DELETE]]** : este comando se utiliza para eliminar filas (registros) existentes de una tabla.

Ejemplo:

```sql
DELETE FROM table_name WHERE condition;
```


