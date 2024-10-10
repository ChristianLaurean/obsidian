---
Fecha_creación: 2024-09-15
Categorias: "[[Areas/FastAPI|FastAPI]]"
tags:
  - Concepto
URL:
---



# Path 

Podemos agregarle parametros para poder filtrar nuestros datos

```python

from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

  

# Entidad Users

class Users(BaseModel):
	id : int
	name: str
	sunname: str
	age: int

  

users_db_fake = [Users(id=1, name="John", sunname="Tovar",age = 28),
				Users(id=2, name="Jonathan", sunname="Gomez",age = 24),
				Users(id=3, name="Chicharito", sunname="hernandez",age = 36)]

  
  
@app.get("/user/{id}")
async def user(id : int):
	user = filter(lambda x : x.id == id, users_db_fake)

try:
	return list(user)[0]
except IndexError:
	return {"message": "User not found"}
```
Se usa para parametros fijos 
## Buscar con querys

```python
http://127.0.0.1:8000/userqury/?id=1

@app.get("/userqury/")
async def user(id : int):
	user = filter(lambda x : x.id == id, users_db_fake)
	try:
		return list(user)[0]
	except IndexError:
		return {"message": "User not found"}

```

Se usa para parametros que no pueder ser necesarios para hacer una petición.