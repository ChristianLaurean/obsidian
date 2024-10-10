---
Fecha_creación: 2024-09-15
Categorias: "[[Areas/FastAPI|FastAPI]]"
tags:
  - Concepto
URL:
---



```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

  
# Entidad Users

class Users(BaseModel):
	name: str
	sunname: str
	age: int

  

users_db_fake = [Users(name="John", sunname="Tovar",age = 28),
				Users(name="Jonathan", sunname="Gomez",age = 24),
				Users(name="Chicharito", sunname="hernandez",age = 36)]

  


  
@app.get("/users")
async def users():
	return users_db_fake
```
