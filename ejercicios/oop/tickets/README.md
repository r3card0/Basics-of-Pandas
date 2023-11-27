#

# Languagues and libraries
````
Python 3.10.6
````
libraries
````
pandas
psycopg2
````

# Object Oriented Programming
Un objeto es una cosa tangible del mundo real, como puede ser una persona, una taza, un carro, etc. Y también puede ser cosas no tangibles, como una cuenta de banco o un ticket que en cualquier sistema de manejo de tickets:pe. Jira.

Como en el mundo real, en programacion, los objetos tienen identidad, atributos y acciones (behaviors).

Una persona (objeto), se identifica con su nombre y tiene atributos, como la edad, altura, género, nacionalidad, etc. Y la persona puede hacer varias acciones, como correr, saltar, dormir, comer, etc.

Un ticket (objeto), se identifica por su id, su descripcion, nombre del proyecto, requester (solicitante), epic, etc y sus atributos se pueden definir por id,  título del ticket, región de los datos a manejar, etc. Las acciones son, crear un reporte de datos en un formato deseado. Crear un dashboard para análisis, crear un shapefile para visualizar datos en un mapa

# Class
una class es un codigo que permite crear objetos. Es un template que permite crear objetos con identidad, atributos y acciones.

El uso de OOP en la resolucion de tickets, es para crear entregables como reportes, dashboards y formatos de datos espaciales para mapas digitales. 

Esto es, con la idea de facilitar el proceso de creación de los entregables, ahorrar tiempo y entender mucho mejor el paradigma de OOP. 

En muchas ocasiones, han solicitado un reporte con columnas específicas para una región y posteriormente, el mismo requester o uno diferente, solicita un reporte igual o similar pero de otra región o fuente. Cuando existe este caso, el uso de OOP es muy util porque solo se tiene que cambiar el la fuen (rbs), correr el proceso y esperar el entregable, reduciendo así el tiempo de resolución. 

Se han creado varias clases con la finalidad de crear un proceso ETL, donde se establezca conexion con la base de datos para la extracción (*extract*) de datos, seguido de la creación del formato y estructura del archivo (*transform*), dónde se entregarán los datos al requestes. En este proceso, la fase LOAD o carga, la puede hacer o no el requester, ya que el recibe los datos y dispone de ellos para análisis o carga a sus herramientas.
