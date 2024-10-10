---
Fecha_creación: 2024-06-14
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - DDL
URL:
---

La `CREATE TABLE`declaración en SQL es un comando del lenguaje de definición de datos ([[Data Definition Language (DDL)]]) que se utiliza para crear una nueva tabla en la base de datos.

## [Sintaxis] de CREATE TABLE de [[SQL]]

La sintaxis de SQL `CREATE TABLE` es la siguiente:

```SQL
CREATE TABLE table_name (    
	column1 datatype,
	column2 datatype,
	column3 datatype,   
	....);
```

- `table_name`es el nombre de la tabla que desea crear.
- `column1, column2,...`son las columnas de la tabla.
- `datatype`es el tipo de datos de la columna, como varchar, int, fecha, etc.

## Ejemplo de CREATE TABLE de SQL

He aquí un ejemplo de la `CREATE TABLE`declaración:

```SQL
CREATE TABLE Employees (
	ID int,
	Name varchar(255),
	Salary int,
	Department varchar(255),
    Position varchar(255)
    );
```

Este comando SQL crea una nueva tabla `Employees`con cinco columnas, denominadas 'ID', 'Nombre', 'Salario', 'Departamento' y 'Puesto'. Los tipos de datos son int para 'ID' y 'Salario', y varchar(255) para los demás.
