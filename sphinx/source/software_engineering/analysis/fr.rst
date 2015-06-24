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
- **Descripción**: El sistema debe proveer una interfaz de acceso al registro de operaciones.
- **Precondición**: 
- **Secuencia normal**: 
- **Poscondición**
- **Excepciones**
- **Rendimiento**
- **Frecuencia**
- **Importancia**
- **Urgencia**
- **Estado**
- **Estabilidad**
- **Comentarios**
  
**RF4** Consulta de operaciones programadas
-------------------------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: 
- **Precondición**
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
- **Descripción**: A través de una interfaz, el sistema mostrará operaciones ya llevadas a cabo con el objetivo de mantener un registro para análisis futuros
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
- **Importancia**
- **Urgencia**
- **Estado**
- **Estabilidad**
- **Comentarios**

**RF6** Descarga del sistema operativo
--------------------------------------

- **Versión**: 
- **Autores**: 
- **Fuentes**: 
- **Objetivos asociados**: 
- **Requisitos asociados**: 
- **Descripción**: Los diferentes nodos podrán descargar imágenes del sistema operativo
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

**RF7** Instalación
-------------------


**RF8** Actualización
---------------------

**RF9** Gestionar error en la instalación
-----------------------------------------

**RF10** Gestionar error en backend
-----------------------------------

**RF11** Autenticación
----------------------

    7. Los nodos esperan al momento en el que la operación debe ser realizada. En caso de que sea instantánea, no se realiza espera alguna.
    8. En caso de que sea un reinicio, el sistema programa el reinicio con un tiempo de espera para que los usuarios que están activos en el sistema puedan reaccionar a tiempo. En caso de que sea una actualización, el sistema realizará también un reinicio siguiendo esta política tras la configuración del sistema para su actualización.
    9. El sistema realiza todos los ajustes para la operación de actualización.

**RF12** Creación de imagen

**RF13** Creación de imagen de actualización

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