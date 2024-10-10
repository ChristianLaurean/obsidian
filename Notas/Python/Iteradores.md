---
Fecha_creación: 2024-05-24
Categorias: "[[Python]]"
tags:
  - Programación
URL:
---


```python
# Create an iterator for range(3): small_value
small_value = iter(range(3))
# Print the values in small_value
print(next(small_value))
print(next(small_value))
print(next(small_value))
```

# Range

Range es un iterador de python que genera una lista de numeros de inicio a un final y crea una secuencia, Pero no es eficiente. ******

```python 
listta = list(range(1,50))
```
# Enumerate

>[!tip] Para que sirve
>Crea un par de elementos de indice para cada elemento del objeto propocionado y produce una lista de valores en **[[Tuplas]]**
>![[Pasted image 20240624100718.png]]
>Ejemplo para desenpaquetar
>```python
>lista = [1,2,4]
>for ixt,item in enumerate(lista):
>	print(ix)
>```


```python
lista = [a,b,c]
mis_tuplas = list(enumerate(lista)) # nos da una lista con sus indices de cada cosa y las retorna en una tupl.
# Create a list of strings: mutants

mutants = ['charles xavier',
	'bobby drake',
	'kurt wagner',
	'max eisenhardt',
	'kitty pryde']
# Create a list of tuples: mutant_list

mutant_list = list(enumerate(mutants,start=1))
# respuesta
[(0, 'charles xavier'), (1, 'bobby drake'), (2, 'kurt wagner'), (3, 'max eisenhardt'), (4, 'kitty pryde')]
```

# ZIP 

>[!tip] Sirve para unir dos [[Listas]] interlazando los elementos por [[Tuplas]]
>```python
>nombre = ['Ana','hugo','Valeria']
>edad = [65,29,42]
>
>conbinados = list(zip(nombre,edad)) # Se interlazan los datos en una tupla [('Ana',65)]

# collections 

Es un modulo que contiene tipos de datos especilizados que se pueden usar como alternativa a las [[Listas]],[[Diccionarios]],[[set]],[[Tuplas]]
`from collections import <cualquiera_de_abajo>` 
- `namedtuple`
- `deque`
- `Counter`
- `OrderedDict`
- `defaultdict` 

###### Counter

```python
from collections import Counter

type_counts = Counter(poke_types) # -> retorna un diccionario
```

## itertools 

- `product` 
- `permutations` 
- `combinations` 
problema: Queremos reunir todos los pares de combinación de tipos de pokemon posible 

* Solución no eficiente 
![[Pasted image 20240809122308.png]]
- Solución eficiente 

### Lo podemos decomprimir con * o list

```python
respuesta = zip(*conbinados)
```

![[Pasted image 20240809122451.png]]


# iterar archivos con [[Pandas]]

**`iterator=True`**: Este parámetro hace que la función `pd.read_csv` devuelva un objeto de tipo iterador en lugar de cargar todo el archivo CSV en un solo DataFrame. Esto es útil para trabajar con archivos grandes que no caben en memoria.

**`chunksize=10000`**: Este parámetro se utiliza junto con `iterator=True` y especifica el tamaño de los "chunks" (fragmentos) en los que se divide el archivo CSV. En este caso, el archivo se leerá en fragmentos de 10,000 filas cada uno.
```python
df_taxi = pd.read_csv("yellow_tripdata_2021-07.csv", iterator=True)
```



# chunksize 

Nos ayuda a separar un DataFrame a partes mas pequeñas.

```python
# Initialize an empty dictionary: counts_dict

counts_dict = {}


# Iterate over the file chunk by chunk

for chunk in pd.read_csv("tweets.csv", chunksize = 10):

	# Iterate over the column in DataFrame
	for entry in chunk["lang"]:
		if entry in counts_dict.keys():
		counts_dict[entry] += 1
		else:
		counts_dict[entry] = 1

# Print the populated dictionary

print(counts_dict)

```
