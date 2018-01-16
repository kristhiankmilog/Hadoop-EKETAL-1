# Hadoop-EKETAL

Para la construcción de Hadoop se necesitan tener en cuenta los siguientes archivos para leer:

* En la carpeta SRC se encuentra el archivo BUILDING.txt para toda la parte de requerimientos que necesita para poder compilar el codigo fuente propio de Hadoop.

Además se debe de contar con:

* Un ambiente Unix (Linux, OS X, etc).
* git
* Maven 3.3.9 o más nuevo.
* Oracle JDK 8 o más nuevo.
* Ambiente EKETAL en: https://github.com/unicesi/eketal

Para ejecutar o compilar el codigo fuente junto con EKETAL ingrese las siguientes lineas de comando en la carpeta SRC que viene en el repositorio de Hadoop-EKETAL.

  $mvn clean package -DskipTests
  
luego de esto ya podemos ejecutar a Hadoop y EKETAL juntos.

El ejemplo mas sencillo es el ejecutar la prueba de WordCount.

*Lo primero es subir un archivo txt del cual se quieran contar las palabras concurrentes por medio de los siguientes comandos
  
  $hadoop namenode -format(si no se a iniciado el nodo)
  $start-dfs.sh
  $ $HADOOP_HOME/bin/hadoop fs -mkdir /user/input (para crear la carpeta donde se ha de colocar el archivo)
  $ $HADOOP_HOME/bin/hadoop fs -put /home/file.txt /user/input
  $ $HADOOP_HOME/bin/hadoop fs -ls /user/input (Esto es para observar si esta el archivo en el HDFS de Hadoop)
  $ $HADOOP_HOME/bin/hadoop jar hadoop-examples-*.jar grep input output 
  $ $HADOOP_HOME/bin/hadoop fs -cat /user/output/outfile

