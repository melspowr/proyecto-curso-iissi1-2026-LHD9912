# Título Proyecto.

## Miembros del grupo LX-XXX-X (sustituir)

1. Alberto Ortega, Iván
1. Andújar Cruz, Juan Carlos
1. Baselga Molina, Álvaro María
1. Casero Calvo, Iván

## 1. Introducción al problema

Ante la privatización de recursos académicos como apuntes, esquemas, y otros documentos y debido a los abusivos precios o anuncios constantes, se busca crear una red de apuntes abiertos a todos los usuarios, con una mejor organización y reducción de anuncios, con el objetivo de tener una gran base de usuarios implementando un sistema donde crear tus propios lienzos y compartirlos con otros usuarios lectores o editores según conveniencia.

El proyecto está principalmente orientado hacia los estudiantes, sin embargo se podría usar en entornos laborales, por lo que se permite la posibilidad de privatizar los lienzos y otorgar un espacio de trabajo más confidencial.

## 2. Glosario de términos

- Copyleft: naturaleza de las licencias que dan libertad al usuario. Estas licencias deben de coincidir con la definición de la asociación GNU: [https://www.gnu.org/philosophy/free-sw.html](https://www.gnu.org/philosophy/free-sw.html)

- Servicio: el conjunto que ofrecemos, este incluye pero no se limita a: la página web, la aplicación y la base de datos.

- Objetos: estos contenidos introducidos por los usuarios en un lienzo, esto incluye pero no se limita a: los trazos, imágenes, videos y documentos,

- Lienzo: sección del servicio en el que se añaden los objetos.

- Bifurcación: copia de un lienzo existente por parte de un usuario. Esta copia deberá de respetar las condiciones impuestas por la licencia del creador original.

## 3. Visión general del sistema

### 3.1. Requisitos generales

- Gestionar carpetas: Como usuario de la aplicación quiero poder organizar mis lienzos mediante carpetas para obtener un mayor orden.

- Permisos de edición: Como propietario de un lienzo, quiero ser capaz de añadir editores a mis documentos para que contribuyan a ellos de forma colaborativa.

- Categorización de lienzos: Como propietario de un lienzo, quiero poder asignar categorías existentes o crear las mías propias para facilitar su posterior búsqueda.

- División de un lienzo: Como editor de un lienzo quiero que los lienzos estén divididos en capas, con 1 capa por editor para evitar mezclar información entre editores

- Herramientas de entrada: Como editor de un lienzo, quiero tener la opción de escribir tanto mediante trazos (pantalla táctil) como con teclado, para adaptarme a mi dispositivo.

- Importación de multimedia: Como editor de un lienzo, quiero poder importar mis propias imágenes para enriquecer los apuntes y diferenciarlos.

- Búsqueda: Como usuario de la aplicación, quiero poder buscar lienzos por nombre y categoría para encontrar rápidamente la información que necesito.

- Valoraciones: Como usuario, quiero poder ver las valoraciones y comentarios de otros usuarios en los lienzos públicos para identificar los de mayor calidad.

- Comentarios: Como usuario, quiero poder dejar comentarios en los apuntes de otros para sugerir cambios o correcciones.

- Bifurcación: Como usuario, quiero poder crear copias de apuntes públicos existentes para editarlos a mi gusto sin alterar el original.

### 3.2. Usuarios del sistema
- Usuario registrado:  Personas que tienen acceso a la plataforma para crear sus propias carpetas, buscar lienzos públicos, editar su perfil y hacer forks de apuntes públicos de la comunidad.

- Propietario / Administrador:  Es el creador original de un documento. Tiene el control total sobre ese lienzo, puede cambiar su privacidad (público/privado), eliminarlo, gestionar las categorías y asignar roles a otros usuarios como el de escritor (y el de lector en caso de que sea un lienzo privado).

- Escritor / Editor:  Usuario perteneciente a un lienzo con permisos de modificación. Pueden añadir contenido (texto, trazos, imágenes) trabajando exclusivamente en su propia capa independiente. Además, tiene acceso al chat interno del lienzo para coordinarse con el propietario y otros editores.

- Lector: Usuario que accede a un lienzo (público o mediante invitación) en modo de solo lectura. No puede cambiar el contenido del apunte ni participar en el chat de escritores, pero puede interactuar dejando comentarios y valorando el documento.

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

##### R.F.01. Información general de chats
Como participante de un chat quiero consultar en los chats los participantes de este y el historial de mensajes con sus respectivas fechas y horas.

**Prueba de aceptación**

- Comprobar que el usuario puede visualizar la lista completa de los participantes del chat.
- Verificar que el historial de mensajes se muestra correctamente junto con la fecha y hora exacta de cada envío.

##### R.F.02. Administración de lienzos
Como administrador de un lienzo quiero poder consultar las carpetas donde están guardadas, las diferentes categorías atribuidas a mi lienzo y el tipo de usuario que accede a mi lienzo.
	
**Prueba de aceptación**

- Comprobar que el administrador del lienzo puede ver la carpeta donde está ubicado el documento.
- Verificar que se muestran en pantalla las distintas categorías atribuidas al lienzo.
- Comprobar que se lista correctamente el tipo de usuario (roles) que tiene acceso al lienzo.
- Se debe aplicar la regla de negocio R.N.01.

##### R.F.03. Datos personales
Como usuario quiero poder consultar mis datos personales cuando lo necesite.

**Prueba de aceptación**

- Comprobar que el usuario puede acceder a la sección de consulta de sus datos.
- Verificar que la información mostrada corresponde fielmente a los datos personales registrados por el usuario.

##### R.F.04. Rango en el lienzo
Como usuario quiero poder consultar quien es el propietario del lienzo y que permisos tengo.

**Prueba de aceptación**

- Comprobar que el usuario puede visualizar de forma clara quién es el propietario del lienzo.
- Verificar que el sistema muestra los permisos específicos que el usuario activo tiene sobre ese lienzo.
- Se debe aplicar la regla de negocio R.N.01.
- Se debe aplicar la regla de negocio R.N.02.

##### R.F.05. Comprensión lienzo
Como usuario me gustaría poder ver la descripción del lienzo y la categoría para comprender mejor el tema que abarca.

**Prueba de aceptación**

- Comprobar que la descripción detallada del lienzo es visible para el usuario.
- Verificar que se muestra la categoría a la que pertenece el documento.

##### R.F.06.  Comparador comentarios
Como lector de lienzos quiero poder ver mis comentarios y los de otros usuarios y ordenarlos por fecha.

**Prueba de aceptación**

- Comprobar que el usuario puede visualizar sus propios comentarios en el lienzo.
- Verificar que el sistema filtra y muestra los comentarios de otros usuarios que tengan una diferencia de publicación menor a una semana.

##### R.F.07. Relación comentarios-lienzo
Como administrador, quiero ver la categoría de un lienzo junto a sus comentarios para moderar su contenido.

**Prueba de aceptación**

- Comprobar que el administrador puede visualizar la categoría a la que pertenece el lienzo.
- Verificar que los comentarios de los lectores son visibles junto a esta información para permitir al administrador comprobar su relación con el contexto.

##### R.F.08. Administración del chat
Como administrador del chat, quiero ver la clase de usuario del que haya escrito un mensaje.

**Prueba de aceptación**

- Comprobar que el administrador del chat puede visualizar todos los mensajes enviados.
- Verificar que junto a cada mensaje se indica claramente la clase o rol del usuario que lo ha escrito.

##### R.F.09. Gestión carpetas personales
Como usuario quiero ver cuántas carpetas tengo y cuál fue la primera de todas ellas.

**Prueba de aceptación**

- Comprobar que el sistema muestra al usuario el recuento total de sus carpetas.
- Verificar que se identifica y resalta cuál de todas las carpetas fue la primera en ser creada.

##### R.F.10. Valoración temporal de los lienzos
Como administrador, quiero ver las fechas de los comentarios de un mismo usuario y ver un histórico de sus valoraciones.

**Prueba de aceptación**

- Comprobar que el administrador puede ver los comentarios agrupados o filtrados por un mismo usuario.
- Verificar que se muestran las fechas exactas de cada comentario para evaluar la progresión temporal.

#### 4.1.1. Requisitos de información

##### R.I.01. Lienzo
Como desarrollador de la aplicación necesito tener la siguiente información sobre los lienzos para una mayor organización:
- Propietario.
- Fecha de creación.
- Registro de cambios.
- Categorías.
- Valoración global//Compuesto.
- Descripción.

**Prueba de aceptación**
- No se puede dejar en blanco la categoría.
- El propietario da permisos de administrador a otra persona y da error.
- Cada nueva modificación se almacena automáticamente en el registro de cambios.

##### R.I.02. Mensaje 
Como usuario quiero tener la siguiente información sobre los mensajes para mantener el control sobre los chats:
- Contenido.
- Tamaño.
- Autoría.
- Fecha y hora del envío.

**Prueba de aceptación**
- Se escribe un contenido con una cantidad de caracteres mayor del tamaño permitido y da error.
- No se permite que la autoría cambie en ningún momento.

##### R.I.03. Usuario
Como desarrollador quiero escribir la siguiente información sobre los usuarios para poder mantenerlos todos identificados:
- Nombre del usuario.
- Correo del usuario.
- Contraseña.

**Prueba de aceptación**
- Se intenta crear una cuenta con un correo ya registrado y da error.
- El nombre y el correo deben ser únicos.
- Se debe escribir la contraseña correctamente o no iniciará sesión.
  
##### R.I.04. Carpeta
Como desarrollador quiero poder acceder a la siguiente información sobre mis carpetas para tener mis archivos más ordenados:
- Nombre de la carpeta.
- Fecha de creación.
- Descripción.
- El conjunto de lienzos que contiene.

**Prueba de aceptación**
- Se intenta crear una carpeta sin lienzos y da error.
- La carpeta debe contener nombre para crearla.

##### R.I.05. Comentario
Como desarrollador quiero incluir la siguiente información sobre los comentarios para saber la opinión de las personas:
- Contenido.
- Emisor.
- Fecha de los comentarios.

**Prueba de aceptación**
- Un comentario debe mantenerse aunque el emisor se haya borrado.
- Intento mandar un mensaje y falla si no contiene nada.

##### R.I.06. Rol
Como desarrollador quiero saber lo siguiente sobre los roles para administrar lo que pueda hacer cada usuario:
- Tipo del rol (Administrador,escritor,lector).
- Permisos.

**Prueba de aceptación**
- El rol da error si no tiene permisos asignados.
- No se le pueden asignar exactamente los mismos permisos a dos roles distintos.

##### R.I.07. Chats
Como desarrollador quiero acceder a la siguiente información sobre los chats para ser consciente de cómo está compuesto el chat:
- Descripción.
- Número integrantes.
- Fecha de creación.

**Prueba de aceptación**
- Un chat debe contener por lo menos 2 integrantes.
- Comprobar si la fecha de creación es posterior a la del lienzo.

##### R.I.08. Categoría
Como desarrollador quiero saber la siguiente información sobre la categoría para saber cómo catalogar mi lienzo:
- Nombre.
- Tamaño.

**Prueba de aceptación**
- La categoría se deja en blanco y da error ya que el tamaño es cero.
- En el nombre se introducen caracteres que no son aceptados y los sustituye con una interrogación.

##### R.I.09. Capa
Como desarrollador quiero saber las siguientes propiedades de las capas para saber quién está aportando al lienzo:
- Número de capa.
- Fecha y hora de creación.
		
**Prueba de aceptación**
- Me da error al intentar eliminar la capa base.
- Una capa anterior no puede estar creada después de una posterior.


#### 4.1.2. Reglas de negocio

##### R.N.01. Control de escritura sobre el lienzo

El sistema debe validar que la acción de escritura esté bloqueada para todos aquellos usuarios que no cuenten con el rol de escritor en ese lienzo.

##### R.N.02. Categorización obligatoria de los lienzos públicos

Para garantizar que la plataforma de apuntes mantenga un orden óptimo en las búsquedas, todo lienzo público debe estar vinculado obligatoriamente a al menos una categoría. El sistema impedirá publicar un lienzo si no se le ha asignado una categoría válida.

##### R.N.03. Control sobre las autovaloraciones

El sistema no permitirá que el usuario creador (Propietario/Administrador) de un lienzo publique comentarios con valoración en su propio documento. Esto se hace para evitar que el autor infle artificialmente la nota de sus apuntes.

##### R.N.04. Eliminación de lienzos:

Por la sanidad del servicio. La eliminación de una cuenta no implica la eliminación inmediata de sus creaciones ni contribuciones. En caso de querer eliminar una capa o lienzo, estos tendrán un temporizador de siete días hasta ser definitivamente eliminados, pudiendo ser bifurcados en ese proceso por otro usuario.

##### R.N.05. Licencias:

La plataforma tendrá un rango limitado de licencias permitidas. Todas ellas copyleft, asegurando la posibilidad de clonar un proyecto y contribuir.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

-- fin entregable 1 --

## 5. Modelo conceptual

### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1.  Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias


