## **Acta de Reunión**
Recomendaciones de Casos de uso

**Fecha y hora:** 14 de noviembre - 10:00 p.m.  
*Ubicación:* Sala de Discord

**Participantes:**  
Héctor Jesús Martínez Basurto, Abdiel Muñiz, Jesús Camacho.

**Coordinador de la reunión:** Abdiel Muñiz


---

## **Agenda de la reunión.**

---
Despues de un drastico cambio de planes, se ha decidido (antes de la reescritura de los casos de uso de Prioridad Muy Alta) seguir las recomendaciones que se vieron en una clase sobre escrituras de casos de uso. Para ello se tomó en cuenta que se necesita:
1. Crear la lista de actores y objetivos
2. Crear el desarrollo de sistema CRUD
---

# **Información y acuerdos tomados.**

---
# 1 - Creación de la lista de actores y objetivos.
Para la creación de esta lista se basó en los casos de uso ya escritos que teniamos con anticipación y se descubireron objetivos de los actores que estaban dentro de los casos de uso ya creados. Nuestra lista entonces fue acomodada de la siguiente manera:
**Actor - Cliente**

**Objetivos:**
- Registrar entrada.
- Registrar datos.
- Pagar membresía.
- Editar datos.
- Realizar una compra.
- Registrar comentario.

**Actor - Recepcionista**

**Objetivos:**
- Registrar usuario.
- Registrar venta.
- Consultar registro de ventas.
- Buscar clientes.
- Generar reporte de ventas.
- Iniciar sesión.
- Registrar comentarios.


**Actor - Dueño**

**Objetivos:**
- Autenticar personal.
- Consultar registro de ventas.
- Generar registro de ventas.

**Actor - Sistema biometrico de huella dactilar**

**Objetivos:**
- Analizar huella dactilar.
- Vincularse con el sistema.

Estos objetivos van se acuerdo al sistema ya planteado.

# 2 - Sistema CRUD.
---
Se tomó en cuenta la recomendación de los casos de uso, y se aplicó el término CRUD, donde se seleccionaron los casos de uso: Registrar usuario, editar datos de usuario, eliminar usuario y buscar usuario para juntarlos en un caso de uso general llamado “Administrar Usuario”. En base a esto, escribimos su descripción de este caso de uso y adaptamos los casos de uso ya escritos para que concuerden con este nuevo caso de uso.

**1. Creación de Administrar Usuarios**

Se escribió el caso de uso de la siguiente manera:

**ALCANCE -** Sistema de registro de gimnasio.

**NIVEL -** Objetivo del usuario

**ACTOR PRIMARIO -** Recepcionista

**STAKEHOLDERS AND INTERESTS**

**Recepcionista -** Quiere gestionar y administrar los usuarios de manera rápida y eficaz, sin tener que manipular los datos de manera manual.

**Cliente -** Quiere que su información esté correcta, protegida y accesible cuando lo requiera.

**Dueño del gimnasio -** Quiere un sistema confiable para la administración centralizada de usuarios.

**PRECONDICIONES.**
- El recepcionista ha iniciado sesión en el sistema.

**POSTCONDICIONES.**
- El sistema realiza con éxito la operación de crear, buscar, editar o eliminar.

**FLUJO NORMAL.**
1. Recepcionista selecciona la opción “Administrar usuarios”.
2. Sistema desplegará las opciones disponibles (crear, buscar, editar y eliminar). 
3. Recepcionista selecciona una opción dependiendo de sus intereses.
4. Sistema redirige según la petición del recepcionista.

**FLUJO ALTERNATIVO.**

a* El sistema muestra fallos en su interfaz

1. El recepcionista reinicia el sistema.

4a. Recepcionista escoge crear.
1. Sistema acciona el UC1 - Registrar usuario.

4b. Recepcionista escoge editar.
1. Sistema acciona el UC3 - Editar datos de usuario.

4c. Recepcionista escoge buscar.
1. Sistema acciona el UC6 - Buscar cliente.

4d. Recepcionista escoge eliminar.
1. Sistema acciona el UC12 - Eliminar cliente.

