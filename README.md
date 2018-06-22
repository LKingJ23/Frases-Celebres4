# Frases-Celebres4
15/06/2018

Atender a los parámetros para acceder a la BD.
En clase  src/main/java/com/aula114/bean/ServiceFrase.java

Ver en pom.xml, se prevee desplegar en tomee

mvn clean install tomee:run
¿Sabes acceder?  http://localhost:8080/JSFMaven

En este proyecto y tomee plugin, sin detalles precisos de configuración
habrá problemas cuando se seleccione ver frases de autores cuyos nombres
contienen tildes, por ejemplo Napoléon Bonaparte.

--
También en pom.xml se tiene plugin tomcat7
Desplegando con tomcat7 (este plugin resuelve bien charset)

mvn clean install tomcat7:run-war-only

  saber comprobar en pom.xml que el contexto es 'app1', y el puerto 8095
  luego, se accede con http://localhost:8095/app1

--
Vemos en consola las siguientes cinco líneas cuando selecciona
el grupo de frases 'perdonar' y luego al autor 'Jacinto Benavente'

ejecutando EL Contructor .....ViewManager
ejecutando setter ..... propiedad service
ejecutando init method.....
EL Autor seleccionado es: Jacinto Benavente ... ViewManager method
Autor seleccionado: Jacinto Benavente ... implementation method

Tienes que tener bien justificado el por qué de esta secuenciación
de ejecución de métodos.

Deberías saber introducir con código adecuado los 'print', que hacen
posible tal salida en la consola, es decir saber donde ponerlos y su
justificación.
--
