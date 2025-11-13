# **Acta de Reunión**
Escritura de casos de uso (Prioridad Media

**Fecha y hora:** 12 de noviembre - 10:00 p.m.  
*Ubicación:* Sala de Discord

**Participantes:**  
Héctor Jesús Martínez Basurto, Abdiel Muñiz, Jesús Camacho.

**Coordinador de la reunión:** Abdiel Muñiz


---

# **Agenda de la reunión.**

---
Se tiene pensado hacer una escritura superficial de los casos de uso de prioriad media, antes de la siguiente revisión de los casos de uso de muy alta prioridad, los casos de uso a escribir, fueron:
1. Editar datos de usuario.
2. Consultar registro de ventas.
3. Autentificar personal.
---

# **Información y acuerdos tomados.**

---
Para cada caso de uso se utilizó la siguiente estructura
Alcance (Para el sistema al que se esta diseñando)
Nivel (metas u objetivos del usuario)
Actor primario (El actor que iniciaria el caso de uso)
Personas interesadas y sus intereses (Personas involucradas y el impacto que generan al utilizar el caso de uso)
Precondiciones (Las condiciones previas que deben tener los actores primarios para usar el caso de uso)
Postcondiciones (El cambio esperado que tendrá el sistema despues de haber utilizado el caso de uso)
Flujo basico (Los pasos basicos que trandrá el caso de uso para realizarse)
Flujo alternativo (Los pasos extras por si algun paso del flujo basi cambia)
Requerimientos especiales (Requerimientos no funcionales)
Lista de variaciones y tecnologias de datos (Metodos I/O y formato de datos)

## 1. UC - Editar datos de usuario
Para nuestro primer caso de uso de prioridad media, es decir, editar datos de usuario, se encontró un requisitos no funcionales mas el cual fue:
- La interfaz debe permitir editar campos específicos sin necesidad de rehacer el registro completo.

Entonces fue que el caso de uso se escribió de la siguiente manera:

**Caso de uso UC-3 | Editar datos del usuario**.

**Alcance:**  Sistema de registro de gimnasio.

**Nivel:**  Objetivo usuario.

**Actor primario:**  Recepcionista.

**Stakeholders and interests:**.

**Recepcionista:** Quiere corregir y actualizar los datos de los clientes sin ningún problema, asegurando que se actualicen los datos de manera correcta.
**Cliente:** Quiere tener la oportunidad de corregir y/o actualizar sus datos.
**Diseño del Gimnasio:** Busca satisfacer las necesidades de los clientes, procurando cubrir errores o disgustos de los clientes.

**Pre-Condiciones**
- El cliente tiene que estar registrado previamente en el sistema
- El recepcionista debe haber registrado en el sistema con su clave única

**Post-Condiciones**
- Los datos del usuario tienen que estar actualizados correctamente en la base de datos del sistema

**Flujo Normal**
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

**Flujo Alternativo**

3a El sistema no detecta la huella del cliente
1. Recepcionista solicita al cliente intentarlo nuevamente
2. Sistema vuelve a validar la huella.

2a. Si falla nuevamente, el recepcionista reinicia el lector de huella.

2b. Si se valida correctamente, continúa en el paso 4 del flujo normal

8a. El cliente no aprueba los nuevos cambios

1. Cliente indica que aun hay datos incorrectos
2. Recepcionista modifica nuevamente los cambios
3. Recepcionista muestra los datos corregidos
4. Cliente aprueba los nuevos cambios
5. continua el paso 9 del flujo normal

9a El sistema detecta inconsistencia en los datos modificados

1. Sistema muestra un mensaje de error
2. Recepcionista revisa los campos modificados
3. Recepcionista corrige los datos
4. Sistema valida nuevamente los datos
5. continua el paso 10 del flujo normal

*a El sistema pierde conexión a internet

1. Sistema activa el modo offline temporal
2. Los datos se guardan localmente
3. Al restablecer la conexión, el sistema sincroniza los datos

**Requerimientos especiales**

- Solo se permite editar datos tras autenticación del recepcionista mediante su clave única.
- La interfaz debe permitir editar campos específicos sin necesidad de rehacer el registro completo.
- Todas las acciones deben completarse en un máximo de 5 clics.
- El sistema debe ofrecer un tiempo de respuesta de 200 milisegundos.
- La pantalla de validación debe ser visible y legible a 1 metro de distancia.
- El sistema debe permitir modo offline temporal para editar datos locales, sincronizando al restablecer la conexión.
  
**LISTA DE VARIACIONES DE TECNOLOGÍAS Y DATOS**

Identificación del cliente por medio de lector de huella digital.



## 2. UC - Consultar registro de ventas
Para el siguiente caso de uso se encontraron los siguientes requisitos no funcionales:
- El sistema debe permitir filtrar ventas por múltiples criterios combinados (fecha, cliente, producto, monto, método de pago).
- El sistema debe permitir exportar los resultados en PDF.
- El sistema debe permitir modo offline para consultas locales recientes en caso de pérdida de conexión.

Y el caso de uso se escribió de la siguiente manera:

**UC 8 | CONSULTAR REGISTRO DE VENTAS**

**ALCANCE:** Sistema de gestión de ventas.

**NIVEL:** Objetivo del usuario.

**ACTOR PRIMARIO:** Recepcionista

**STAKEHOLDERS AND INTERESTS**

**Recepcionista:** Quiere consultar el historial de ventas para verificar transacciones realizadas y atender consultas de clientes.

**Cliente:** Espera que la información de su compra esté correctamente registrada para cualquier futura reclamación o cambio.

**Dueño del negocio:** Quiere un sistema confiable que registre y muestre correctamente todas las ventas realizadas, garantizando transparencia y control financiero.

**PRECONDICIONES**
- El recepcionista ha iniciado sesión en el sistema correctamente
- El sistema cuenta con registros de ventas almacenados.

**POSTCONDICIONES**
- Se muestra la información detallada de las ventas solicitadas (fecha, productos, total, método de pago, cliente, etc.)

**FLUJO NORMAL**
1. Recepcionista selecciona la opción “Consultar registro de ventas”
2. Sistema muestra un panel de búsqueda con filtros, por fecha, producto, cliente o número de factura.
3. Recepcionista ingresa los criterios de búsqueda.
4. Recepcionista da clic en el botón “Buscar”.
5. Sistema valida los criterios ingresados.
6. Sistema consulta la base de datos de ventas.
7. Sistema muestra la lista de resultados coincidentes con los criterios ingresados.
8. Recepcionista selecciona una venta específica para ver el detalle.
9. Sistema muestra el detalle de la venta seleccionada.
10. Recepcionista puede optar por exportar el registro a un archivo (PDF, Excel o CSV).
11. Sistema genera el archivo solicitado y lo descarga.

**FLUJO ALTERNATIVO**

5a. El recepcionista no ingresa ningún criterio de búsqueda.
1. Sistema muestra un mensaje indicando que se deben ingresar al menos un criterio de búsqueda.
2. Recepcionista ingresa los criterios y continúa en el paso 4 del flujo normal.
   
6a. No se encuentran resultados.
1. Sistema muestra un mensaje indicando que no existen registros que coincidan con los criterios seleccionados.
2. Recepcionista puede modificar los filtros y realizar una nueva búsqueda
3. Continua con el paso 4 del flujo normal.
   
10a. Error al generar el archivo.
1. Sistema notifica que hubo un error al generar el archivo.
2. Recepcionista puede intentar nuevamente la exportación o contactar al soporte técnico.

**REQUERIMIENTOS ESPECIALES**
- El sistema debe permitir filtrar ventas por múltiples criterios combinados (fecha, cliente, producto, monto, método de pago).
- El tiempo de respuesta de la búsqueda no debe superar los 2 segundos.
- El sistema debe permitir exportar los resultados en PDF.
- La interfaz debe ser accesible y responsiva, adaptándose a distintos tamaños de pantalla.
- El sistema debe permitir modo offline para consultas locales recientes en caso de pérdida de conexión.
- El sistema deberá estar disponible el 95% del tiempo, durante las 24 horas del día, para permitir consultas en cualquier momento.

**LISTA DE VARIACIONES DE TECNOLOGÍAS Y DATOS**

Exportación del registro de ventas utilizando librerías de generación de documentos.



## 3. Autenticar Personal

Para el ultimo caso de uso escrito en esta reunión, se encontraron más requisitos no funcionales los cuales fueron:
- El sistema debe bloquear la cuenta tras 3 intentos fallidos consecutivos.
- El sistema debe mantener la sesión activa mientras el usuario no cierre sesión.
- La pantalla de inicio de sesión debe mostrar mensajes claros y una indicación visual de carga durante la validación.

Y el caso de uso fue escrito asi:

**UC - 11		|	AUTENTICAR PERSONAL**

**ALCANCE -** Sistema de registro de gimnasio.

**NIVEL -** Objetivo del usuario

**ACTOR PRIMARIO -** Recepcionista

**STAKEHOLDERS AND INTERESTS**

**Recepcionista -** Quiere un sistema seguro para que no cualquier usuario tenga acceso a los movimientos para hacer en él

**Cliente -** Quiere tener certeza de que un recepcionista confiable esté manejando sus datos de forma segura.

**Dueño del gimnasio -** Quiere un sistema confiable donde se evite la intervención de terceros, quiere hacer un sistema que refleje transparencia y limitaciones entre sus clientes y trabajadores.

**PRECONDICIONES**
- El recepcionista tiene la clave de acceso al sistema.

**POSTCONDICIONES**
- El recepcionista ingresa al sistema principal.

**FLUJO NORMAL**
1. Sistema muestra la página de autenticación y pide la clave única.
2. Rececionista ingresa su clave valida.
3. Recepcionista envía la clave ingresada. 
4. Sistema valida la clave.
5. Sistema concede acceso y dirige al recepcionista a la página principal.

**FLUJO ALTERNATIVO**

4a. La clave de ingreso no es válida
1. Sistema informa sobre la clave inválida y permite intentar de nuevo
2. Recepcionista da click en “Intentar de nuevo”
3. Regreso al paso 2 del flujo normal

4b. Se intentó ingresar la clave de acceso más de 3 veces
1. Sistema muestra un mensaje “Se ha excedido el límite de intentos para acceder”
2. Sistema bloquea por 30 segundos el ingreso al sistema.
3. Se reinicia el caso de uso.

5a. El sistema no concede el acceso por un fallo en el sistema.
1. Se reinicia el caso de uso.

**REQUERIMIENTOS ESPECIALES**
1. El sistema debe ofrecer un tiempo de respuesta de alrededor de 200 milisegundos (casi inmediato). 
2. Todas las acciones del sistema deberán completarse en un máximo de 5 clics. 
3. El sistema deberá estar disponible el 95% del tiempo durante las 24 horas del día. 
4. La pantalla donde se muestra el mensaje de acceso debe ser visible y legible a 1 metro de distancia. 
5. Los botones y campos de acción más frecuentes deberán estar ubicados dentro del área visual principal del usuario. 
6. El sistema debe bloquear la cuenta tras 3 intentos fallidos consecutivos.
7. El sistema debe mantener la sesión activa mientras el usuario no cierre sesión.
8. La pantalla de inicio de sesión debe mostrar mensajes claros y una indicación visual de carga durante la validación.

**LISTA DE VARIACIONES DE TECNOLOGÍAS Y DATOS.**
Ninguno.

---

## Temas pendientes para la siguiente reunión.
Para nuestro siguiente taller de requisitos se terminará de escribir de manera superficial los casos de uso de prioridad baja.
---
