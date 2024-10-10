---
Fecha_creación: 2024-08-02
Categorias: "[[Python]]"
tags:
  - Arquitectura
URL:
---
# Archivos

```bash
pip install python-dotenv
```

```python
# .env
DB_HOST=localhost
DB_PORT=5432
DB_NAME=database
DB_USER=user
DB_PASSWORD=password
```

```python
from dotenv import load_dotenv

load_dotenv()

host = os.getenv("DB_HOST")
port = os.getenv("DB_PORT")
name = os.getenv("DB_NAME")
user = os.getenv("DB_USER")
password = os.getenv("DB_PASSWORD")
```

```python
si se encuentra en otro directorio
# app.py
from dotenv import load_dotenv

dotenv_path = Path('path/to/.env')
load_dotenv(dotenv_path=dotenv_path)
```

- <font color="#92d050">constants.py:</font> Colocamos todas las constantes de nuestro proyecto
![[Pasted image 20240802125404.png]]
- <font color="#92d050">config.py:</font> Archivo para traernos todas las variables de entorno
![[Pasted image 20240802125514.png]]
- <font color="#92d050">requirements.txt:</font> Es un archivo que tendrá todas nuestras dependencias de nuestro proyecto. puedes ver un poco mas en: [[Entornos virtuales en Python]]
# Carpetas

- <font color="#92d050">Carpeta config</font> podemos agregar todos nuestros archivos .env
- <font color="#92d050">Carpeta src</font>: Tenemos todos nuestros archivos del proyecto

![[Pasted image 20240802125823.png]]
