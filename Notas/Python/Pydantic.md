---
Fecha_creación: 2024-08-30
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---

Es una biblioteca en Python que permite la validación de datos a través de modelos de datos tipados, asegurando que los datos cumplan con ciertas restricciones y tipos antes de que se utilicen en la aplicación.

### Ejemplo de Uso

Imagina que tienes una aplicación que pregunta a un LLM sobre detalles de un producto. Puedes usar `pydantic` para definir la estructura del producto y validar la respuesta.

```python
from typing import Optional
from pydantic import BaseModel, Field

class Person(BaseModel):
    """Information about a person."""

    # Cada campo es opcional, permitiendo que el modelo decline extraerlo si no tiene información.
    # Las descripciones proporcionan contexto adicional al LLM para mejorar la precisión de la extracción.
    
    name: Optional[str] = Field(
	    default=None, description="The name of the person")
    lastname: Optional[str] = Field(
        default=None, description="The lastname of the person if known")
    country: Optional[str] = Field(
        default=None, description="The country of the person if known")
```

```python
class Classification(BaseModel):

Classification_sentiment: str = Field(
	...,
	enum=["Positivas","Negativas","Neutras"],
	description="La clasificación de las reviews del producto"
)
```
### Explicación Detallada

1. **Uso de `BaseModel`**: `Person` hereda de `BaseModel`, que es la clase base de `Pydantic`. Esto permite que `Person` valide datos de manera automática y convierte los valores en los tipos correctos.
    
2. **Campos Opcionales**:
    
    - Cada campo (`name`, `lastname`, `country`) está definido como `Optional[str]`. Esto indica que estos campos son opcionales y pueden ser `None` si la información no está disponible.
    - Esto es útil en aplicaciones LLM, donde no siempre se puede garantizar que toda la información esté disponible o sea extraíble.
3. **Campo `Field`**:
    
    - `Field` se utiliza para proporcionar configuraciones adicionales a cada campo, como un valor por defecto (`default=None`) y una `description`.
    - La descripción es especialmente importante porque se envía al LLM como un contexto adicional, ayudando al modelo a entender mejor qué tipo de información debería extraer para cada campo.
4. **Doc-strings**:
    
    - El doc-string de la clase `Person` (`"""Information about a person."""`) y los comentarios en cada campo sirven como documentación y contexto adicional para el LLM.
    - El LLM utiliza esta información para mejorar la precisión al intentar extraer detalles sobre una persona.