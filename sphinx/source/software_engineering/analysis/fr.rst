Requisitos funcionales
======================

**RF1**: Programar operación
-----------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: OBJ1
- **Requisitos asociados**: 
- **Descripción**: A través de la interfaz administrativa se podrán programar diferentes tipos de operaciones que serán realizadas por los diferentes nodos
- **Precondición**: El administrador deberá estar autenticado en el sistema.
- **Secuencia normal**:

    1. El administrador accede a la interfaz principal del sistema.
    2. Introduce la operación a realizar utilizando los controles de la interfaz.
    3. Selecciona los nodos en los que la operación debe ser realizada
    4. Indica si la operación ha de realizarse de forma inmediata o en un momento futuro.
    5. Añade la operación a la lista de operaciones por realizar.
    6. El sistema contacta con todos los nodos e indica la operación a realizar.
    
- **Poscondición**: Los nodos han recibido la operación y la realizarán en el momento indicado.
- **Excepciones**: En caso de que se dé algún tipo de error en la comunicación entre los diferentes componentes el administrador será informado.
- **Rendimiento**
- **Frecuencia**
- **Importancia**
- **Urgencia**: Alta
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**


**RF2** Ordenar cancelación
---------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: En caso de que sea necesario una operación puede ser cancelada antes de que sea realizada.
- **Precondición**: 

    + El administrador está autenticado en el sistema.
    + Una o más operaciones han sido programadas.

- **Secuencia normal**:

    1. El administrador accede a la interfaz principal y desde ahí consulta las operaciones programadas.
    2. El sistema muestra todas las operaciones programadas para el futuro.
    3. El administrador solicita la cancelación de una de las operaciones a través de la interfaz.
    4. El sistema solicita a todos los nodos a los que se solicitó la realización de esta operación la cancelación de la misma.

- **Poscondición**: La operación es cancelada en todos los nodos en los que se programó.
- **Excepciones**: En caso de que se dé un error en la conexión con los nodos se notificará al administrador.
- **Rendimiento**
- **Frecuencia**
- **Importancia**: Alta
- **Urgencia**: Alta
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**

**RF3** Consulta al registro de operaciones
-------------------------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: Caso base que representa el mecanismo de acceso a la base de datos.
- **Precondición**: El administrador está autenticado en el sistema.
- **Secuencia normal**: 

    1. El administrador accede al sistema y abre la vista deseada.
    2. El sistema consulta los datos asociados a dicha vista.
    3. La base de datos retorna la información.
    
- **Poscondición**: El sistema muestra a través de la interfaz los datos solicitados.
- **Excepciones**: En caso de que se dé un error en la conexión con los nodos se notificará al administrador.
- **Rendimiento**
- **Frecuencia**
- **Importancia**: Baja
- **Urgencia**: Baja
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**
  
**RF4** Consulta de operaciones programadas
-------------------------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: El sistema debe proveer una interfaz de acceso al registro de operaciones programadas para realizarse en el futuro.
- **Precondición**: El administrador está autenticado en el sistema.
- **Secuencia normal**:
  
    1. El usuario accede a la interfaz de visualización de operaciones.
    2. El sistema consulta a la base de datos y muestra los resultados en la interfaz.

- **Poscondición**: Los resultados son mostrados en pantalla.
- **Excepciones**: En caso de que exista algún error de comunicación con la base de datos el administrador es notificado.
- **Rendimiento**
- **Frecuencia**
- **Importancia**: Alta
- **Urgencia**: Alta
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**

**RF5** Consulta de histórico
-----------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: A través de una interfaz, el sistema mostrará operaciones llevadas a cabo con el objetivo de mantener un registro para análisis futuros
- **Precondición**: El administrador debe estar autenticado en el sistema.
- **Secuencia normal**:

    1. El administrador accede a la interfaz de consulta.
    2. El sistema solicita a la base de datos la información.
    3. Se muestran los datos por pantalla

- **Poscondición**:

    + Los datos son mostrados en la interfaz.
    
- **Excepciones**: En caso de un error en la comunicación con la base de datos el administrador es informado.
- **Rendimiento**
- **Frecuencia**
- **Importancia**: Media
- **Urgencia**: Media
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**

**RF6** Descarga del sistema operativo
--------------------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: Los diferentes nodos podrán descargar imágenes del sistema operativo.
- **Precondición**: El nodo debe tener instalado el *software* de instalación y descarga.
- **Secuencia normal**:

    1. El nodo detecta mediante un protocolo de descubrimiento los diferentes nodos presentes en la red que contienen imágenes de sistemas operativos.
    2. Elige un servidor de la lista de resultados y se conecta a este.
    3. Si los dos equipos satisfacen los requisitos de seguridad del otro, comienza la descarga.
