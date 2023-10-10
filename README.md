# Programación de Computadores - UNAL
# Arreglos

## Listas 
<table cellspacing="1" bgcolor="">
	<tr bgcolor="#252582">
		<th><b>Definición</b></th>
	</tr>
	<tr bgcolor="#e4e4ed">
		<td style="color:#141414">Una lista es una secuencia de elementos que puede almacenar datos heterogeneos tales como: enteros, reales, cadenas, tuplas, diccionarios y otros m as, inclusive otras listas. Una lista se escribe como la secuencia de datos a mantener, separados por una coma (,), y delimitada por los par entesis cuadrados [].<br>
    La principal caracteristica de una lista es la <b>mutabilidad</b>, lo que implica que pueda ser modificada luego de haberse definido.</td>
	</tr>
</table>


**Ejemplo 1:** Ejemplos de listas en python.

```python
# Lista vacia
lista = []
lista2 = list()
# Lista con un elemento tipo int
listaEntero = [1]
# Lista con dos elementos tipo int
listaEnteros = [1, 2]
# Lista con un string y un entero
listaMixta = ['hola', 1]
# Lista con cinco elementos
listaVariada = [1, 2, 'tres', 4.0, "cinco"]
```

Las listas tienen dos atributos: el elemento almacenado y el indice.
 - **Variable almacenada:** Puede ser un objeto de cualquier tipo (de momento pensémoslo como una variable de los tipos fundamentales de *Python*).
 - **Indice:** Es la posición en la cual se almacena la variable. Se trata de un dato entero que inicia sigue la secuencia *cantidad - 1* elemntos de la lista, esto es, el primer indice es 0, el segundo 1 hasta llegar a *n-1*, donde n es la cantidad de elementos de la lista.

**Ejemplo 2:** Acceso por indice
```python
# Lista con cinco elementos
listaVariada = [1, 2, 'tres', 4.0, "cinco"]
print(listaVariada)
print(listaVariada[0]) # Imprime 1
print(listaVariada[1]) # Imprime 2
print(listaVariada[2]) # Imprime tres
print(listaVariada[3]) # Imprime 4.0
print(listaVariada[4]) # Imprime cinco
```

## Operadores 
### Concatenar
Se utiliza el operador *+* concatena de forma horizontal las listas operadas.

**Ejemplo 3:** Concatenación de listas
```python
lista1 = [1, 2, 3]
lista2 = ['A', 'B', 'C']
lista3 = lista1 + lista2
print(lista3) # [1, 2, 3, 'A', 'B', 'C']
```

### Repetir
Se utiliza el operador *, el cual repite de forma horizontal la lista un número entero de veces.
**Ejemplo 4:** Repetición de listas

```python
lista1 = [1, 2, 3]
lista4 = lista1*2
print(lista4) # [1, 2, 3, 1, 2, 3]
```

### Indexación y slicing
Utilizando en operador *[index]* se accede a los elementos de la lista. En python se deben tener en cuenta algunos elementos importantes a la hora de manipular los subindices:
 - Se inicia con 0 y termina en *n-1*, donde n es la cantidad de elementos de la lista. 
 - Si se da un indice superior a *n-1* se tiene como resultado error de ejecución.
 - Python soporta indices negativos, donde -1 retorna el último elemento, -2 el penultimo y asi sucesivamente (*awesome*).
 

**Ejemplo 5:** Indexación
```python
lista5 = [1, 2, 3, 4, 5]
print(lista[0]) # Imprime 1
print(lista[3]) # Imprime 4
print(lista[-1]) # Imprime 5
print(lista[-2]) # Imprime 4
```

**Ejemplo 6:** Problemas con la Indexación
```python
lista5 = [1, 2, 3, 4, 5]
print(lista[5]) # IndexError list index out of range
```

