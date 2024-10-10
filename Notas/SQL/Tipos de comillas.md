---
Fecha_creación: 2024-06-18
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Fundamentos
URL:
---
1. **Comillas simples (`'`)**: Se utilizan para delimitar valores literales de tipo texto (strings). Por ejemplo:
    
    ```sql
    SELECT 'Hola, mundo!';
```
2. **Comillas dobles (`"`)**: Se utilizan para delimitar identificadores (como nombres de tablas o columnas) que son sensibles a mayúsculas y minúsculas o que contienen caracteres especiales. Por ejemplo:
    
    ```sql
    CREATE TABLE "MiTabla" (
	    "ID" serial PRIMARY KEY,
	    "Nombre" varchar(100) 
	);
	```

