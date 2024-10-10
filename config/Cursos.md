
```button
name Nuevo registro
type command
action QuickAdd: Areas
```

```dataview
TABLE without id 
  file.link AS "Title",
  Autor AS "Autor",
  Categoria AS "Categoria",
  Tipo_curso

FROM "Areas"
```
