---
Fecha_creación: 2024-07-15
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - DCL
URL:
---

En SQL, `GRANT`y `REVOKE`son comandos del lenguaje de control de datos (DCL) que se utilizan para proporcionar y eliminar privilegios de usuario respectivamente.

## GRANT

`GRANT` permite a los administradores de bases de datos otorgar permisos o privilegios a los usuarios sobre un objeto de base de datos. Existen varios tipos de privilegios, como SELECT, INSERT, UPDATE, DELETE, REFERENCES, ALL.

Puedes utilizar la `GRANT`declaración de la siguiente manera:

```sql
GRANT privilege_name
ON object_name
TO {user_name |PUBLIC |role_name}
[WITH GRANT OPTION];
```

Ejemplo:

```sql
GRANT SELECT ON employees TO user1;
```

En este ejemplo, `user1`se concede permiso para leer/realizar operaciones SELECT en la `employees`tabla.

## REVOKE

`REVOKE` se puede utilizar cuando queremos revocar algunos o todos los privilegios que se asignaron anteriormente a un usuario o a un grupo de usuarios. La sintaxis para utilizar el `REVOKE`comando es similar a la del `GRANT`comando.

Aquí está la sintaxis:

```SQL
REVOKE privilege_name
ON object_name
FROM {user_name |PUBLIC |role_name}
```

Ejemplo:

```SQL
REVOKE SELECT ON employees FROM user1;
```

En este ejemplo, `user1`se revoca el permiso para leer/realizar operaciones SELECT en la `employees`tabla.

La gestión de permisos es un aspecto importante de la gestión de bases de datos; comprenderlos, utilizarlos y realizar `GRANT`operaciones `REVOKE`ayudan a mantener la integridad y seguridad de sus datos en SQL.

# Crear un grupo o usuarios 

En PostgreSQL, los "grupos" son conocidos como "roles". Puedes crear un rol que actúe como un grupo de usuarios.

```sql
CREATE ROLE nombre_grupo;
```
### Crear Usuarios y Asignarlos al Grupo

Luego, puedes crear usuarios (también roles) y asignarlos al grupo.

1. **Crear Usuarios:**


```sql
CREATE ROLE nombre_usuario1 WITH LOGIN PASSWORD 'contraseña1'; 
CREATE ROLE nombre_usuario2 WITH LOGIN PASSWORD 'contraseña2';
```

2. **Asignar Usuarios al Grupo:**

```sql
GRANT nombre_grupo TO nombre_usuario1; 
GRANT nombre_grupo TO nombre_usuario2;
```
### Ejemplo Completo

Supongamos que deseas crear un grupo llamado `desarrolladores` y dos usuarios `usuario1` y `usuario2` que pertenezcan a este grupo.

1. **Crear el grupo:**
```sql
CREATE ROLE desarrolladores;
```
2. **Crear los usuarios:**

```sql
CREATE ROLE usuario1 WITH LOGIN PASSWORD 'password1'; 
CREATE ROLE usuario2 WITH LOGIN PASSWORD 'password2';
```


3. **Asignar los usuarios al grupo:**

```sql
GRANT desarrolladores TO usuario1; 
GRANT desarrolladores TO usuario2;`
```
### Verificar la Creación de Roles y Asignaciones

Puedes verificar la creación de roles y sus asignaciones utilizando las siguientes consultas:

1. **Listar Roles:**

`\du`

2. **Verificar Privilegios:**

`\dp`