---
Fecha_creación: 2024-04-16
Categorias: "[[Areas/SQL|SQL]]"
tags:
  - Fundamentos
  - SQL
URL: 
Tipo_recurso: Blog
---
# Reglas para escribir SQL

1. El caso y el espacio no importan
![[no_formatting.png]]
2. Es común finalizar una declaración SQL con un `;`, pero ya pocas herramientas lo requieren.
![[semicolon.png]]
3. Las declaraciones deben comenzar con una palabra clave.
![[keyword.png]]
# Mejores prácticas para escribir [[SQL]] 

Si bien estas no son reglas, son estándares comúnmente acordados.

#### <span style="background:#fff88f">Caso consistentemente</span>

Si bien a SQL no le importan las mayúsculas y minúsculas, se considera una buena práctica hacerlo de forma coherente. Por ejemplo, puede optar por:
- Utilice siempre mayúsculas para palabras clave y nombres de funciones (esto varía mucho según los usuarios)
- Utilice siempre minúsculas para los nombres de columnas y tablas (esto es una práctica recomendada muy aceptada)
![[Export (5) 1.png]]

 

#### <span style="background:#fff88f">Espacios</span>

Una razón importante por la que SQL es tan legible es que parece una oración o un párrafo. La forma en que se utiliza el espaciado juega un papel importante en la legibilidad de una consulta. En general, es común:

- tenga una nueva línea para cada columna en su declaración `SELECT` para que sea fácil de leer
- tener una nueva línea para cada palabra clave
- Si la cláusula de palabra clave es compleja, utilice una nueva línea y aplique sangría hasta la siguiente palabra clave.
![[spaced_formatting.png]]
#### <span style="background:#fff88f">Nombre con intención</span>

Es muy importante prestar atención a los nombres que le da a las columnas y tablas. No solo hace que las cosas sean legibles, sino que cuando desarrollas un estándar dentro de tu equipo, todos pueden avanzar más rápido porque pueden esperar el nombre de cada columna/tabla.

Convenciones de nomenclatura comunes:

- Utilice mayúsculas y minúsculas (por ejemplo, nombre_columna NO NombreColumna) 

- Los campos ambiciosos deben tener como prefijo el nombre (por ejemplo, account_id, no id).

- Los campos de marca de tiempo deben terminar con _at (por ejemplo, creado_at)

- Los campos de fecha deben terminar con _date (por ejemplo, create_date)

- Las columnas deben ser singulares o plurales, dependiendo de lo que signifique el valor de una sola fila (por ejemplo, transmisiones es mejor que transmisión, porque cada fila es una agregación de transmisiones diarias. Pero día es mejor que días porque cada fila es solo un día).

- Utilice unidades cuando no sea obvio (por ejemplo, ingresos_usd o peso_kg)

- Evite el uso de palabras clave SQL al nombrar columnas y tablas (por ejemplo, evite `date` o `month`)
#### <span style="background:#fff88f">Comenta con todo tu corazón</span>

Puede agregar comentarios a su código (notas que no se ejecutan en la base de datos pero que otros pueden leer) usando `--` o `/*` .

Los comentarios se utilizan para:

- Explicar por qué has hecho algo (para ti mismo en el futuro o para cualquier otra persona que lea tu código)

- Elimine parte del código para que pueda probar diferentes versiones de su consulta
 
![[comments.png]]