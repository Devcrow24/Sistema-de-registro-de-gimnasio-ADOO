# **Acta de Reunión**
Escritura de casos de uso (Prioridad Baja)

**Fecha y hora:** 13 de noviembre - 10:00 p.m.  
*Ubicación:* Sala de Discord

**Participantes:**  
Héctor Jesús Martínez Basurto, Abdiel Muñiz, Jesús Camacho.

**Coordinador de la reunión:** Abdiel Muñiz


---

# **Agenda de la reunión.**

---
Se tiene pensado hacer una escritura superficial de los casos de uso de prioriad baja, antes de la siguiente revisión de los casos de uso de muy alta prioridad, los casos de uso a escribir, fueron:
1. Generar reporte de ventas.
2. Agregar comentario.
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

## 1. UC - Generar reporte de ventas
**ALCANCE -** Sistema de registro de gimnasio.

**NIVEL -** Objetivo del usuario.

**ACTOR PRIMARIO -** Recepcionista

**STAKEHOLDERS AND INTERESTS**


**Recepcionista -** Quiere generar un reporte de una o más ventas de la fecha que desee para entregarlas al dueño

**Dueño del gimnasio -** Quiere tener reportes para tomar decisiones financieras en base a sus ventas.

**PRECONDICIONES.**

- El recepcionista ha seleccionado la venta con la cual quiere generar el reporte

**POSTCONDICIONES.**

- El sistema genera el reporte de venta correctamente

**FLUJO NORMAL.**
1. Recepcionista selecciona generar un reporte de ventas.
2. Sistema muestra los filtros de búsqueda disponibles
3. Sistema indica al recepcionista que especifique el reporte de la venta en especifico
4. Recepcionista selecciona el filtro en específico para generar el reporte
5. Recepcionista da clic en “Continuar”
6. Sistema valida los filtros del usuario.
7. Sistema da una vista previa del reporte que se va a generar y pregunta sobre la confirmación
8. Recepcionista confirma generar el reporte de dicha venta
9. Sistema pregunta el formato para generar el reporte (PDF, Excel o CSV)
10. Recepcionista selecciona el formato del reporte.
11. Sistema descarga el reporte conforme a los filtros y el formato.

**FLUJO ALTERNATIVO.**

6a. No existen ventas con los filtros seleccionados.
1. Sistema muestra un mensaje indicando que no existen registros que coincidan con los criterios seleccionados.
2. Regreso al paso 2 del flujo normal.
   
8a. Recepcionista no confirma porque no quería esos datos.
1. Da click en “cancelar”
2. Regreso al paso 2 del flujo normal.
   
11a. El sistema no descarga el reporte por fallas técnicas
1. Sistema notifica que hubo un error al descargar el archivo.
2. Recepcionista puede intentar nuevamente la exportación o contactar al soporte técnico.

**REQUERIMIENTOS ESPECIALES**
- El sistema debe permitir filtrar ventas por múltiples criterios combinados (fecha, cliente, producto, monto, método de pago).
- El reporte debe generarse en menos de 3 segundos
- El tiempo de respuesta de la búsqueda no debe superar los 2 segundos.
- El sistema debe permitir exportar los resultados en PDF.
- La interfaz debe ser accesible y responsiva, adaptándose a distintos tamaños de pantalla.
- El sistema debe permitir modo offline para consultas locales recientes en caso de pérdida de conexión.
- El sistema deberá estar disponible el 95% del tiempo, durante las 24 horas del día, para permitir consultas en cualquier momento. 

**LISTA DE VARIACIONES DE TECNOLOGÍAS Y DATOS.**
Ninguna.




## 2. UC - Agregar comentario.
El caso de uso se escribió de la siguiente manera:

**ALCANCE -** Sistema de registro de gimnasio.

**NIVEL -** Metas del usuario

**ACTOR PRIMARIO-** Recepcionista

**STAKEHOLDERS AND INTERESTS**

**Recepcionista -** Quiere tener un registro sobre el comportamiento de los clientes dentro de las instalaciones.

**Cliente -** Quiere que su comentario sobre los demás clientes quede registrado para recibir seguimiento por parte del personal si es necesario.

**Dueño del gimnasio -** Quiere tener una visualización o pruebas escritas de sus clientes para darles un seguimiento oportuno.

**PRECONDICIONES.**
- El cliente tiene una cuenta registrada.
- El recepcionista ha iniciado sesión en el sistema.
- El cliente o recepcionista quiere reportar una queja de otro cliente

**POSTCONDICIONES.**
- El sistema guarda el comentario en el perfil del cliente.

**FLUJO NORMAL.**
1. Recepcionista selecciona la opción para registrar un comentario
2. Sistema muestra un formulario de registro de comentarios.
3. Recepcionista llena el formulario.
4. Recepcionista da clic en guardar.
5. Sistema valida el formulario.
6. Sistema guarda el comentario y lo muestra en el perfil del cliente.
   
**FLUJO ALTERNATIVO.**

5a. Sistema detecta que no todos los campos del formulario han sido llenados
1. Sistema muestra el mensaje “Llena todos los campos del formulario”
2. Recepcionista llena los campos
3. Regreso al paso 4 del flujo normal

**REQUERIMIENTOS ESPECIALES**
- El sistema debe ofrecer un tiempo de respuesta de alrededor de 200 milisegundos (casi inmediato).
- La interfaz de usuario deberá incluir iconos y atajos para acceder a las  funcionalidades principales rápidamente. 
- Todas las acciones del sistema deberán completarse en un máximo de 5 clics. 
- El sistema deberá estar disponible el 95% del tiempo durante las 24 horas del día.
- La pantalla donde se muestra el mensaje de acceso debe ser visible y legible a  1 metro de distancia. 
- El sistema debe permitir modo offline temporal para registrar entradas locales cuando falle la conexión al servidor central, sincronizando datos al restablecerse la conexión. 
- Los botones y campos de acción más frecuentes deberán estar ubicados dentro del área visual principal del usuario.

**LISTA DE VARIACIONES DE TECNOLOGÍAS Y DATOS.**
Ninguna


---

## Temas pendientes para la siguiente reunión.
Para nuestro siguiente taller de requisitos se hara la segunda revisión de los requisitos de prioridad muy alta el dia 14 de noviembre, donde sebusca generar retroalimentacion y hacer una reescritura con mas artefactos que nos ayuden a tener los casos de uso muy bien estructurados
