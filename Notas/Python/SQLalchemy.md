---
Fecha_creación: 2024-06-17
Categorias: "[[Python]]"
tags:
  - Carga_datos
URL:
---

# 1 ¿Que es?
Es un ORM que nos sirve para interacturar con una base de datos con python.


# 2 Uso de SQLalchemy

Asegúrate de tener un servidor de PostgreSQL instalado y en funcionamiento. También necesitarás instalar el paquete `psycopg2` para conectar con PostgreSQL.

### 2.1 Instalación de psycopg2

```bash
pip install psycopg2-binary
```
### 2.2 Conexión a la Base de Datos PostgreSQL

```python
import pandas as pd 
from sqlalchemy import create_engine  
# Crear motor de base de datos 
db_engine = create_engine('postgresql+psycopg2://username:password@localhost/mydatabase')
```
Crea un objeto del motor que administra las conexiones de la [[Base de datos]]
## Módulo 3: Operaciones CRUD con [[Pandas]]

### 3.1 Creación de una Tabla desde un DataFrame

```python
# Crear un DataFrame 
df = pd.DataFrame(data)  # Escribir DataFrame a la base de datos 
df.to_sql('users', engine, if_exists='replace', index=False)`
```
### 3.2 Lectura de Datos desde la Base de Datos

```python
# Leer datos desde la base de datos 
df = pd.read_sql('SELECT * FROM users', engine) 
print(df)
```
### 3.3 Actualización de Datos

Para actualizar datos, primero leemos los datos en un DataFrame, realizamos las modificaciones necesarias y luego escribimos de nuevo los datos en la base de datos.

```python
# Leer datos desde la base de datos 
df = pd.read_sql('SELECT * FROM users', engine)  
# Actualizar datos en el DataFrame 
df.loc[df['name'] == 'Alice', 'age'] = 31  
# Escribir DataFrame actualizado a la base de datos 
df.to_sql('users', engine, if_exists='replace', index=False)`
```

### 3.4 Eliminación de Datos

Para eliminar datos, seguimos un proceso similar al de la actualización. Leemos los datos, eliminamos las filas necesarias y luego escribimos de nuevo en la base de datos.

```python

# Leer datos desde la base de datos 
df = pd.read_sql('SELECT * FROM users', engine)  
# Eliminar datos del DataFrame 
df = df[df['name'] != 'Bob'] 
# Escribir DataFrame actualizado a la base de datos 
df.to_sql('users', engine, if_exists='replace', index=False)`
```

## Módulo 4: Integración con Procesos de Ingeniería de Datos

### 4.1 Proceso ETL (Extract, Transform, Load)

Pandas es muy útil para llevar a cabo procesos ETL. A continuación, se muestra un ejemplo básico de un proceso ETL usando Pandas y PostgreSQL.

```python
def etl_process():     
	# Extracción     
	df = pd.read_csv('data.csv')          
	# Transformación     
	df['age'] = df['age'] + 1          
	# Carga     
	df.to_sql('users', engine, if_exists='append', index=False)  
etl_process()`
```
### 4.2 Manejo de Errores

Es importante manejar los errores adecuadamente durante las operaciones de ETL.

```python
try:     
	df = pd.read_csv('data.csv')
	df['age'] = df['age'] + 1     
	df.to_sql('users', engine, if_exists='append', index=False) 
except Exception as e:     
	print(f"Error: {e}")
```
