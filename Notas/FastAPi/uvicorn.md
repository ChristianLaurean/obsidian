---
Fecha_creación: 2024-09-14
Categorias: "[[Areas/FastAPI|FastAPI]]"
tags:
  - Concepto
URL:
---
Es un servidor que nos proporcionar [[Notas/FastAPi/FastAPI|FastAPI]].

- Es muy rápido


## isntalar Uvicorn

```bash
pip install "uvicorn[standard]"
```

### Arrancar uvicorn

```python
#Main: es el nombre del fichero que queremos arrancar
#app: nombre de la inicialización de FastAPI 
# --reload: Es un argumento que lo que hara es recargar el servidor cada vez que cambieamos algo del fichero
uvircorn main:app --reload
```
