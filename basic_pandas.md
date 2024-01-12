# Pandas 🐼
- [ ] [Pandas 🐼](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#pandas--1)
- [ ] [Series](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#series)
- [ ] [DataFrame](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#dataframe)

## Pandas 🐼
- [ ] [Como funciona el metodo **to_numeric**](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#como-funciona-el-metodo-to_numeric)

# Series
- [ ] [Como importar librerias](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#importar-librerias)
- [ ] [Como crear Series](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#como-crear-series)
- [ ] [Conocer las propiedades de una Serie](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#como-conocer-las-propiedades-de-una-serie-values)
- [ ] [Como indexar una Serie](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#como-indexar-una-serie-index)
- [ ] [Acceder a los elementos de una Serie](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#como-accesar-a-los-elementos-de-una-serie)
- [ ] [Como crear una Serie a partir de un diccionario](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#como-convertir-diccionarios-en-series)

# DataFrame
- [ ] [Como importar librerias](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#importar-librerias)
- [ ] [Como crear un DataFrame]()
- [ ] [Como crear un DataFrame a partir de un diccionario]()
- [ ] [Como castear columnas en un DataFrame](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#como-castear-columnas-en-un-dataframe)
- [ ] [Como castear de *int64* a *int8* o cualquier otro numerico](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#como-castear-de-int64-a-int8-o-cualquier-otro-numerico)
- [ ] [Como funciona el método **apply( )**](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#c%C3%B3mo-funciona-el-metodo-apply--en-un-dataframe-de-pandas)
- [ ] [Diferencia entre *int32* y *int64*](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#cual-es-la-diferencia-entre-int32-y-int64-en-python)
- [ ] [Como funciona el metodo **assign( )**](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#como-funciona-el-m%C3%A9todo-assign-)

## Importar librerias
````
import pandas as pd
import numpy as np
````

# Como crear series
- [**Series**](https://pandas.pydata.org/pandas-docs/stable/user_guide/dsintro.html#series): Una serie es una lista, pero su mejor definicion es un arreglo unidimensional etiquetado, que es capaz de almacena datos de cualquier tipo  (integers, strings, floating point numbers, Python objects, etc.) Las etiquetas están colectivamente referidas como indice. El método basico para crear una serie:

  ````
  s = pd.Series(data, index=index)
  ````
  

    Datos que pueden ser convertidos a una Serie:

    - Un diccionario de Python

    - Un ndarray

    - Un valor escalar (como 5)


La serie es un conunto de elementos ordenadas. Es una lista ordenada y etiquetada por indices.
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
# Como convertir diccionarios en Series
Para convertir un diccionario en una serie se usa el siguiente codigo
````
serie_from_dict = pd.Serie(irregular_verbs)
````
Al convertir un diccionario a serie, lo que sucede es que las *keys* se vuelven *index* y los values, se convierten en los elementos de la Serie.
````
serie_from_dict
````
output
````
base form      arise
past           arose
participle    arisen
dtype: object
````
Visualizar los indices:
````
serie_from_dict.index
````
output
````
Index(['base form', 'past', 'participle'], dtype='object')
````
## Cambiar de la indexaxion de la Serie
Cambiar la indexacion sustityendo el indice ````'participle'````, por el valor ````'adverb'````
````
pd.Series(irregular_verbs, index = ['base form','past','adverb'])
````
output
````
base form    arise
past         arose
adverb         NaN
dtype: object
````
Se observa que al crear un nuevo indice, el valor correspondiente es nulo *NaN*, lo cual indica que se desconoce su valor


# Como castear columnas en un Dataframe?
Una forma de castear columnas de tipo string a numerico, se puede aplicar un proceso donde se aplican los metodos *to_numeric* y *df.assign( )* 👉[castear un string a numeric](https://github.com/r3card0/Basics-of-Pandas/blob/main/basic_pandas.md#como-funciona-el-metodo-to_numeric)

Cuando un dataframe, tiene una combinación de tipos de datos como son *string*, *númerico*, etc, no se puede usar el metodo
````
df.astype('int32').dtypes
````
Por que marca el siguiente error:
````
ValueError: invalid literal for int() with base 10: 'Chile'
````
Y quiere decir que la columna "Chile" no es candidato para castear a *int32*

## Como castear de int64 a int8 o cualquier otro numerico

# ¿Cómo funciona el metodo *apply( )* en un dataframe de pandas?
El metodo *apply( )*, solo sirve para ejecutar funciones que afectaran al dataframe. Por medio del parametros *axis=*, se define si la funcion se aplicara a las filas o a las columnas. Aplicado a las filas o indices *(axis=0* y aplucado a las columnas *(axis=1)*

[Ver pandas.DataFrame.apply](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.apply.html)

# Cual es la diferencia entre *int32* y *int64* en Python

La diferencia principal esta en terminos de capacidad de almacenamientos, porque un *integer* es manejado en bits (1s y 0s). Un dato numerico de 64-bit integer, puede almacenar un mucho mejor cantidades de numeros mas pequeños y mas grandes en virtud de tenes mas bits.

Tipo de capacidad

|Type| Capacity|
|-|-|
|Int16|(-32,768 to +32,767)|
|Int32|(-2,147,483,648 to +2,147,483,647)|
|Int64|(-9,223,372,036,854,775,808 to +9,223,372,036,854,775,807)|

# Como funciona el metodo *to_numeric*
El metodo pandas.to_numeric( ), convierte un argumento al tipo de dato numerico y por default asigna *int64*. A este cambio, tambien se le conoce como *castear* o *cast* en ingles.

Supongamos que hay un dataframe con la columna llamada *limite_de_velocidad*, la cual almacena valores de velocidad en el tipo de dato string
````
# diccionario velocidades
velocidades = { 'calle':['presidente','main'],'limite_de_velocidad':['80','100']}
````
````
# convertir diccionario a pandas.DataFrame
import pandas as pd
df_velocidades = pd.DataFrame(velocidades)
````
````
# ver tipos de datos del dataframe
df_velocidades.dtypes
````
Output
````
calle                  object
limite_de_velocidad    object
dtype: object
````
````
# convertir de string a numerico reasignando la variable limite_de_velocidad
limite_de_velocidad = pd.to_numeric(df_velocidades['limite_de_velocidad'])
````
ver el cambio de tipo de dato
````
limite_de_velocidad
````
Output
````
0     80
1    100
Name: limite_de_velocidad, dtype: int64
````
Para aplicar el cambio, se puede usar el metodo *assign( )*, el cual permite crear o reasignar columnas. En este caso, se reasignara el tipo de dato.
````
# convertir de string a numerico reasignando la variable limite_de_velocidad aplicando el método assign( )
df_velocidades = df_velocidades.assign(limite_de_velocidad = pd.to_numeric(df_velocidades['limite_de_velocidad']))
````
````
# observar los cambios
df_velocidades.dtypes
````
Output
````
calle                  object
limite_de_velocidad     int64
dtype: object
````

# Como funciona el método **assign( )**
El metodo df.assign(), asigna nuevas columnas a un dataframe o permite castear las columnas ya existentes.

## Crear nueva columna llamada speed_category
Se puede crear una nueva columna a partir de una columma existente. Ver el [proceso *to_numeric*]() 

## Castear una columna existente
Se puede castear una columna existente. Ver el [proceso *to_numeric*]() 


