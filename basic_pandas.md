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

