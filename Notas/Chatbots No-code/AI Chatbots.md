---
Fecha_creación: 2024-10-09
Categorias: "[[Chatbots No-Code]]"
tags:
  - Fundamentos
URL: https://www.youtube.com/watch?v=SWP3k-24jT4&t=458s
---


### Chatbots Tradicionales vs Chatbots de IA

1. **Chatbots Tradicionales (Old School)**:
    
    - Son limitados y manuales.
    - Operan basados en reglas predefinidas, lo que significa que solo pueden manejar situaciones que estén dentro de esas reglas. No pueden adaptarse a consultas fuera de este marco.
2. **Chatbots con IA**:
    
    - Utilizan un **modelo de lenguaje grande (LLM)** para interpretar y comprender la consulta del usuario.
    - Son más flexibles y capaces de adaptarse a una amplia variedad de solicitudes.


### Lógica de los Chatbots con IA de bajo nivel

1. **Prompt del usuario**:
    - El usuario formula una pregunta o hace una consulta.
2. **Búsqueda en la base de conocimiento**:
    - El chatbot busca en su base de datos o sistema de conocimiento para comprender mejor la solicitud.
3. **LLM**:
    - La IA procesa la solicitud del usuario utilizando la base de conocimiento, generando una respuesta adecuada.
4. **Respuesta**:
    - El chatbot devuelve una respuesta al usuario basada en el análisis y procesamiento de su solicitud.

 
>[!warning] Problema: La Limitación de los Tokens
>El gran desafío con los chatbots impulsados por IA está relacionado con la **limitación de tokens**. Los tokens incluyen:
>- El prompt del usuario.
>- La base de conocimiento.
>- La memoria del modelo.
>- La respuesta generada.
>Cuanto más larga sea la respuesta, más tokens consume, lo que puede limitar la efectividad de la IA.
>
>**Tabla de tokens**
>![[Pasted image 20241009083623.png]]


### Solución: **Chunking**

El **chunking** es una técnica que ayuda a superar la limitación de tokens. Esta técnica consiste en dividir la base de conocimiento en fragmentos más pequeños, seleccionando solo los más relevantes para la consulta del usuario.

Proceso de Chunking:

1. El usuario envía un prompt.
2. La base de conocimiento se divide en fragmentos más pequeños.
    - Para determinar qué fragmentos son más importantes, se utilizan **embeddings**, que capturan el significado semántico de los textos.
3. Se recuperan los fragmentos más relevantes basados en la consulta del usuario.
4. Se crea un nuevo mensaje que incluye la pregunta del usuario junto con los fragmentos más importantes.
5. Este nuevo prompt se alimenta al LLM.
6. Finalmente, la IA genera y devuelve una respuesta al usuario.

![[Pasted image 20241009084654.png]]

# [[Embeddings]] 

Los **embeddings** son representaciones numéricas de palabras o fragmentos de texto, que capturan su **significado semántico** en un espacio multidimensional. Cada palabra o fragmento se convierte en un vector numérico, y la proximidad entre estos vectores indica cuán similares son en cuanto a significado.

### Explicación detallada de embeddings:

![[Pasted image 20241009085149.png]]1. **Puntos en un espacio**:  
Cada palabra o fragmento de texto se representa como un punto en un espacio multidimensional. Estos puntos están ubicados según el significado semántico del texto.

- **Ejemplo visual**: Imagina un gráfico donde palabras como "perro" y "gato" están cerca porque comparten un contexto semántico similar (ambos son animales domésticos), mientras que "perro" y "mesa" estarán más distantes porque no están relacionados en significado.

![[Pasted image 20241009085440.png]]
2. **Vectores numéricos**:  
    Las frases, palabras o fragmentos de texto se convierten en vectores, es decir, representaciones numéricas que consisten en una serie de números. Estos números codifican aspectos del significado del texto.
    
    - **Ejemplo**: La palabra "rey" puede tener una representación vectorial como [1.2,−0.5,0.8][1.2, -0.5, 0.8][1.2,−0.5,0.8], mientras que "reina" podría ser [1.3,−0.4,0.9][1.3, -0.4, 0.9][1.3,−0.4,0.9], lo que sugiere que son similares pero no idénticas.

3. **Similitud en el espacio**:  
	La proximidad de los puntos (vectores) en este espacio multidimensional indica similitud de significado.
	
	- **Similares**: Cuando los vectores están cercanos entre sí, significa que las palabras o frases tienen significados similares.
	- **Distantes**: Si los vectores están alejados, los significados de las palabras o frases son diferentes.

4. **Medición de la similitud**:  
	La similitud entre dos vectores se mide calculando la distancia entre ellos, normalmente utilizando métricas como la distancia coseno o la euclidiana.
	
	- **Ejemplo**: Si dos vectores tienen una pequeña distancia entre sí, los significados de las palabras o frases son más cercanos (e.g., "gato" y "perro"). Si la distancia es grande, los significados son más diferentes (e.g., "gato" y "coche").

### Resumen:

- **Embeddings** transforman palabras y fragmentos de texto en **vectores numéricos** que representan su significado semántico.
- Los **vectores similares** estarán **cerca** entre sí en el espacio multidimensional, lo que indica que los significados de las palabras son similares.
- Al medir la **distancia entre vectores**, podemos cuantificar cuán relacionados están los significados de diferentes palabras o frases.


## Lógica de los Chatbots con IA de Alto nivel

![[Pasted image 20241009090107.png]]
