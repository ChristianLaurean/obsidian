---
Fecha_creación: 2024-06-17
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---
`argparse` es un módulo de la biblioteca estándar de Python que se utiliza para crear interfaces de línea de comandos. Permite definir qué argumentos espera un programa, cómo deben ser procesados, y genera automáticamente mensajes de ayuda y errores cuando los usuarios proporcionan argumentos incorrectos.

### Ventajas de usar `argparse`

1. **Facilita la creación de scripts reutilizables**: Al permitir a los usuarios proporcionar diferentes argumentos, puedes hacer tus scripts más flexibles y configurables.
2. **Automatización de tareas repetitivas**: Scripts que utilizan `argparse` pueden ser utilizados en tareas automatizadas sin intervención humana, simplemente pasando los argumentos necesarios.
3. **Generación automática de ayuda y documentación**: `argparse` genera automáticamente mensajes de ayuda basados en los argumentos definidos, lo que facilita a los usuarios entender cómo usar tu script.
4. **Manejo de errores**: `argparse` maneja automáticamente los errores cuando los argumentos no se proporcionan correctamente o son inválidos.

### Ejemplo de uso de `argparse`

```python
import argparse

def main():
    parser = argparse.ArgumentParser(description='Un ejemplo de script con argparse.')

    # Definición de argumentos
    parser.add_argument('--name', type=str, required=True, help='Nombre del usuario')
    parser.add_argument('--age', type=int, help='Edad del usuario')
    parser.add_argument('--verbose', action='store_true', help='Imprimir información detallada')

    # Parsear argumentos
    args = parser.parse_args()

    # Uso de los argumentos
    if args.verbose:
        print(f"Argumentos recibidos: {args}")

    print(f"Hola, {args.name}!")
    if args.age:
        print(f"Tienes {args.age} años.")

if __name__ == "__main__":
    main()
```

### Desglose del ejemplo

1. **Creación del objeto ArgumentParser**:
    
    python
    
    Copiar código
    
    `parser = argparse.ArgumentParser(description='Un ejemplo de script con argparse.')`
    
    Aquí creamos un objeto `ArgumentParser` con una descripción que se mostrará cuando el usuario solicite ayuda.
    
2. **Definición de argumentos**:
    
    python
    
    Copiar código
    
    `parser.add_argument('--name', type=str, required=True, help='Nombre del usuario') parser.add_argument('--age', type=int, help='Edad del usuario') parser.add_argument('--verbose', action='store_true', help='Imprimir información detallada')`
    
    Definimos tres argumentos:
    
    - `--name`: un argumento de cadena obligatorio.
    - `--age`: un argumento entero opcional.
    - `--verbose`: un argumento booleano opcional que se activa si está presente.
3. **Parsear los argumentos**:
    
    python
    
    Copiar código
    
    `args = parser.parse_args()`
    
    Esto analiza los argumentos proporcionados en la línea de comandos y los almacena en el objeto `args`.
    
4. **Uso de los argumentos**:
    
    python
    
    Copiar código
    
    `if args.verbose:     print(f"Argumentos recibidos: {args}")  print(f"Hola, {args.name}!") if args.age:     print(f"Tienes {args.age} años.")`
    
    Usamos los argumentos para personalizar el comportamiento del script. Si `--verbose` está presente, imprimimos todos los argumentos recibidos. Luego saludamos al usuario por su nombre y, si se proporciona, también imprimimos su edad.
    

### Ejecución del script

Para ejecutar este script desde la línea de comandos, podrías usar:

bash

Copiar código

`python script.py --name Juan --age 28 --verbose`

Esto imprimiría:

css

Copiar código

`Argumentos recibidos: Namespace(name='Juan', age=28, verbose=True) Hola, Juan! Tienes 28 años.`