- **Poscondición**: La imagen del sistema operativo es descargada en el nodo interesado.
- **Excepciones**:

    + En caso de que no se encuentre ningún nodo, se abortará la operación.
    + En caso de que la conexión sea interrumpida la operación será detenida el nodo intentará reestablecerla. En caso de que no sea posible un registro del fallo será almacenado.
    + En caso de que la conexión no sea factible debido a que una de las partes rechace el certificado ofrecido por la otra, la operación terminará y se almacenará el fallo en el registro.
- **Rendimiento**
- **Frecuencia**
- **Importancia**: Muy alta
- **Urgencia**: Alta
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**

**RF7** Instalación
-------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: Una vez descargado el sistema operativo, el nodo procede a su instalación.
- **Precondición**: La imagen del sistema operativo debe haber sido descargada previamente.
- **Secuencia normal**:

    1. El nodo desempaqueta la imagen del sistema operativo.
    2. Los diferentes ficheros son almacenados en la carpeta adecuada, fijando los permisos adecuados y determinando el propietario de los mismos.
    3. Se almacena toda la información relativa al proceso de instalación en el fichero de registro. 
- **Poscondición**: El sistema operativo queda instalado en el nodo.
- **Excepciones**: En caso de cualquier fallo (escritura, integridad de la imagen...) comienza el caso de uso **RF9**
- **Rendimiento**: 
- **Frecuencia**: 
- **Importancia**: Alta
- **Urgencia**: Alta
- **Estado**: Completo
- **Estabilidad**
- **Comentarios**


**RF8** Actualización
---------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: Caso de uso similar a **RF7**. La única variación es que el nodo no sobreescribe una serie de directorios en el proceso de instalación, en los que se almacenan los datos personales de los usuarios o cualquier otro fichero que deba ser almacenado de forma persistente. 
- **Precondición**: El sistema debe contar con una imagen del sistema operativo descargada (**RF6**).
- **Secuencia normal**:

    1. Se realizan todos los pasos del caso de uso **RF7**, pero no se sobreescribe la información contenida en los diferentes directorios especificados.
- **Poscondición**: El sistema es reemplazado por otra versión del mismo, sin que esto afecte a los datos de los usuarios.
- **Excepciones**: Se consideran las mismas excepciones que el caso de uso **RF7**.
- **Rendimiento**
- **Frecuencia**
- **Importancia**: Alta
- **Urgencia**: Alta
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**

**RF9** Gestionar error en la instalación
-----------------------------------------
 
- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**
- **Precondición**: Se debe dar un error no recuperable de forma autónoma.
- **Secuencia normal**:

    1. Ante un error, el nodo determina el tipo de incidente y almacena la información sobre este en un fichero.
    2. El nodo vuelca todo el histórico de operaciones realizadas en el fichero.
    3. El nodo espera durante un tiempo a que un usuario humano corrija el error manualmente. En caso de que esta interacción no se dé en el periodo especificado, el sistema se reinicia. En caso de que un administrador decida solucionar manualmente el error, se muestra una interfaz administrativa mínima. 
- **Poscondición**: El incidente es registrado y en caso de que un administrador solucione el mismo, el sistema se recupera.
- **Excepciones**
- **Rendimiento**
- **Frecuencia**
- **Importancia**: Media
- **Urgencia**: Media
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**: Es necesario tener en cuenta que este caso de uso se realiza únicamente cuando el nodo no puede resolver el incidente de forma autónoma.


**RF10** Gestionar error en backend
-----------------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: En el caso de que se dé un error durante la realización de una operación a través del *backend*, este caso de uso es iniciado.
- **Precondición**: Se debe detectar un error.
- **Secuencia normal**:

    1. El software detecta un comportamiento anómalo en el transcurso de una operación.
    2. Mediante diferentes mecanismos intenta detectar el tipo de fallo que se ha dado.
    3. Una vez identificado el error, se emite un mensaje de error. En caso de que no sea posible identificar el tipo de fallo, se muestra un mensaje genérico.
- **Poscondición**: El administrador es informado del fallo.
- **Excepciones**:
- **Rendimiento**
- **Frecuencia**
- **Importancia**: Media
- **Urgencia**: Baja
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**

**RF11** Autenticación
----------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: El administrador debe validar su identidad mediante la introducción de unas credenciales de acceso al *backend*.
- **Precondición**: El administrador no ha validado su identidad previamente.
- **Secuencia normal**:
  
    1. El administrador accede al *backend*.
    2. El *backend* detecta que el usuario es desconocido, y muestra una interfaz de autenticación.
    3. El administrador introduce las claves y solicita el acceso son las mismas.
    4. Si las claves son válidas, se da acceso al sistema y se muestra la interfaz principal. En caso contrario se muestra un mensaje informativo y de nuevo se solicita la introducción de datos válidos.