El *slicing* es quizá la operación mas poderosa de listas y tuplas en python. No creo poder explicarlo mejor de lo que está en este [post](https://stackoverflow.com/questions/509211/understanding-slicing) de *stackoverflow*.

### Existencia
Se puede utilizar el operador *in* para determinar si un elemento hace parte de una lista. La respuesta del operador es *True* si el elemento se encuentra en la lista y *False* en caso contrario.

**Ejemplo 7:** Operador *in*
```python
lista5 = [1, 2, 3, 4, 5]
print(5 in lista5) # True
```

Para que dimensionen el poder de este operador, si se quiere buscar un elemento en una lista desordenada, el pero caso es recorrer toda la lista y comparar elemento a elemento.
```python
lista5 = [1, 2, 3, 4, 5]
bandera : bool = False
for n in lista5:
  if n == 5 : bandera = true
print(bandera)
```

**Disclaimer:** En una lista de un par de elementos parece trivial, pero en una lista de 1.000.000 de datos sí se va a ver la diferencia.

### Recorrer listas 
#### the for approach
Es la manera más práctica, en lo técnico, *Phyton* crea una ennumeración y se recorre con el ciclo for.

**Ejemplo 7:** *for* para recorrer una lista.
```python
lista5 = [1, 2, 3, 4, 5]
for i in lista5:
	print(i) 
```

```python
lista5 = [1, 2, 3, 4, 5]
for i in range(0,len(lista5)):
	print(lista5[i]) 
```

#### the while approach
Para recorrer una lista se debe utilizar la indexación y un indice con actualización.

**Ejemplo 7:** *while* para recorrer una lista.
```python
lista5 = [1, 2, 3, 4, 5]
i : int = 0
while i < len(lista5)
	print(lista5[i]) 
```

### List comprenhension (estaba dificil de traducir)
Es una forma generar listas a partir de condiciones especificas en una sola linea de código.

**Ejemplo 8:** Lista con cubos del 3 al 6.
```python
listaCubos = [x**3 for x in range(3,7)]
print(listaCubos) 
```

```python
listaCubos = [(lambda x : x**3) for x in range(3,7)]
print(listaCubos) 
```

```python
listaCubos = [27, 64, 125, 216] # Hardcoded
print(listaCubos) 
```

```python
listaCubos = list(range(3,7)) # Dolor
for i in range(3,7):
	listaCubos[i] = listaCubos[i]**3
print(listaCubos) 
```

## Métodos utiles
### len
Retorna la cantidad de elementos de una lista.

**Ejemplo 9:** Usos de *len()*
```python
lista = [1, 2, 3, 4]
nombre = ["Minch", "Yoda"]
trabajo = ["Stars", "War", "Movie"]
empty = []
print(len(lista))
print(len(nombre))
print(len(trabajo))
print(len(empty))
```

### append
Agrega elementos al final de la lista.

**Ejemplo 10:** Usos de *append()*
```python
nombres = ["Antonio", "Johan"]
nombres.append("Monica")
print(nombres)
nombres.append("Maria")
print(nombres)
nombres.append("Mabel")
print(nombres)
```

### pop
Elimina el elemento de un determinado índice, en caso de no especificarse índice, se elimina el último elemento. El método *pop* retorna el elemento eliminado.

**Ejemplo 11:** Usos de *pop()*
```python
nombres = ["Antonio","Johan","Monica","Maria","Mabel"]
nombres.pop(1) #remueve a Johan
print(nombres)
nombre_borrado = nombres.pop() # remueve a Mabel
print(nombre_borrado + " ha sido eliminada de la lista.")
print(nombres)
```

### insert
Permite insertar (agregar) elementos en una posición específica de una lista.

**Ejemplo 12:** Usos de *insert()*
```python
nombres = ["Antonio", "Johan", "Maria"]
nombres.insert(0, "Guttag")
print(nombres)
nombres.insert(2, "Peter")
print(nombres)
nombres.insert(len(nombres)//2, 10)
print(nombres)
```

### remove
Permite eliminar la primera aparición (de izquierda a derecha) de un elemento de una lista.

**Ejemplo 13:** Usos de *remove()*
```python
lista = ["a", "e", "i", "o", "u", "i", "x"]
lista.remove("x")
print(lista)
lista.remove("i")
print(lista)
lista.remove("i")
print(lista)
```

### count
Obtiene las veces que un elemento se encuentra en una lista.

**Ejemplo 14:** Usos de *count()*
```python
lista = [4, 3, 8, 8, 2, 5, 4, 6, 8, 9]
print(lista.count(2))
print(lista.count(8))
print(lista.count(5))
print(lista.count(7))
```

### index
El método index obtiene la primera ocurrencia de un elemento en una lista. Si el objeto buscado no se encuentra en la lista, se generará una excepción....luego vemos como pilotearlo.

**Ejemplo 15:** Usos de *index()*
```python
lista = [4, 3, 8, 8, 2, 5, 4, 6, 8, 9]
print(lista.index(2))
print(lista.index(8))
print(lista.index(5))
```

### max - min
Obtiene el máximo/mínimo elemento de una lista.

**Ejemplo 16:** Usos de *max() / min()*
```python
t = [4, 5, -1, 6, 7]
print(max(t))
print(min(t))
```

### sort
Ordena una lista. Se le puede indicar si ascendente o descendentemente, al igual que el criterio (llave) usado para ordenar.

**Ejemplo 16:** Usos de *sort*
```python
lista = [4, 5, -1, 6, 7]
lista.sort() # De menor a mayor
print(lista)
lista.sort(reverse = True) # De mayor a menor
print(lista)
```

**Ejercicio:** Revisar la diferencia entre sort() y sorted().

## Listas como arreglos
Un arreglo o vector es una tupla o **lista** de n elementos del mismo tipo (En este curso usaremos las listas para representar arreglos). A los elementos de un arreglo se les llama componentes del arreglo.

 - []: Arreglo vacio.
 - [1, 0, 7, -2, 8]: Un arreglo de enteros de 5 componentes.
 - ['Radio', 'Lado']: Un arreglo de cadenas de 2 componentes. 
 - [1.3, 2.4, -3.0, 4.5]: Un arreglo de reales de 4 componentes.
 - [True, False, False]: Un arreglo de booleanos de 3 componentes.

En general, un arreglo *v* se puede representar de la siguiente forma:

$$ v = [v_0, v_1, v_2, \cdots , v_{n-2}, v_{n-1}]$$

donde el arreglo está constituido por n componentes.

En general las listas tienen todas las propiedades para definir un vector en el sentido matemático, no obstante los operadores definidos para las listas, no están sobrecargados para representar operaciones matemáticas, para ello en el futuro se usará [numpy](https://numpy.org/).

## Reto 10
Desarrolle la mayoría de ejercicios en clase. Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_10 en slack.

1. Desarrollar un algoritmo que calcule el promedio de un arreglo de reales.
2. Desarrollar un algoritmo que calcule el [producto punto](https://www.cuemath.com/algebra/dot-product/) de dos arreglos de números enteros (reales) de igual tamaño.
3. Hacer un algoritmo que deje al final de un arreglo de números todos los ceros que aparezcan en dicho arreglo.
4. Revisar que son los algoritmos de *sorting*, entender *bubble-sort* ([enlace](https://www.geeksforgeeks.org/bubble-sort/) a implementación).
