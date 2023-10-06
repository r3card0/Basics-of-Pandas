# Logica a seguir para filtrar datos.

Filtrar varias columnas, un valor
* Filtro 1: col1:1, col2:True, col3 any value
````
def filtro1():
  # 1. crear dataframe
  # 2. aplicar filtro
  df = df[(df['col1'] == 1) & (df['col2´] == True)]
  return df
````
En este filtro, no se considera el valor de la col3 porque no importa que valor se escoga.

* Filtro 2: col1:1 y2 , col2:False, col3: 'a' y 'z'
````
def filtro2():
  # 1. crear dataframe
  # 2. aplicar filtro
  df = df[(df['col1'].isin([1,2]) & (df['col2'] == False) & (df['col3'].isin(['a','z']))]
  return df
  
  
