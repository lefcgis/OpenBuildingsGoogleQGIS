# <h1> Data Mining with OpenBuilding with Jupyter & QGIS 😃🎁 </h1>

![Builts](https://www.tabulado.net/content/images/size/w1200/2024/09/Open-Buildings.jpg)

El crecimiento urbano global es uno de los mayores desafíos que enfrentan los gobiernos y organizaciones en la actualidad. Según proyecciones de la ONU, 2.500 millones de personas adicionales vivirán en ciudades para 2050, con el aumento concentrado en el hemisferio sur. Este crecimiento demanda herramientas avanzadas para entender cómo evolucionan las ciudades, con el fin de planificar mejor la distribución de servicios esenciales como electricidad y agua. El soporte de bases de datos de huellas de construcciones para consumo por lotes de Google Search nos permite utilizar un conjunto de datos temporales que rastrea cambios en la presencia y altura de edificios desde 2016 hasta 2023. Para este caso acotado, es toda la información referida a Perú (20,472,312 casos), que equivale a 4.97 GB de almacenamiento.



## **Pasos a seguir en Jupyter Notebook** ✨🧮</h1>

## 1. Importar librerías.
import pandas as pd    
import numpy as np     
import geopandas as gpd    

## 2. Abrir el CSV.
df = pd.read_csv(r"D:\ruta\open_buildings_v3_polygons_ne_10m_PER.csv")    
df.head()    

## 3. Desarrollar el dataframe.
df['geometry'] = gpd.GeoSeries.from_wkt(df['geometry'])    
gdf = gpd.GeoDataFrame(df, geometry='geometry')    
gdf.head()    

## 4. Migrar a shapefile (4326).
gdf.to_file(r"D:\ruta\shp\op_b_v3_10_pes.shp")    


## 5. Abrir la capa en QGIS y diseñar la simbología temática.  


    



_#fsociety_


 







