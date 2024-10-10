---
Fecha_creación: 2024-09-16
Categorias: "[[Areas/FastAPI|FastAPI]]"
tags:
  - Concepto
URL:
---
los **routers** son componentes que permiten organizar las rutas (endpoints) de una aplicación en módulos separados, facilitando la gestión y el mantenimiento del código.


#### Creando un router

1. Creamos una carpeta que se llame router 
```python
# Archivo
from fastapi import APIRouter

router = APIRouter(prefix="/products", 
				   tags=["products"],
				   responses={404:{"message": "Error"}})

# Archivo main 
from routers import products
# Routers
app.include_router(products.router)
```
