# Participate in the Action - Sistema para el Análisis de Problemas (Pita-SAEP) #
## Diseño Conceptual y requerimientos funcionales (2011) ##

El presente documento es una propuesta preliminar del diseño conceptual y de requerimientos funcionales del sistema SAEP‐PitA. El objetivo es dar al equipo de investigadores del Observatorio del Desarrollo y a estudiantes del curso de ingeniería de software de la Escuela de Computación e Informática (ECCI) mayores detalles sobre los requerimientos funcionales e iniciar posibilidades de integración con otros sistemas como el de la cuenca de Volcán o SIR‐SUR en el Observatorio del Desarrollo de la Universidad de Costa Rica. La presente iniciativa se desarrolla en el marco del proyecto “Mejora de la oferta educativa en gestión ambiental: experiencia interuniversitaria en Pérez Zeledón”, con apoyo del Consejo Nacional de Rectores y las cuatro universidades públicas (UCR‐UNED‐ITCR‐UNA).

Propuesta elaborada por: Álvaro Fernández y Carlos
Andrés Méndez Rodríguez, Observatorio del Desarrollo, UNIVERSIDAD DE COSTA RICA

# Sistema para el Análisis Espacial de Problemas (SAEP) #

## Introducción ##

Esta propuesta para el software SAEP‐PitA busca desarrollar un sistema web de información geográfica con un conjunto de herramientas de propósito general que permitan simular, experimentar, medir, administrar y analizar problemas contextualmente situados geográficamente.

Se prevé que el sistema pueda integrar datos tanto digitados, leídos de archivos o bases de datos, como suministrados por componentes de mediación externos de conexión a puerto. Específicamente se propone el diseño e implementación de acumuladores de datos provenientes de dispositivos de censado de variables medio ambientales, como temperatura, humedad relativa, pluviosidad, luminosidad solar y otras, lo que le permitirán al usuario vincular el modelo virtual de representación de su comunidad, con variables ambientales reales y de esta forma ajustar su estudio, análisis, y simulaciones a su realidad cotidiana.

El diseño del SAEP‐PitA se asienta en la Internet y por lo tanto posee las facilidades de comunicación que brinda esta red. Podrá funcionar tanto auto-contenido localmente en un computador, como en diálogo dinámico entre usuarios o comunidades de usuarios.

En el 2010 e inicios de 2011 se diseñó una primera versión del sobre la base de la plataforma del Sistema de Información Regional de la Zona Económica Especial (SIR-ZEE). Actualmente, la implementación del software ha alcanzado un 80%. En el segundo semestre de 2011, se adaptará a la plataforma del Observatorio del Desarrollo de la UCR con vistas a su posible utilización en colaboración con el SIR-SUR.


## REQUERIMIENTOS FUNCIONALES ##

  * Visualización en MapServer y pmapper. (Requerimiento de software)

  * Colocar las siguientes capas de información geográfica, que pueda seleccionar el usuario: poblados, escuelas, ríos y cuerpos de agua, tipo y uso de suelos, fauna, flora, clima, situación socioeconómica, etc (ver el Atlas Digital del ITCR).

  * Además, tener dos capas adicionales:

  1. Organizaciones de monitoreo: En el mapa deben visualizarse con un icono que permita al usuario tener mayores detalles como: Nombre, descripción, ubicación, imágenes, enlaces, entre otros.
  1. Estaciones de monitoreo: En el mapa deben visualizarse con un icono que permita al usuario tener mayores detalles como descripción, ubicación, organización, entre otros atributos, un enlace y una imagen.



  * Las organizaciones de monitoreo y las estaciones de monitoreo deben ser clasificadas:

  1. Unas categorías definidas por el proyecto:
  1. Otros cualesquiera por el usuario final.
  1. Los usuarios autorizados para administrar las categorías son: Sólo los profesores.



  * Consulta y análisis de información por categorías (requiere de la construcción de la consulta en el sistema). Ejemplos:

  1. Escuelas en riesgo de inundación por unidad administrativa (distrito, cantón)
  1. Erosión por cultivo según pendiente y tipo de suelo por unidad administrativa (distrito, cantón)
  1. Uso del suelo distinto a bosque dentro del área de protección en riberas (10 o 50 metros) por unidad administrativa (distrito, cantón)
  1. ¿A qué distancias de los ríos se encuentra cada uno de los hospitales?
  1. Para construir el comedor estudiantil para el distrito escolar SD2 se requiere conocer las coordinadas del punto central entre las escuelas.

**Interfaz de ejemplo “constructor de consultas”:**

