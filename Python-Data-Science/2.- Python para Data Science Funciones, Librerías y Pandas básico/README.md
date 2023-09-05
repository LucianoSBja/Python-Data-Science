# Conocimiento de tupla

- **Las tuplas son inmutables, lo que significa que no se pueden modificar una vez que se han creado.**
- **Las tuplas pueden contener objetos de diferentes tipos, mientras que las listas solo pueden contener objetos del mismo tipo.**

## Creación de tuplas

Hay varias formas de crear tuplas en Python. La forma más básica es usar paréntesis para encerrar los objetos que queremos incluir en la tupla. Por ejemplo, la siguiente línea crea una tupla con los números 1, 2 y 3:

```python
tupla = (1, 2, 3)


También podemos crear tuplas usando una coma para separar los objetos. Por ejemplo, la siguiente línea crea la misma tupla que la anterior:

python
tupla = 1, 2, 3


Podemos usar variables para crear tuplas. Por ejemplo, la siguiente línea crea una tupla con el nombre y el valor de un vehículo:

python
nombre = "Passat"
valor = 153000
tupla = (nombre, valor)


Finalmente, podemos usar el método `tuple()` para convertir una lista en una tupla. Por ejemplo, la siguiente línea convierte la lista `["Passat", "Golf", "Audi A3"]` en una tupla:

python
nombres_carros = ["Passat", "Golf", "Audi A3"]
tupla = tuple(nombres_carros)


## Acceso a los elementos de una tupla

Los elementos de una tupla se pueden acceder usando índices. Los índices de las tuplas comienzan en 0, por lo que el primer elemento tiene el índice 0, el segundo elemento tiene el índice 1, y así sucesivamente.

Para acceder a un elemento de una tupla, podemos usar el operador `[]`. Por ejemplo, la siguiente línea imprime el segundo elemento de la tupla `tupla`:

python
print(tupla[1])


También podemos usar la función `len()` para obtener la longitud de una tupla. Por ejemplo, la siguiente línea imprime la longitud de la tupla `tupla`:

python
print(len(tupla))
```

<br>

# Selecciones en Tuplas

Para seleccionar un elemento único de una tupla, podemos usar el operador []. El operador [] toma dos argumentos: el índice del elemento que queremos seleccionar y el tipo de índice.

El índice de un elemento de una tupla comienza en 0, por lo que el primer elemento tiene el índice 0, el segundo elemento tiene el índice 1, y así sucesivamente.

El tipo de índice puede ser un número entero o un slice. Un slice es una tupla de dos números enteros que indica el rango de elementos que queremos seleccionar.

Ejemplos

```python
# Seleccionar el primer elemento
tupla = ("Jetta Variant", "Passat", "Crossfox", "DS5")
elemento = tupla[0]
print(elemento)

```

Este código imprime el siguiente resultado:

```
Jetta Variant
```

```python
# Seleccionar el último elemento
tupla = ("Jetta Variant", "Passat", "Crossfox", "DS5")
elemento = tupla[-1]
print(elemento)

```

Este código imprime el siguiente resultado:

```
DS5
```

```python
# Seleccionar una secuencia de elementos
tupla = ("Jetta Variant", "Passat", "Crossfox", "DS5")
elementos = tupla[1:3]
print(elementos)

```

Este código imprime el siguiente resultado:

```
('Passat', 'Crossfox')
```

Selección de elementos dentro de tuplas anidadas

Las tuplas pueden anidarse, lo que significa que una tupla puede contener otras tuplas. En este caso, podemos usar el operador [] de manera recursiva para acceder a los elementos de las tuplas anidadas.

Ejemplo

```python
tupla = (("Jetta Variant", "Passat"), ("Crossfox", "DS5"))
elemento = tupla[1][-1]
print(elemento)

```

Este código imprime el siguiente resultado:

```
DS5
```

<br>

# Iterando en tuplas

Para iterar sobre una tupla, podemos utilizar un bucle for. El código siguiente itera sobre la tupla nombres_carros:

```python
nombres_carros = ("Jetta Variant", "Passat", "Crossfox", "DS5")
for carro in nombres_carros:
print(carro)
Utiliza el código con precaución.
```

Este código imprimirá lo siguiente:

```
Jetta Variant
Passat
Crossfox
DS5
Desempaquetando tuplas
```

Podemos desempaquetar una tupla asignando los elementos de la tupla a variables individuales. El código siguiente asigna los elementos de la tupla `nombres_carros` a las variables `carro1`, `carro2`, `carro3` y `carro4`:

```python
nombres_carros = ("Jetta Variant", "Passat", "Crossfox", "DS5")
carro1, carro2, carro3, carro4 = nombres_carros

```

Este código imprimirá lo siguiente:

```
Jetta Variant
Passat
Crossfox
DS5
```

Podemos utilizar el operador `*` para ignorar algunos elementos de una tupla. El código siguiente asigna los elementos de la tupla nombres_carros a las variables `carro1` y `carro4`:

```python
nombres_carros = ("Jetta Variant", "Passat", "Crossfox", "DS5")
carro1, *_, carro4 = nombres_carros

```

Este código imprimirá lo siguiente:

```
Jetta Variant
DS5
```

Utilizando la función `zip()`

La función `zip()` crea un iterador que combina elementos de dos o más colecciones. El código siguiente crea un iterador que combina los elementos de las listas `carros` y `valores`:

````

```python
carros = ["Jetta Variant", "Passat", "Crossfox", "DS5"]
valores = [153000, 185000, 100000, 220000]

carros_y_valores = zip(carros, valores)
````

Podemos recorrer el iterador `carros_y_valores` utilizando un bucle for:

```python
for carro, valor in carros_y_valores:
print(carro, valor)

