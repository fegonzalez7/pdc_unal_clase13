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
 - **Variable almacenada:** Puede ser un objeto de cualquier tipo (de momento pensemoslo como una variable de los tipos fundamentales de *Python*).
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
**Ejemplo 7:** Operador *in*
```python
lista5 = [1, 2, 3, 4, 5]
print(5 in lista5) # True
```


#### the while approach



### List comprenhension (estaba dificil de traducir)

## Métodos utiles
### len

### append

### pop

### insert

### remove

### count

### index

### min

### max

### sort

## Listas como arreglos


