# **ACTA DE REUNIÓN**
Parte Final del Proyecto

**Fecha y hora:** 29 y 30 de noviembre - 10:00 p.m.  
*Ubicación:* Sala de Discord

**Participantes:**  
Héctor Jesús Martínez Basurto, Abdiel Muñiz, Jesús Camacho.

**Coordinador de la reunión:** Abdiel Muñiz

---

# **AGENDA DE REUNIÓN.**

---
Despues de una pausa, y de la revisión completa de los casos de uso escritos, se realizó el durante estos dos dias la creación del modelo de dominio con estas caracteristicas:
- Cambios del proyecto 
- Identificación de clases conceptuales
- Descripción de las clases conceptuales
- Conexión del modelo de dominio
---

# **INFORMACIÓN Y ACUERDOS TOMADOS.**
---
## 1.Cambios del proyecto.
Estos pequeños cambios y platicas se hicieron en las semanas de ausencia que tuvimos, no eran cambios muy relevantes por lo que se omitieron las minutas. En este casos, estos son de los cambios que se plantearon durante estas semanas:
- Se complementó la visión del proyecto identificando algunos huecos argumentales que no nos permitia definir con totalidad nuestro dominio del problema
- Se acomodaron de mejor manera con el formato FURPS las especificaciones complementarias.
- Se modificaron los objetivos en concreto que tenian los actores, jusstificando los casos de uso escritos
- Se eliminaron casos de uso que no debian ser parte del sistema.
- Se realizó un glosario para comprenden terminos escenciales.
- Por ultimo se identificaron riesgos que podrian ocurrir durante la implementación y despues de ser lanzado el proyecto
---
## 2.Identificación de clases conceptuales
Con ayuda del glosario, se hicieron dos metodos para identificar clases conceptuales:

*Metodo 1: Busca de sustantivos en casos de uso y requisitos especiales*

*Metodo 2: Revisión de proyectos similares que nos sirva de guia*

En dichos metodos se encontraron las siguientes clases conceptuales que podrían ser parte de nuestro modelo de dominio.
Registro, Huella biometrica, cliente, recepcionista, asistencia, membresía, pago, cuenta, acceso, entrada, vencimiento.
## 3. Descripción de las clases conceptuales
Las clases identificadas se acomodaron en una tabla con las consignas de simbolo e intención.

```Markdown
- Simbolo: Registro
- Intención: Evidencia de una actividad realizada, un registro tiene fecha y hora.
```
```
- Simbolo: Huella biométrica
- Intención: Dato biológico único de una persona utilizado para identificarla.
```
```
- Simbolo: Cliente
- Intención: persona que adquiere un servicio.
```
```
- Simbolo: Recepcionista
- Intención: Persona que se encargaría en la atención al cliente
```
```
- Simbolo: Asistencia
- Intención: Presencia de una persona en un lugar
```
```
- Simbolo: Membresía
- Intención: Servicios ofrecidos al cliente a cambio de un ingreso monetario
```
```
- Simbolo: Pago
- Intención: Transferencia de dinero a cambio de un servicio
```
```
- Simbolo: Cuenta
- Intención: Identidad registrada de una persona
```
```
- Simbolo: Acceso
- Intención: El derecho o el permiso para entrar
```
```
- Simbolo: Entrada
- Intención: Espacio por donde se entra a alguna parte
```
```
- Simbolo: Vencimiento
- Intención: Representa la fecha limite del plazo de un bien.
```

# 4. Conexión del modelo de dominio (Diagrama)
De todas las clases conceptuales identificadas, solamente se relacionaron algunas por el hecho de que habia clases similares que podrian adjuntarse en una sola o bien, tratarse de asociaciones entre las demas clases, se llegó a la conclusión entonces que el modelo de dominio termino siendo:
### Ciente
***Atributos:*** nombre, clave unica.
- Un *cliente* tiene una huella *biometrica*
- Un *cliente* registra creo o muchas *asistencias*
- Un *cliente* tiene una *membresia*
- Un *cliente* realiza cero o muchos *pagos*
- Un *cliente* tiene una *cuenta*

### Huella Biometrica
***Atributos:*** Huella
- Una *huella* pertenece a un *cliente*
- Una **huella* valida una *asistencia*

### Asistencia
***Atributos:*** Fecha, Hora.
- Cero o muchas *asistencias* son registradas por un *cliente*
- Una *asistencia* es validada por una *huella*.

### Cuenta
- Una *cuenta* pertenece a un *cliente*
- Una *cuenta* pertenece a un *recepcionista*

### Membresia
***Atributos:*** Fecha, Estado, Precio.
- Una *membresia* pertenece a un *cliente*
- Una *membresía* es renovada por cero o varios *pagos*

### Pago
***Atributos:*** Monto.
- Cero o varios *pagos* los realiza un *cliente*.
- Cero o varios *pagos* renuevan una *membresia*.

### Recepcionista
***Atributos:*** Nombre, clave unica
- Un *recepcionista* tiene una *cuenta*

# TEMAS PENDIENTES PARA LA SIGUIENTE REUNIÓN.
Realización de la exposición final.