**REQUERIMIENTOS ESPECIALES **
1. El sistema debe ofrecer un tiempo de respuesta alrededor de 200 milisegundos (casi inmediato). 
2. Solo se permitirá agregar o eliminar usuarios tras autenticación mediante una clave única del recepcionista. 
3. La interfaz de usuario deberá incluir iconos y atajos para acceder a las funcionalidades principales rápidamente. 
4. Todas las acciones del sistema deberán completarse en un máximo de 5 clics. 
5. El sistema deberá estar disponible el 95% del tiempo durante las 24 horas del día. 
6. El sistema debe conectarse con lector biométrico y lector de código, permitiendo actualizar o reemplazar los dispositivos sin modificar el software principal. 
7. El lector de huella debe reconocer al cliente en menos de 3 segundos el 95% del tiempo. 
8. La pantalla donde se muestra el mensaje de acceso debe ser visible y legible a 1 metro de distancia. 
9. El sistema debe permitir modo offline temporal para registrar entradas locales cuando falle la conexión al servidor central, sincronizando datos al restablecerse la conexión. 
10. Los botones y campos de acción más frecuentes deberán estar ubicados dentro del área visual principal del usuario. 
11. En caso de interrupción eléctrica o cierre inesperado, el sistema deberá guardar automáticamente la última transacción en curso 
12. El sistema debe mostrar los resultados de búsqueda en menos de 2 segundos el 90% del tiempo. 
13.  La interfaz debe permitir editar campos específicos sin necesidad de rehacer el registro completo.
14. El sistema debe permitir modo offline para consultas locales recientes en caso de pérdida de conexión.
15. El sistema debe mantener la sesión activa mientras el usuario no cierre sesión.

**LISTA DE VARIACIONES DE TECNOLOGÍAS Y DATOS.**
Sistema biométrico de huella dactilar.

---
**2. Crear (Registrar Usuario - adaptación)**

--No hubo necesidad de adaptar el flujo normal o alternativo, salvo modificar el paso 1 y 2 del flujo normal--

*Pre-adaptación*

**FLUJO NORMAL:**
1. Cliente solicita registrarse en el gimnasio.  
2. Recepcionista informa sobre las opciones de membresía disponibles.  
3. (...) 

*Adaptado*

**FLUJO NORMAL:**
1. Recepcionista informa sobre las opciones de membresía disponibles al cliente que quiere registrarse. 
2. Cliente elige una membresía. 
3. (...)

---

**3. Buscar (Buscar cliente - adaptación)

Se adaptó esta caso de uso, tenemos el antes y despues de los flujos (que fue lo unico adaptado)

*Pre-adaptación*

**FLUJO NORMAL:**
1. Recepcionista quiere buscar un cliente. 
2. Recepcionista ingresa el nombre del cliente en la barra de búsqueda. 
3. Sistema busca en la base de datos el nombre del cliente ingresado. 
4. Sistema valida que los datos ingresados sean correctos 
5. Sistema muestra al/los cliente(s) relacionados con la búsqueda. 
6. Recepcionista selecciona el perfil del cliente. 
7. Sistema muestra el perfil del cliente. 

*Adaptado*

**FLUJO NORMAL:**
1. Sistema muestra la barra de búsqueda.
2. Recepcionista ingresa el nombre del cliente en la barra de búsqueda.
3. Sistema busca en la base de datos el nombre del cliente ingresado.
4. Sistema valida que los datos ingresados sean correctos
5. Sistema muestra al/los cliente(s) relacionados con la búsqueda.
6. Recepcionista selecciona el perfil del cliente.
7. Sistema muestra el perfil del cliente.

---
**4. Editar (Editar datos de usuario - adaptación)**

Se adaptó esta caso de uso, tenemos el antes y despues de los flujos (que fue lo unico adaptado)

*Pre-adaptación*

**FLUJO NORMAL:**
1. Cliente solicita modificar sus datos del gimnasio.
2. Recepcionista solicita la huella del usuario.
3. Cliente proporciona su huella digital
4. Recepcionista pregunta al usuario los datos a modificar
5. Cliente proporciona los datos a cambiar
6. Recepcionista edita los datos proporcionados del usuario
7. Recepcionista muestra los nuevos datos del cliente
8. Cliente aprueba los nuevos cambios
9. Sistema valida el cambio de datos del cliente
10. Recepcionista guarda los cambios
11. Sistema actualiza el perfil del cliente