![http://www.candres.com/archivo/consultas.jpg](http://www.candres.com/archivo/consultas.jpg)

  * SIMULACION Función de articulación entre categorías de datos mediante algoritmos introducidos por el usuario, que permita plantear simulaciones de "qué pasa si".
    1. Vinculando por ejemplo la categoría "uso de suelo" con "turbidez del agua" mediante un algoritmo que diga: si duplico (o aumento en cualquier porcentaje) en tal finca la cantidad de bosque, se reduce a la mitad (o en cualquier otro porcentaje) la turbidez de la quebrada que pasa por el límite de esta propiedad.
    1. El PitA-SAEP deberá ser flexible para que este tipo de reglas puedan agregarse en cualquier momento.
    1. Esta funcionalidad debería permitir una complejización ulterior mediante introducción de otras variables correlacionadas: por ejemplo, distancia de la finca a la quebrada, pendiente, tipo de suelo, de tal forma que estos factores puedan incluirse en nuevos algoritmos igualmente definidos por el usuario.
    1. Es necesario que las capas de información georreferenciada permitan hacer cálculos de área que puedan igualmente articularse en estos algoritmos multifactoriales.
    1. Actores sociales: La posibilidad de crear reglas por parte del usuario debe supeditarse a su previa caracterización en términos de pertenecer a un grupo de actores sociales cuyos atributos permitan la creación y ejercicio de las reglas de que se trate: por ejemplo, para aumentar el bosque en una propiedad, el usuario debe tener la autoridad correspondiente a los atributos de propietario o agente estatal (del Ministerio de Ambiente en este caso, o como oficial de ambiente en la municipalidad).

**INTERFAZ DE EJEMPLO PARA LA VENTANA PRINCIPAL**

![http://www.candres.com/archivo/ejem.png](http://www.candres.com/archivo/ejem.png)

**LINKS EXTERNOS**

El siguiente es el link de la página principal del proyecto

http://www.moe-gaur.odd.ucr.ac.cr aunque por el momento el que funciona es:

http://mgau.odd.ucr.ac.cr

SAEP-PitA bajo la plataforma SIRZEE (San Carlos)

http://www.sirzee.itcr.ac.cr/modules/GIS/maep/htdocs/map_default.phtml

Atlas Digital 2008 en:

http://usuariosigcr.hostei.com/index.php?option=com_content&view=frontpage&Itemid=7


Manual de php

http://www.php.net/manual/en/

http://www.php.net/manual/es/

Componentes a utilizar en el proyecto

http://mapserver.org/

http://www.pmapper.net/index.shtml

http://postgis.refractions.net/

Tecnologías a valorar

http://geoserver.org/display/GEOS/Welcome

## REQUERIMIENTOS NO FUNCIONALES ##

Algunos requerimientos no funcionales que se han identificado son:

### Integridad: ###

Cada componente y funcionalidad debe tener consistencia en el sistema en general, en otras palabras, cada elemento del sistema debe cumplir con un propósito acorde con la visión del cliente o la arquitectura.

### Integración: ###

Eventual integración o interoperabilidad con el proyecto volcán del OdD.

### Usabilidad: ###

Utilizar almenos objetos gráficos como botones, paneles, combo box, iconos, imágenes, barras de desplazamiento, scroll up/down, campos para texto y menu de opciones. Además el sistema contará con Logo, mapa del sitio, contacto, guía al usuario (ayuda), enlaces reconocibles, entre otros.

### Seguridad: ###

1.Sólo los usuarios registrados y autenticados podrán crear, editar o eliminar (según corresponda) documentos. Usuarios no autenticados podrán hacer sólo lectura.

2.El sistema debe contar con un administrador de cuentas para modificar privilegios o eliminar usuarios.

### Disponibilidad: ###

El sistema debe estar disponible las 24 horas con 365 días por lo menos en un 97%. Se entenderá por disponibilidad que el sistema cumpla con los requerimientos funcionales y no funcionales. Por ejemplo si un servicio está durando más del tiempo establecido se tomará como no disponible.

### Desempeño: ###

Ningún servicio como la autenticación, el despliegue del mapa, entre otros no debe sobrepasar los 20 segundos.

### Hardware: ###

1.El software debe visualizarse de manera coherente con un monitor de resolución 1024 x 768 o más alta.

2.Los requerimientos de desempeño anteriores se cumplirán con máquinas de 1.5 Hrz y 250 MB RAM o más.

### Software: ###

1. Programado con php, postGIS, mapserver y p.mapper.

2. El sistema estará disponible en Firefox, Internet Explorer y Google Crome.

### Modificabilidad: ###

El sistema no debe ser difícil de mantener o configurar en el futuro. En la medida posible deberá ofrecer archivos de configuración, documentación interna del código y manuales de consulta para el administrador del sistema.

### Testing del software ###

El desarrollo del software debe contar con un servidor de pruebas ya que no es posible hacer uso del servidor del OdD para eso. El software se implantará en el servidor del OdD después de que se ha probado su funcionalidad correcta y simulando el ambiente del servidor del OdD.