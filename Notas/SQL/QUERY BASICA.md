---
Fecha_creación: 
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Fundamentos
  - SQL
URL: 
Tipo_recurso: Blog
---
# Seleccionar columnas


![[Export 1.png]]
- ¿Que estamos haciendo? Definir las columnas (y los nombres de las columnas) en la tabla de resultados final.
- ¿Cuándo lo necesito? ¡En cada consulta! Es lo único que se requiere de cada consulta que escriba.

## ¿CÓMO FUNCIONA?

- La cláusula `SELECT` especifica las columnas que queremos que se devuelvan y los nombres de las columnas.

- La cláusula `FROM` especifica de qué tablas de nuestra base de datos provienen las columnas.
```SQL
SELECT
	<col_name> {AS <alias>},
	<col_name> {AS <alias>}
FROM <table_name>
```

## Seleccionar valores únicos

Cuando desee seleccionar solo los valores únicos en una columna, puede usar la palabra clave: `DISTINCT`:
![[select_distinct.png]]
## NO OLVIDES

1. SELECT * es caro (y lento): intenta no usarlo
2. No olvide incluir su esquema al hacer referencia a una tabla de base de datos (`<nombre_esquema>.<nombre_tabla>`)
3. Puede cambiar el nombre de las columnas (Alias) utilizando la palabra clave `AS` (no siempre es necesario, pero es una buena práctica)
4. Consulte las [[Buenas Practicas escribiendo querys|Mejores Practicas]] de nomenclatura para asegurarse de utilizar nombres de columnas sensatos al cambiarles el nombre.