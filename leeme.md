Presentaré este archivo en forma de bitacora con el procedimiento de desarrollo utilizado

Para cumplir el desafio opte por desarrollo local, teniendo en cuenta el tiempo que podría destinar, con esto busco generar un producto utilizable que luego mejorar si es posible
Utilizaré windows
Lo primero es la revisión de los datos que se utilizaran como entrada
Luego modelar la base de datos teniendo en mente lo visto en los datos y la salida requerida anunciada en el desafio
    * El primer modelo es muy simple con solo lo necesario para la lectura de los datos, manipulación de ellos y su carga
    * Si el tiempo alcanza propondré un modelo más completo con lo que puediese ser utilizado en esta nueva área de lider.cl para videojuegos
    * El modelo lo cree directamente con sintaxis sql en mysql y lo ejecuto para generar la db
    * la fecha del archivo result la dejaré sin formato fecha, pues no se utilizará como tal

Escogí python como lenguaje para el código, esto debido a que nunca lo había utilizado y aprovecharé para aprender
    * comienzo con ver ejemplos del lenguaje y las funciones mas básicas

Estructuro algunas clases pensando en en orientación a objetos:
    * una clase de conexión para acceder a la base de datos y ejecutar las queries
    * una clase para trabajar los csv
    * una clase main para invocar los metodos

Cada una de las acciones que describa y las elecciones tomadas fue previamente investigado en distintas fuentes

Escribo codigo para las conexiones a la base de datos y los pruebo

Escribo código para lectura de los csv (primero desde archivos locales y luego lo modifico para hacerlo desde github), probé arreglos y la estructura panda, me quedo con esta última que es bastante versatil
Antes de guardar lo capturado del csv decido limpiar los requistros cuyas tuplas no estan completas en sus valores, en este caso para el campo userscore
    * podría haber calculado promedios del mismo juego en otras consolas, pero decidí que lo mas simple era eliminarlo
Genero las consultar para el registro en mysql workbench y una vez listas las llevo al código
    * las pruebo ejecutando el código y viendo por terminal si escribe los datos correctos en la estructura
    * finalmente guardo lo que contienen las estructuras en la base de datos

Escribo código para generar resultados solicitados
    * escribo varios alternativas de consula para generar resultados
    * escojo consulta que entrega los 10 (primeros y ultimos puestos) incluyendo todos aquellos juegos que comparten la misma calificación (metascore), dejo las otras consultas en archivo pruebas_db.sql en caso de que quieran ser probadas o utilizadas
    * lo mismo que en caso de lectura, pruebo las consultas primero directo en workbench y luego integradas al código viendo si las estructuras contienen los datos correctos
    * finalmente genero los archivos en una carpeta local

Lamentablemente borre todo el codigo de prueba que fuí generando cuando daba con lo definitivo esperado, recordé que es una buena practica mantenerlo cuando estaba generando la escritura de los resultados, así que éste lo mantuve en el archivo Pruebas.py

Para finalizar el código agregue validaciones o restricciones

Mejoras visualisadas:
    - separar las consultas sql que se presentan como string en una clase
    - investigar sobre alternativas de estructuras y funciones para optimizar código en tiempos de carga y utilización de memoria
    - implementar el código utilizando paralelismo

Al subir el proyecto a github a travez de visual studio code se generó el branch master, lo que me impide hacer merge con el main, por lo que solicito la revisión sobre master

Herramientas utilizadas:
mysql workbench
visual studio code
power designer

pip install urllib
pip install PyMySQL
pip install SQLAlchemy