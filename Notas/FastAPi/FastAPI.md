---
Fecha_creación: 2024-09-14
Categorias: "[[Areas/FastAPI|FastAPI]]"
tags:
  - Framework
URL:
---


Es un Framework moderno y rapido de alto rendimiento para contruir APis con [[Python]]


### Instalación

```bash
pip install "fastapi[all]"
```

### FastAPI 101

```python
from fastapi import FastAPI

app = FastAPI()
# Si alguien hace una petición Get nos devolvera Wordl
@app.get("/") 
async def read_root(): 
	return {"Hello": "World"}
```

#### Crear Post

```python

from fastapi import FastAPI
from pydantic import BaseModel

class Users(BaseModel):
	id : int
	name: str
	sunname: str
	age: int


app = FastAPI()

# Si alguien hace una petición Get nos devolvera Wordl
@app.posts("/user/") 
async def create_user(user: User): 
	return [{"Hello": "World"}].append(user)
```
