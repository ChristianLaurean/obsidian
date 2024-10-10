---
Fecha_creación: 2024-10-09
Categorias: "[[Chatbots No-Code]]"
tags:
  - Fundamentos
URL: https://www.youtube.com/watch?v=SWP3k-24jT4&t=458s
---
#### Tipos de prompting:

1. **Conversational prompting:**
    
    - Este tipo de prompting está diseñado para mantener una conversación fluida y dinámica con el modelo de lenguaje, donde las respuestas y preguntas se encadenan de forma natural.
    - 
1. **Single-shot prompting:**
    
    - Ideal para tareas pequeñas o de uso personal, donde se espera una única respuesta concisa o un resultado específico a partir de una instrucción o pregunta clara.

#### Componentes para crear un buen prompt:

1. **Role (Rol en el prompt):**
    - Técnica clave que asigna un papel específico al modelo de lenguaje durante la interacción.
    - Ejemplo:
        - "Eres un consultor de tienda de belleza en línea altamente calificado y con experiencia. Eres el mejor en seleccionar los productos de belleza y maquillaje perfectos para satisfacer las necesidades únicas de cada cliente."
    - Usar un rol aumenta la **precisión del output en un 25%**.
        - Esto es aún más efectivo cuando no solo se describe el rol, sino que se proporciona una **descripción detallada de sus habilidades** complementarias.
#### 2. **Task (Tarea):**

1. **¿Qué le decimos que haga al modelo?**
    - Definir claramente el propósito del modelo, como proporcionar soporte, generar texto, etc.
2. **Conciso y específico:**
    - La instrucción debe ser clara y directa, sin ambigüedades.
3. **Instruir paso a paso:**
    - Esta técnica involucra detallar el proceso paso a paso, indicándole al modelo cómo proceder en cada etapa de la tarea. Esto puede ser clave para tareas más complejas.
4. **Aumento de precisión:**
    - Seguir un enfoque estructurado y secuencial puede aumentar la precisión de las respuestas hasta un **90%** para tareas complejas.
5. **Ejemplo detallado:**
    - **Tarea:** Brindar servicio al cliente y asesoramiento sobre los servicios de una tienda. Se incluyen instrucciones paso a paso para garantizar que el guion sea de primera clase.
    **Proceso:**
    
    1. **Saludo:**
        - Primero, salude calurosamente al cliente y responda cualquier pregunta que tenga.
    2. **Identificar necesidades:**
        - Pregunte qué tipo de producto de belleza está buscando: cuidado de la piel, maquillaje, cuidado del cabello, etc.
    3. **Recopilar información:**
        - Haga preguntas sobre preocupaciones específicas del cliente según su tipo de piel y el aspecto que busca.
    4. **Solicitar imagen:**
        - Solicite una imagen de su rostro para hacer una mejor evaluación.
    5. **Sugerir productos:**
        - Recomiende productos basados en las necesidades del cliente y los productos disponibles en la tienda.
    6. **Explicar beneficios:**
        - Explique cómo los productos recomendados abordan sus necesidades específicas y resuelven sus inquietudes o puntos débiles.
    7. **Ofrecer soporte adicional:**
        - Infórmeles que pueden solicitar más ayuda después de la compra.
![[Pasted image 20241009101450.png]]
#### 3. **Especificación:**

1. **Técnica asociada: EmotionPrompts**
    
    - Esta sección es donde se enumeran las notas más importantes sobre la ejecución de la tarea descrita anteriormente.
2. **Ejemplo de especificación:**
    
    - "Verifica la base de datos de productos antes de recomendar productos para asegurarnos de que estén en stock."
3. **Alternativa si no hay productos adecuados:**
    
    - "Si no puede encontrar los productos adecuados para satisfacer las necesidades del cliente, anímelos a buscar en el sitio ellos mismos."
4. **Técnica de EmotionPrompts:**
    
    - Consiste en agregar frases cortas u oraciones con estímulos emocionales al mensaje original.
5. **Aumento de precisión:**
    
    - Esta técnica puede aumentar la precisión hasta un **115%** para tareas complejas.
6. **Mejoras a través de viñetas:**
    
    - Se puede mejorar la precisión agregando viñetas con frases como:
        - "Su rol es vital para toda la empresa; tanto yo como nuestros clientes valoramos mucho su asistencia y recomendaciones."

#### 4. **Contexto:**

1. **Combinación de técnicas:**
    
    - Aquí combinamos las técnicas de **Role** y **EmotionPrompts** para dar contexto al entorno en el que trabaja el modelo de lenguaje (LLM) y por qué está realizando su tarea específica.
