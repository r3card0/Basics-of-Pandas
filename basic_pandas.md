# Pandas

## Importar librerias
````
import pandas as pd
import numpy as np
````

# Como crear series
La serie es un conunto de elementos ordenadas. Es una lista ordenada.
````
serie1 = pd.Series([10,8,4,45,6]
````
## Como conocer las propiedades de una Serie: values
Lista los elementos de una serie (lista)
````
Serie1.values
````
output
````
array[(10,8,4,45,6)]
````

## Como indexar una serie: index
Se puede asignar valores a los indices de una serie.

Previo a la asignacion de valores al indice, se puede ver el tipo de indice actual de la serie con el comando:
````
serie1.index
````
output
````
RangeIndex(start=0,stop=5,step=1)
````
Asignar nuevos valores al indice
````
serie1 = pd.Series([10,8,4,45,6], index = ['a','b','c','d','e'])
````
Ver de nuevo el tipo de indice
````
serie1.index
````
output 
````
Index(['a', 'b', 'c', 'd', 'e'], dtype='object')
````

## Como accesar a los elementos de una Serie
Se usa los "*[ ]*" para accesar a los elementos de la serie. Accesar y mostrar el elemento de la posicion *3*
````
serie1[3]
````
output
````
45
````

# Como crear diccionarios
Un diccionario es una estructura de datos que almacena informacion en pares.

Forma manual para crear un diccionario
````
# crear un diccionario con verbos irregulares en inglés
irregular_verbs = {
    "base form" : "arise",
    "past" : "arose",
    "participle": "arisen"
}
````
En la variable *irregular_verbs* se almaceno el diccionario y sus elementos. Para visualizar el contenido de un diccionario.
````
print(irregular_verbs)
````
Output
````
'base form': 'arise', 'past': 'arose', 'participle': 'arisen'}
````
## Como acceder a los keys de un diccionario: *keys()*
Para acceder a los keys de un diccionario se usa el metodo **keys()**
````
irregular_verbs.keys()
````
output
````
dict_keys(['base form', 'past', 'participle'])
````
## Como acceder a los values de un diccionario: *values()*
Para acceder a los *values* de un diccionario, se usa el metodo **values()**
````
irregular_verbs.values()
````
output
````
dict_values(['arise', 'arose', 'arisen'])
````
## Como acceder al valor de una *key* deternminada
Usar una *key* para acceder a su valor.
````
irregular_verbs['past']
````
output
````
'arose'
````