```

Este código imprimirá lo siguiente:

```
Jetta Variant 153000
Passat 185000
Crossfox 100000
DS5 220000
```

También podemos desempaquetar el iterador `carros_y_valores` en dos variables:

```python
carro, valor = zip(*carros_y_valores)

```

Este código imprimirá lo siguiente:

```
Jetta Variant 153000
Passat 185000
Crossfox 100000
DS5 220000
```

<br>

## En esta aula aprendimos:

- Qué son las tuplas.
- Formas de crear una tupla.
- Técnicas de selección de elementos y particionamiento con tuplas de Python.
- Formas de iterar una tupla.
- La técnica conocida como desempaquetado de tuplas.
- A utilizar la built-in function zip().

<br><br>

# Diccionario

- Los diccionarios son una estructura de datos que almacenan datos en pares de valores. La clave es la llave que se utiliza para acceder al valor.
- Los diccionarios se crean usando llaves {}. Cada elemento del diccionario es un par de valores, que se separan por dos puntos (:).
- Hay dos formas principales de crear diccionarios:
  - Declarando explícitamente las claves y los valores:

```python
datos = {
    "nombre": "Alejandro",
    "edad": 25,
    "sexo": "masculino"
}

```

- Usando el método dict():

```python
datos = dict(nombre="Alejandro", edad=25, sexo="masculino")

```

<br><br>

# Operaciones con Diccionarios

- Para acceder al valor de un elemento de un diccionario, podemos usar el operador de corchetes [ ]. Por ejemplo, para acceder al valor del vehículo Passat, podemos usar el siguiente código:

```python
print(datos['Passat'])

```

- Para buscar si existe una llave dentro de un diccionario, podemos usar el método in. Por ejemplo, para verificar si existe la llave "Passat" en el diccionario datos, podemos usar el siguiente código:

```python
print('Passat' in datos)
```

- Para obtener el tamaño de un diccionario, podemos usar el método len(). Por ejemplo, para obtener el tamaño del diccionario datos, podemos usar el siguiente código:

```python
print(len(datos))
```

- Para adicionar un elemento a un diccionario, podemos usar el operador de asignación. Por ejemplo, para adicionar el vehículo "DS5" al diccionario datos, podemos usar el siguiente código:

```python
datos['DS5'] = 100000
```

- Para eliminar un elemento de un diccionario, podemos usar el método del. Por ejemplo, para eliminar el vehículo "Passat" del diccionario datos, podemos usar el siguiente código:

```python
del datos['Passat']
```

<br><br>

# Metodos con Diccionarios

**update()**: Actualiza o incluye un elemento dentro de un diccionario.
**copy()**: Crea una copia de un diccionario.
**pop()**: Elimina un elemento de un diccionario.
**clear()**: Borra todos los elementos de un diccionario.

**update()**

- Por ejemplo, para actualizar el valor del vehículo Passat de 94 centavos a 95 centavos, podemos usar el siguiente código:

Python

```python
datos.update({"Passat": 95})
```

- Para incluir un nuevo vehículo, por ejemplo el Fusca, que vale 150.000, podemos usar el siguiente código:

```python
datos.update({"Fusca": 150000})
```

**copy()**

- Esta copia es independiente del diccionario original, lo que significa que podemos modificarla sin afectar al diccionario original.

```python
datos_copy = datos.copy()
```

**pop()**

- Para eliminar un elemento de un diccionario, utilizamos el método pop(). Para eliminar el vehículo Passat, podemos usar el siguiente código:

```python
datos.pop("Passat")
```

- Si el elemento no existe, se devolverá un error. Para evitar esto, podemos pasar un mensaje como parámetro al método pop(). Por ejemplo, para indicar que la llave no fue encontrada, podemos usar el siguiente código:

```python
datos.pop("Passat", "Llave no encontrada")
```

**clear()**

- Para borrar todos los elementos de un diccionario, utilizamos el método clear(). Por ejemplo, para borrar el diccionario datos_copy, podemos usar el siguiente código:

```python
datos_copy.clear()
```

<br><br>

# Iterando en diccionarios

El método **keys()** nos devuelve una lista con las llaves del diccionario.
El método **values()**nos devuelve una lista con los valores del diccionario.
El método **items()** nos devuelve una lista de tuplas, cada tupla conteniendo una llave y su valor.

Podemos utilizar un bucle for para iterar sobre los elementos de un diccionario, utilizando cualquiera de estos métodos como referencia.

Por ejemplo, para iterar sobre las llaves de un diccionario, podemos usar el siguiente código:

```python
for llave in diccionario.keys():
  print(llave)
```

Para iterar sobre los valores de un diccionario, podemos usar el siguiente código:

```python
for llave in diccionario.keys():
  print(llave)
```

Para iterar sobre las llaves y los valores de un diccionario, podemos usar el siguiente código:

```python
for llave, valor in diccionario.items():
  print(llave, valor)
```

Por ejemplo, para desempacar los elementos de una tupla, podemos usar el siguiente código:

```python
for key, value in datos.items():
    print(key, "=", value)
```

<br>

## En esta aula aprendimos:

- Estructuras de datos, que representan un tipo de mapeo, conocidas como diccionario, en el lenguaje Python.
- Formas de crear diccionarios en Python.
- Operaciones básicas con diccionarios (pertinencia, acceso, asignación, etc.).
- A utilizar los métodos más importantes de diccionarios (update(), pop(), clear(), etc.).
- Técnicas de iteración en diccionarios.

<br><br>

# Built-in Functions

Las built-in functions son funciones que ya existen dentro del lenguaje Python. No necesitamos crearlas, ya están disponibles, solo tenemos que utilizarlas.

[Built-in Functions]('https://docs.python.org/3/library/functions.html')

<br>
