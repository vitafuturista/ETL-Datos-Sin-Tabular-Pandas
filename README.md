Este programa importa, procesa y concatena52 tablas de datos semanales con formato no tabular, para transformarlas en un formato estructurado que puede ser utilizado para análisis. El procesamiento incluye la adición de nuevas columnas, renombrado de columnas específicas y la organización de los datos por semana y fecha. Finalmente, las tablas procesadas se concatenan y se exportan para su posterior uso.

Descripción del Proyecto
El proyecto importa 52 tablas de datos, que no tienen un formato tabular consistente. A continuación, se realiza el siguiente procesamiento en cada DataFrame:
- Renombrado de columnas específicas: Algunas columnas tienen nombres no descriptivos, como Unnamed: 1, que son renombradas para mayor claridad.
- Adición de la columna "region": Se agrega una columna "region" que clasifica los datos en tres categorías: nacional, internacional y global, dependiendo de la fila.
- Eliminación de filas innecesarias: Se eliminan ciertas filas de los DataFrames para limpiar los datos.
- Creación de nuevas columnas: Se generan nuevas columnas con la semana y la fecha, que se extraen de los nombres de los archivos de las tablas.
- Al finalizar el procesamiento, todas las tablas se concatenan en un único DataFrame y se exportan a un archivo para su uso posterior.
  
Estructura del Código
- Importación de Tablas: Las tablas son importadas con un formato no tabular y se renombrarán para tener nombres de columnas más representativos.
- Renombrado de Columnas: Se utiliza un diccionario para renombrar las columnas de cada DataFrame. Las columnas como Unnamed: 1, Unnamed: 4, Unnamed: 6, etc., se cambian a nombres más descriptivos como product, ly_applicants, ly_admitted, ly_registered, entre otros.
- Añadir la Columna "Region": Una nueva columna llamada region es añadida a cada DataFrame con valores como nacional, internacional y global, dependiendo de la fila.
- Crear Columnas de "Semana" y "Fecha": Extraemos la información de la semana y la fecha a partir del nombre de los archivos y los asignamos como nuevas columnas a cada DataFrame.
- Concatenación y Exportación: Todos los DataFrames procesados son concatenados en uno solo, y luego exportados a un archivo CSV para su análisis.
