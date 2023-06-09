# Cómo manipular y analizar datos en Pandas 

## Qué es Pandas

Es una librería de Python 🐍 que permite manipular dos tipos de estructuras de datos: listas y tablas.

- [ ] Las listas o arrays o estructuras de 1 dimensión, pueden ser manipuladas por las **Series**
- [ ] Las tablas o estructuras de dos dimensiones pueden ser manipulados por el **DataFrame**

![ima](https://pandas.pydata.org/pandas-docs/stable/_images/01_table_dataframe.svg)

## Series & DataFrame

- [**Series**](https://pandas.pydata.org/pandas-docs/stable/user_guide/dsintro.html#series): is a one-dimensional labeled array capable of holding any data type (integers, strings, floating point numbers, Python objects, etc.). The axis labels are collectively referred to as the index. The basic method to create a Series is to call:
  ```
  s = pd.Series(data, index=index)
  ```
  

    Here, data can be many different things:

    - a Python dict

    - an ndarray

    - a scalar value (like 5)



- [**DataFrame**](https://pandas.pydata.org/pandas-docs/stable/user_guide/dsintro.html#dataframe): is a 2-dimensional labeled data structure with columns of potentially different types. You can think of it like a spreadsheet or SQL table, or a dict of Series objects. It is generally the most commonly used pandas object. Like Series, DataFrame accepts many different kinds of input:

  - Dict of 1D ndarrays, lists, dicts, or Series

  - 2-D numpy.ndarray

  - Structured or record ndarray

  - A Series

  - Another DataFrame


- [ ] [Como crear e indexar series]()
- [ ] [Como crear dataframes]()
- [ ] [Como manejar e indexar archivos: csv, excel, JSON]()
- [ ] [Como conectarse a bases de datos sql]()

## Funcionalidades básicas y esenciales de Pandas

- [ ] [Formatos de lectura para cargar y guardar]()
- [ ] [Tipos de variables que componen un dataframe]()
- [ ] [Estructuras de dataframe en detalle]()
- [ ] [Como borrar filas, columnas y copiar información]()
- [ ] [Cómo aplicar funciones def y lambdas en un dataframe]()
- [ ] [Cómo usar los comandos: *concat* y *append*]()
- [ ] [Cómo usar la funcón *groupby*]()
- [ ] [Cómo manejar valores nulos: NaN]()


## Practicas para no olvidar

### Como eliminar registros duplicados

* Para resolver esta premisa, usé la funciòn ```drop_duplicates()```
* Hay una variante, la cual se puede usar para extraer los registros contrarios ```drop_duplicates(keep=False)```. La siguiente fuente permite usar mas opciones: [drop_duplicates](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.drop_duplicates.html)
* La sintaxis correcta es: ```dataframe.drop_duplicates()```