- **Poscondición**: El administrador está autenticado en el sistema.
- **Excepciones**: En caso de un fallo interno, se ejecuta el caso de uso **RF10**.
- **Rendimiento**:
- **Frecuencia**:
- **Importancia**: Alta
- **Urgencia**: Alta
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**

   
**RF12** Creación de imagen del sistema operativo
-------------------------------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: El conjunto de herramientas incluye una utilidad para la creación de imágenes del sistema operativo.
- **Precondición**
- **Secuencia normal**: 
        
    1. El administrador ejecuta el programa de creación de la imagen, indicando la fuente de los datos (un dispositivo de almacenamiento, un directorio local...).
    2. El sistema explora el directorio donde están contenidos todos los ficheros y los empaqueta.
- **Poscondición**: Se cuenta con una imagen del sistema operativo.
- **Excepciones**: En caso de que no se cuente con los permisos suficientes para la creación de la imagen la aplicación notifica al administrador adecuadamente.
- **Rendimiento**
- **Frecuencia**
- **Importancia**
- **Urgencia**: Alta
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**

**RF13** Creación de imagen de instalación o actualización
----------------------------------------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: El administrador podrá empaquetar un conjunto reducido de herramientas que conforman un sistema operativo capaz de llevar a cabo los procesos de instalación o actualización.
- **Precondición**:
- **Secuencia normal**:

    1. El administrador ejecuta la aplicación para crear la imagen del sistema, especificando si es una operación de instalación o actualización.
    2. La aplicación obtiene los diferentes componentes de entre una serie de fuentes (descarga de repositorios de código, de una fuente local...) y los almacena.
    3. Se crea un contenedor con todos los diferentes componentes (*scripts* de instalación, paquetes descargados, archivos de configuración...)
- **Poscondición**: Se ha creado una imagen con las herramientas mínimas para la instalación o actualización del sistema.
- **Excepciones**: 
    
    + En caso de fallos internos la aplicación notifica al administrador.
    + Si el administrador cancela la operación el caso de uso termina y la imagen no es creada.
- **Rendimiento**
- **Frecuencia**
- **Importancia**: Alta
- **Urgencia**: Alta
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**

**RF14** Realizar operación
---------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: A petición del *backend* administrativo, el nodo realiza una operación determinada con una serie de parámetros indicados por el *backend*.
- **Precondición**: El servicio de procesado de peticiones debe estar activo.
- **Secuencia normal**:
    
    1. Al recibir una petición los nodos validan la identidad del servidor. En caso de que dicha validación sea satisfactoria el caso de uso continúa, siendo finalizado en caso contrario.
    2. Al recibir una operación, los nodos comprueban los parámetros y programan la acción a realizar. Se almacena una referencia a la misma en un registro.
    3. Los nodos esperan al momento en el que la operación debe ser realizada. En caso de que sea instantánea, no se realiza espera alguna.
    4. En caso de que sea un reinicio, el sistema programa el reinicio con un tiempo de espera para que los usuarios que están activos en el sistema puedan reaccionar a tiempo. En caso de que sea una actualización, el sistema realizará también un reinicio siguiendo esta política tras la configuración del sistema para su actualización.
    5. El sistema realiza todos los ajustes para la operación de actualización.
- **Poscondición**: La operación es realizada.
- **Excepciones**: En caso de que el servidor no sea considerado de confianza el caso de uso termina.
- **Rendimiento**
- **Frecuencia**
- **Importancia**
- **Urgencia**
- **Estado**
- **Estabilidad**
- **Comentarios**

**RF15** Cancelar operación
---------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: A petición del administrador es posible cancelar operaciones programadas.
- **Precondición**: Caso de uso **RF2**
- **Secuencia normal**:

    1. El nodo recibe una petición del *backend*. En caso de que confíe en este, se continuá.
    2. El mensaje recibido contiene el identificador único de la operación a realizar. El nodo busca la operación utilizando dicho parámetro en el registro.
    3. En caso de encontrar la operación, se elimina la misma del bucle de eventos.
- **Poscondición**: La operación es cancelada.
- **Excepciones**: En caso de que no encuentre la operación en el registro, el caso de uso termina. Es muy improbable que esto suceda, dado que el mensaje es enviado únicamente a los nodos en los que la operación se programó.
- **Rendimiento**
- **Frecuencia**
- **Importancia**: Media
- **Urgencia**: Media
- **Estado**: Completo
- **Estabilidad**: Estable
- **Comentarios**

.. image:: ../img/analysis_cu_marcobootstrap.*
    :align: center

.. 
    - **Versión**: 
    - **Autores**: 
    - **Fuentes**: 
    - **Objetivos asociados**: 
    - **Requisitos asociados**: 
    - **Descripción**
    - **Precondición**
    - **Secuencia normal**
    - **Poscondición**
    - **Excepciones**
    - **Rendimiento**
    - **Frecuencia**
    - **Importancia**
    - **Urgencia**
    - **Estado**
    - **Estabilidad**
    - **Comentarios**