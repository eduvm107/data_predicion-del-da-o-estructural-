# Datos corregidos (balanceados) - Open Buildings Lima+Callao

Datos descargados para corregir el desbalanceo de distritos en el proyecto
de predicción de daño estructural (Grupo 06, Big Data Analytics ESAN).

## Contenido

- `open_buildings/lima_callao_full_buildings.csv.gz` — huellas de edificios
  de Lima+Callao (3,200,050 edificios), recortadas desde el GeoParquet
  completo de Perú (Open Buildings v3) vía Source Cooperative
  (`https://data.source.coop/cholmes/google-open-buildings/geoparquet-by-country/country_iso=PE/PE.parquet`).

- `open_buildings_25d/` — 286 tiles GeoTIFF (5x5km, 4m de resolución) de
  altura de edificios, descargados de Google Earth Engine
  (`GOOGLE/Research/open-buildings-temporal/v1`, imagen
  `91_EPSG_32718_2023_06_30`), cubriendo todo el bbox de Lima+Callao.

Estos datos reemplazan una versión anterior truncada (de un dataset de
Kaggle) que solo cubría 168,693 edificios en un cuadrado de 25x25km del
sur-centro de Lima, sesgando el ranking de riesgo hacia los distritos
ricos del sur. Con estos datos completos, el pipeline cubre 48/50 distritos
de Lima+Callao.