*Adaptado*

**FLUJO NORMAL:**
1. Recepcionista solicita el nombre del usuario.
2. Cliente brinda su nombre.
3. Sistema activa el “UC- Buscar cliente”
4. Recepcionista pregunta al usuario los datos a modificar
5. Cliente proporciona los datos a cambiar
6. Recepcionista edita los datos proporcionados del usuario
7. Recepcionista muestra los nuevos datos del cliente
8. Cliente aprueba los nuevos cambios
9. Sistema valida el cambio de datos del cliente
10. Recepcionista guarda los cambios
11. Sistema actualiza el perfil del cliente

---
**5. Eliminar (Eliminar cliente - Cración)**

Por ultimo se hizo la creación del caso de uso de Eliminar cliente, que ya se habia contemplado anteriormente, pero aun no se habia peusto en desarrollo porque se habia discutido que serian pasos innecesarios, pero ahora se ha replanteado nuevamente y se ha hecho la siguiente descripción:

**ALCANCE -** Sistema de registro de gimnasio.

**NIVEL -** Objetivo del usuario

**ACTOR PRIMARIO -** Recepcionista

**STAKEHOLDERS AND INTERESTS**

**Recepcionista -** Quiere eliminar al usuario de manera rápida y sin complicaciones, sin la posibilidad de un error humano de borrar al usuario por equivocación.

**Cliente -** Quiere que el proceso sea rápido y quiere asegurarse que sus datos sean eliminados correctamente.

**Dueño del gimnasio -** Quiere que la eliminación se haga de forma segura.

**PRECONDICIONES.**
- El recepcionista ha iniciado sesión en el sistema.
- El cliente tiene una cuenta registrada

**POSTCONDICIONES.**
- El sistema realiza con éxito la operación de eliminar cliente.
- El sistema eliminar al cliente de la base de datos

**FLUJO NORMAL.**
1. Recepcionista selecciona la opción “Eliminar usuario”
2. Sistema acciona el UC - Buscar cliente
3. Recepcionista a clic en “Eliminar”
4. Sistema muestra un mensaje de confirmación
5. Recepcionista confirma la eliminación del cliente
6. Sistema elimina la cuenta de la base de datos.
7. Sistema muestra un mensaje de “Cuenta eliminada con éxito”
8. Sistema redirige al recepcionista a la página principal.

**FLUJO ALTERNATIVO.**

a* El sistema muestra fallos en su interfaz
1. El recepcionista reinicia el sistema.

**REQUERIMIENTOS ESPECIALES**
1. El sistema debe ofrecer un tiempo de respuesta alrededor de 200 milisegundos (casi inmediato). 
2. Solo se permitirá eliminar usuarios tras autenticación mediante una clave única del recepcionista. 
3. La interfaz de usuario deberá incluir iconos y atajos para acceder a las funcionalidades principales rápidamente. 
4. Todas las acciones del sistema deberán completarse en un máximo de 5 clics. 
5. El sistema deberá estar disponible el 95% del tiempo durante las 24 horas del día. 
6. La pantalla donde se muestra el mensaje de acceso debe ser visible y legible a 1 metro de distancia. 
7. El sistema debe permitir modo offline temporal para registrar entradas locales cuando falle la conexión al servidor central, sincronizando datos al restablecerse la conexión. 
8. Los botones y campos de acción más frecuentes deberán estar ubicados dentro del área visual principal del usuario. 
9. En caso de interrupción eléctrica o cierre inesperado, el sistema deberá guardar automáticamente la última transacción en curso.
10. El sistema debe mostrar los resultados de búsqueda en menos de 2 segundos el 90% del tiempo. 
11. El sistema debe permitir modo offline para consultas locales recientes en caso de pérdida de conexión.
12. El sistema debe mantener la sesión activa mientras el usuario no cierre sesión.

**LISTA DE VARIACIONES DE TECNOLOGÍAS Y DATOS.**
Ninguno.



---
## Temas pendientes para la siguiente reunión.
Se estima que el dia de mañana ahora si se pueda hacer la reescritura de los casos de uso con esta retroalimentación planteada.
