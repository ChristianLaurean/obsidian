---
Fecha_creación: 2024-05-31
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---

```Python
import zipfile


def extract_zip(path_name, path_destination):
    with zipfile.ZipFile(path_name, 'r') as zip_file:
        zip_file.extractall(path_destination)# Se crea una carpeta y se descomprime los archivos ahi no hay necesidad de ponerle el tipo de archivo.
        zip_file.extract(ruta)# solos se descomprime sin carpetas
```

# archivo gz

```python
import gzip
import shutil

# Nombre del archivo comprimido y descomprimido
compressed_file = 'taxi_zone_lookup.csv.gz'
decompressed_file = 'taxi_zone_lookup.csv'

# Descomprimir el archivo
with gzip.open(compressed_file, 'rb') as f_in:
    with open(decompressed_file, 'wb') as f_out:
        shutil.copyfileobj(f_in, f_out)
```
