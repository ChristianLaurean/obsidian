---
Fecha_creación: 2024-09-16
Categorias: "[[Areas/FastAPI|FastAPI]]"
tags:
  - Concepto
URL:
---


Son:  
- imagenes, 
- PDFS

## Creando

1. Crear una carpeta static/images
2. Guardamos los recursos estáticos
```python
from fastapi.staticfiles import StaticFiles
app = FastAPI()
app.mount("/static", StaticFiles(directory="static"), name="static")
```
