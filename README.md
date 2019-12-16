# Desafio Final AD

**AUTORES**

Nombre - NIA

Cristian Cabrera Pinto - 100363778
David Gil López - 100363815
David González González - 100363873
Diego Cabeza Gonzalez - 100315003
Hector Herreros Orcajo - 100346112
Javier Corrochano Jiménez - 100363782

Este conjunto de ficheros pertenece a la practica final de la asignatura de Análisis de Datos.

## Manual para comprender todos los ficheros y ejecución.

### Estructura de ficheros

Hemos estructurado todos los ficheros de la siguiente forma:

    - README.md: Fichero actual con la información de funcionamiento de los ficheros de la práctica.

    - Indice_Preprocesado.ipynb: Notebook de Jupyter que funciona como índice hacia el resto de notebooks que contienen el preprocesado de los datos y algunos procesados necesarios para algunos análisis realizados. En estos notebooks queda documentado y justificado todo lo que se hace y suu finalidad.

    - Indice_Analisis.ipynb: Notebook de Jupyter que funciona como índice hacia el resto de notebooks que contienen el análisis de datos extensivo realizado.

    - Analisis: Carpeta con los notebooks de análisis, para acceder a ellos bastaría con hacer uso del índice.

    - Preprocesado: Carpeta con los notebooks de preprocesado, para acceder a ellos bastaría con hacer uso del índice.

    - Dataset: Carpeta en la que se deben localizar los ficheros de datos necesarios para la ejecución del trabajo realizado.
    
    - Imagen: Carpeta que contiene imagenes necesarias para la ejecución. En este caso, las imágenes máscara para hacer wordcloud.
    
**IMPORTANTE**: Dentro de la carpeta de Analisis existe un fichero oculto llamado .mapbox_token, este contiene el token necesario para que los mapas sean generados.
    
### Data sets necesarios

Todos los notebooks entregados ya se encuentran totalmente ejecutados, por lo que no es necesario ejecutarlos para ver su contenido. Sin embargo, si se quieren ejecutar se deben tener en cuenta algunas cosas:

Todos los notebooks van a leer datos de ficheros ubicados en el directorio 'Dataset'. En ella se deben encontrar inicialmente los siguientes ficheros.

    - datos_check.csv
    - datos_consejos.json
    - datos_negocios.csv
    - datos_opiniones.csv
    - datos_usuarios.csv
    
    *Estos ficheros han sido proporcionados a la hora de hacer la práctica.*
    
Hemos utilizado data sets externos, y ya que no son muy pesados los incluimos en la entrega de la práctica:
    
    - crime-data_crime-data_crimestat.csv: Datos de delitos en la ciudad de Phoenix.
    - pop-by-zip-code.csv: Población por código postal de Phoenix.
    
El resto de ficheros de datos necesarios para ejecutar análisis son generados por los ficheros de preprocesado. Los notebooks de preprocesado realizan cambios en los datos y estos se vuelven a guardar con el mismo nombre pero añadiendo '_limpios'.

En algunas ocasiones se necesitan otros datos que no son los obtenidos limpios por el preprocesado. Esto es el caso de los siguientes ficheros **EN CASO DE EJECUCIÓN RECOMENDAMOS EJECUTAR LOS NOTEBOOKS DE LA CARPETA /PREPROCESADO PARA OBTENER TODOS LOS FICHEROS DE DATOS**:

    - datos_negocios_limpios_categoriasExtendidas.csv: Archivo resultante del procesado de categorias extendidas indicado en el indice de preprocesado. Es necesario para ejecutar el analisis de negocios (I).
    
    - Archivos pkl de checks: Se crean en el preprocesado de checks y son necesarios para ejecutar el análisis de checks.
    
    - influencers.csv: Fichero generado en analisis de usuarios (I) y que contiene los usuarios del cluster de influencers. Este fichero se utiliza en analisis de usuarios (II).
    
    - datos_opiniones_sintexto.csv: Fichero generado en Procesado_opiniones_sinTexto. Este fichero nos ha servido para hacer uso de las opiniones sin necesidad de usar el texto, algo que nos ha hecho más ligero el fichero y nos ha permitido cargarlo en memoria.
    
### Librerias necesarias

Además de librerías básicas hemos usado otras para hacer algunos análisis y sería necesario instalarlas para ejecutar el código:

    - TextBlob: Librería para hacer análisis de sentimiento. Se puede instalar haciendo lo siguiente:
        pip3 install -U textblob

    - plotly: Libería para hacer uso de mapas. Instalación:
        pip3 install plotly==4.4.1
        
    - networkx: Libería para hacer grafos:
        pip3 install networkx
        
    - wordcloud: Libería para hacer mapas de palabras.
        pip3 install wordcloud

En principio esto sería todo lo necesario para ejecutar el código, aun así, recomendamos hacerlo solo en caso de extrema necesidad ya que en algunos casos (como el predictor, algunos preprocesados o preprocesados) pueden tardar demasiado tiempo.