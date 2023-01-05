Carga de archivos y limpieza de datos

El proceso para realizar el EDA en las tablas elegidas fue el siguiente:

-Lectura de archivos con librería Pandas y carga de datos en dataframes.
-Búsqueda de valores nulos y eliminación de las filas que los contenían cuando no representaban suficiente peso para el análisis.
-Búsqueda de valores duplicados.
-Normalización de nombres de las columnas.
-Asignar tipos de datos acorde a lo que expresaban las columnas.
-Eliminación de columnas irrelevantes.

Los nombres de los dataframes elegidos se deben al orden de visualización en la página de Enacom de donde se extrajeron los datos.
Luego, en la descarga de archivos los nombres son más coherentes con lo que contienen.

Análisis por cada tabla

mapa_penetración

-columnas: Año, Trimestre, Provincia, Accesos por cada 100 hogares
-No contenía datos nulos.
-No contenía duplicados.
-Se cambió la coma por el punto en "Accesos por cada 100 hogares" y tipo de dato de object a float.

data_four

-columnas: Unnamed: 0,Unnamed: 1,Unnamed: 2	,Unnamed: 3	,Unnamed: 4	,Unnamed: 5

  Y fueron renombradas como: Año,Trimestre,Provincia,Banda_ancha_fija,Dial_up,Total
-Se encontraron 26 filas con datos nulos y se eliminaron.
-Se cambió el tipo de dato a las columnas "Banda_ancha_fija","Dial_up","Total" para quitar los puntos y tranformar los datos a tipo float.
-Se cambiaron los datos Nan en la columna Dial_up con la media.

data_seven

-columnas: Año,Trimestre,Mbps (Media de bajada),Trimestre.1
  
  Y se renombró una columna: Año,Trimestre,Media_de_bajada,Trimestre.1

-Se cambiaron las comas por puntos en la columna Media_de_bajada y se definió el tipo de dato float.

data_sixteen

-columnas: Provincia,Partido,Localidad,Poblacion,ADSL,CABLEMODEM,DIALUP,FIBRAOPTICA,SATELITAL,WIRELESS,TELEFONIAFIJA,3G,4G,link,Latitud,Longitud
-Se eliminó la columna "link".
-No contenía duplicados.
-No contenía datos nulos.

Los KPIs presentados son : Variación porcentual trimestral de accesos cada 100 hogares.
                           Crecimiento promedio en la velocidad media de bajada por año.
                           Distribución de conexiones por banda ancha y banda angosta por provincia.
                           Cablemodem y fibra optica por provincia.

Con el crecimiento promedio en la velocidad media de bajada por año se puede ver la mejora progresiva en el servicio. Además, esto tiene una correlación
positiva con los ingresos que perciben las empresas proveedoras de internet. A su vez, teniendo un panorama claro de qué provincias tienen mayor acceso a
banda ancha se puede observar aquellas donde la conexión sigue siendo menos eficiente, e invertir en ellas con tecnologías mejores como cablemodem y fibra óptica.