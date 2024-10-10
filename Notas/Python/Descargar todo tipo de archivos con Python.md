---
Fecha_creación: 2024-06-20
Categorias: "[[Extracción]]"
tags:
  - Programación
URL:
---

## descargar archivos


### `iter_content()`

- **Uso**: Se utiliza comúnmente con respuestas que pueden contener datos binarios, como archivos.
    
- **Función**: Descarga los datos en bloques de tamaño específico y los va retornando en cada iteración.
    
- **Ventajas**: Es útil para descargar archivos grandes porque permite controlar el tamaño del bloque de descarga.

```python
# No se cierre la conexión del servidor hazta que se descarge y se descarga en chunks.

response = requests.get(url,stream=True)
# WB:escritura binaria
with open('img.jpg', 'wb') AS file:
	for chunk in response.iter_content(1024):#kilobites
		file.write(chunk)
```

### `iter_lines()`

- **Uso**: Se utiliza para leer respuestas de texto línea por línea.
    
- **Función**: Itera sobre las líneas de texto en una respuesta de solicitud.
    
- **Ventajas**: Útil para respuestas de texto grande donde deseas procesar línea por línea, como en archivos de texto o datos CSV.


```python
import requests

r = requests.get(url,stram=True)
r.raise_for_status()

for line in r.iter_lines()
	if line:
		yield json.loads(line)
```

## Forma sencilla 
```python
import requests

r = requests.get(url,stram=True)
r.raise_for_status()

with open("path", "wb") as file:
	file.write(request.contect)

```