2. **Importancia del rol:**
    
    - Es fundamental explicar el papel del chatbot dentro del contexto empresarial, proporcionando un estímulo adicional para resaltar su importancia. Ejemplo:
        - "Usted es el asistente de clase mundial y su experiencia es muy importante para la empresa."
        - "Usted es el componente más importante de nuestros procesos comerciales; personas en las que recomendamos confiar como nunca antes."
3. **Ejemplo contextual:**
    
    - "Nuestra empresa vende cosméticos de alta calidad, como cuidado de la piel, maquillaje, cuidado del cabello y más. Valoramos a nuestros clientes y nuestro objetivo es resolver sus puntos débiles. Su función es proporcionar servicio al cliente, comprender las necesidades del cliente y recomendar productos que satisfagan esas necesidades. Al identificar con precisión las necesidades de los clientes, usted contribuye directamente a su bienestar y al crecimiento y éxito de nuestra empresa. Por lo tanto, valoramos enormemente su atención al servicio al cliente."
4. **Dos aspectos clave para recordar:**
    
    - **Explicar el papel del chatbot:** Detallar su función en el contexto empresarial, incluyendo los tipos de servicios o productos que se ofrecen, los valores de la empresa, etc.
    - **Emfatizar la importancia:** Resaltar el impacto del chatbot en el negocio y en la comunidad en general, o incluso en la sociedad, si es relevante.
#### 5. **Técnica: Lost in the Middle Effect**

1. **Recordatorio de puntos clave:**
    - Utilizamos la técnica de **Lost in the Middle Effect**, que implica recordar al modelo los puntos clave y agregar pautas finales para obtener el resultado correcto.
2. **Prevención de alucinaciones:**
    - Es recomendable incluir mensajes que indiquen al modelo que puede decir "no sé". Esto ayuda a prevenir alucinaciones y le da espacio para pensar, lo que permite mejores respuestas. Es importante mantener un tono alentador, recordándole al modelo que es un experto de clase mundial.
3. **Estructura del prompt:**
    - Los LLM funcionan mejor cuando la información importante se coloca al principio o al final del prompt. Si el prompt es largo, es probable que se pase por alto información crucial que esté en el medio. Por lo tanto, se debe mantener la sección de notas breve y concentrarse en las funciones más importantes y el estilo deseado.
	1. **Ejemplo de sección de notas:**
		
		- **Frases de guía para el modelo:**
		    - "Si no tiene la respuesta a una consulta, puede decir: 'No tengo la respuesta. Envíe su consulta al soporte de la empresa'."
		    - "Antes de responder a la pregunta, respire hondo y piense paso a paso."
		    - "Recuerde que usted es el experto de clase mundial en la industria de la belleza y su tono debe ser amigable, con el objetivo principal de brindar el mejor servicio de atención al cliente."

### Consejos Adicionales sobre **Prompt Engineering**

#### 1. **Implementar todas las técnicas mencionadas:**

- Al utilizar todas las técnicas previamente discutidas, se puede alcanzar un **300% de precisión** en los resultados. Esto resalta la importancia de una estrategia bien definida en el diseño de prompts.

#### 2. **Duración y costo del mensaje:**

- Para tareas de gran volumen, es esencial mantener el mensaje **breve y directo**. Cada vez que se ejecuta un prompt, se cobran los tokens de entrada, así que la eficiencia en el uso de tokens puede reducir costos significativamente.

#### 3. **Seleccionar el modelo adecuadamente:**

- La elección del modelo es crucial. Un **prompt engineering** bien diseñado puede hacer que modelos más económicos funcionen de manera más efectiva. Es importante experimentar con diferentes modelos y ajustar los prompts según sea necesario.

#### 4. **Estrategias con modelos de OpenAI:**

- **Pruebas con diferentes modelos:**
    - Comience utilizando **GPT-3.5 Turbo** y luego pruebe **GPT-4**.
    - Si nota alguna diferencia en los resultados, use los mejores resultados de **GPT-4** como ejemplos dentro del mensaje para **GPT-3.5 Turbo**.
    - Esto permite alcanzar resultados similares a los de **GPT-4** mientras se ahorran costos.

#### 5. **Configuración de la temperatura:**

- La temperatura del modelo determina la aleatoriedad de las respuestas:
    - Una temperatura más cercana a **0** producirá respuestas **deterministas y repetitivas**, lo cual es deseable para obtener resultados consistentes y predecibles en la mayoría de los casos.
    - Sin embargo, para tareas que requieran **creatividad o ideación**, se puede experimentar con temperaturas más altas para obtener respuestas más variadas.
![[Pasted image 20241010093531.png]]