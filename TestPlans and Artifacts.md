# Test Plans

Es para organizar pruebas manuales asociadas a los Work Items, para mantener un registro del testing.

1) Necesitamos agregar un Test Case aun Work Item (en boards), para luego crear un Test Plan.
  Para ello, vamos a la sección Boards > Boards y clickeamos los tres puntos verticales en una User Story, y seleccionamos "+ Add Test".
2) Dentro de Test Case, podemos añadir tests especificos de ese Work Item, o sino "shared steps" que son etapas comunes a todos los casos de testeo, por ejemplo loggearse antes de realizar cualquier acción.
3) Vamos a Test Plans, que ahora está activado, y registramos los resultados de nuestras pruebas (las pruebas se realizan con otras herramientas, no desde DevOps).

Está asociado mas a pruebas manuales que a pruebas unitarias, o cualquier tipo que ya hay que realizar desde el código. Es una serie de pasos para tener el registro de lo que se hizo en esa User Story.
Tiene herramientas para documentar lo que está ocurriendo.
A partir de lo que no funcione en los Test Plans, podemos crear Work Items del tipo "Bug".

*Las pruebas unitarias están a cargo del desarrollador, muchas veces para que se apruebe una feature, puede llegar a ser obligatorio que cada método o clase venga acompañada de las correspondientes pruebas unitarias para ser aprobado*

Al momento de ejecutar el Build, se corren los test unitarios del proyecto y eso genera un reporte (puede ser tomado como evidencia como el QA, pero no hay mas que eso).

*El Bug es un estado inesperado del sistema*
El work item "Bug" se puede generar desde Test Plans, porque lo encuentre un QA, o también desde un reporte de fallos de un usuario del software.


# Artifacts

Un artifact es el resultado de los procesos que se implementan a un código fuente. Puede ser una amplia gama de resultados, puede ser muchas cosas, binario, libreria, zip, etc.

## Azure Artifacts
Es un repositorio de Artifacts. Puede tener librerías privadas de objetos que utilicen otras personas o de repositorios públicos. La idea es que todo quede almacenado en Azure para nuestro consumo, para no depender de la fuente original de estos objetos o librerías.

Puedo, de crear una librería que quiero que sea privada, almacenarla en Artifacts para que otros proyectos o soluciones puedan consumirlas.

```
  Se consume agregando en el archivo Config la referencia (url) a ese paquete.
```
Ejemplo de Uso:

Hay una empresa cuyos proyectos dependen de diferentes librerías de dominio público.
Para evitar problemas de compatibilidad de actualizarse las mismas, la empresa, en lugar de consumirlas directamente desde la fuente, utiliza una copia de la versión de la librería que funciona con el proyecto, la cual está alojada en Artifacts.
Esta práctica también asegura el funcionamiento de nuestros proyectos en caso de que se caiga la fuente original.
