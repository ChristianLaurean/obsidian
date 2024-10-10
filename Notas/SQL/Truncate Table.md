---
Fecha_creación: 2024-07-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - DDL
URL:
---
La `TRUNCATE TABLE`instrucción es una operación del lenguaje de definición de datos (DDL) que se utiliza para marcar las extensiones de una tabla para su desasignación (vacía para su reutilización). El resultado de esta operación elimina rápidamente todos los datos de una tabla, generalmente omitiendo una serie de mecanismos de aplicación de integridad destinados a proteger los datos (como los activadores).

Elimina de forma eficaz todos los registros de una tabla, pero no la tabla en sí. A diferencia de la [[DELETE]] instrucción, `TRUNCATE TABLE` no genera instrucciones de eliminación de filas individuales, por lo que no se aplica la sobrecarga habitual de registro o bloqueo.

## Sintaxis

En SQL, la `TRUNCATE TABLE`declaración es bastante simple:

```sql
TRUNCATE TABLE table_name;
```

En este comando, "table_name" se refiere al nombre de la tabla que desea borrar.

## Ejemplo

Si tiene una tabla llamada `Orders`y desea eliminar todos sus registros, deberá utilizar:

```sql
TRUNCATE TABLE Orders;
```

Después de ejecutar esta declaración, la `Orders`tabla aún existiría, pero estaría vacía.

Recuerde, aunque `TRUNCATE TABLE`es más rápido y utiliza menos recursos del sistema y del registro de transacciones que `DELETE`, no invoca activadores y no se puede revertir, así que utilícelo con precaución.

## Limitaciones
Truncar conserva la estructura de la tabla para uso futuro. Pero no se puede truncar una tabla que:

- Se hace referencia a una restricción FOREIGN KEY. (Puede truncar una tabla que tenga una clave externa que haga referencia a sí misma).
- Participa en una vista indexada.
- Se publica mediante replicación transaccional o replicación de combinación.

Si intenta truncar una tabla con una restricción de clave externa, SQL Server le impedirá hacerlo y tendrá que utilizar la `DELETE`declaración en su lugar.

En el caso de las tablas particionadas, `TRUNCATE TABLE`elimina todas las filas de todas las particiones. La operación no está permitida si la tabla contiene columnas LOB - `varchar(max), nvarchar(max), varbinary(max), text, ntext, image, xml`, o si la tabla contiene columnas de flujo de archivos o columnas de tipo de datos de geoespacial, geografía, geometría y id de jerarquía, o cualquier columna de tipos de datos definidos por el usuario de CLR.


