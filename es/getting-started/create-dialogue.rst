Creación de Diálogo
###################

Opciones
--------------

**Tiene prioridad**


**Inscripción Automática**
Esta opción inscribirá automáticamente a todos los participantes que se encuentren en la base de datos en este diálogo así también a todos los participantes 
que recién hicieron el opt-in. **Precaución** Tan pronto como se presione *Guardar*, el diálogo comenzará para todos los participantes que se encuentren en el programa.

**Interacciones**


Tiempo
-----------

**Fixed Time (Tiempo Programado)**
Esta opción enviará un mensaje en un tiempo determinado, asegúrese que la zona horaria en la que se encuentra coincide con la zona horaria del país en el cual sus participantes viven.

**Offset days**
El mensaje será enviado x días después de que el participante envíe por última vez un mensaje.  


**Offset time**
El mensaje será enviado x minutos después de que el participante envíe por última vez un mensaje. 

**Respuesta Requerida**

Cuando esta opción es seleccionada los participantes no recibirán la pregunta/mensaje que este creando actualmente, **a no ser que** la pregunta que seleccione del menú es respondida.
Esto es útil cuando quiera forzar a los participantes a seguir cierta manera específica de usar su programa.

Mensajes Diferentes
--------------------

**Anuncio**

Un anuncio es la opción más sencilla. Es un mensaje que será enviado al participante a cierta hora. 




**Pregunta**

Una pregunta consiste en el contenido de la pregunta (por ejemplo. Cuál es su sexo?) y la palabra clave.
La palabra clave permite a Vusion reconocer que pregunta está respondiendo el participante. (por ejemplo. sexo)
Hay dos clases de preguntas. Abiertas y cerradas. 

En una pregunta cerrada todas las respuestas necesitan estar definidas. 
Puede aplicar una label a todas las respuestas que son recibidas como respuestas a esta pregunta. (por ejemplo. sexo)
Si define masculino como la respuesta, los participantes deberán responder escribiendo en el mensaje de texto *sexo masculino*.
Así el mensaje entrante de los participantes siempre tendrá la forma: *[palabra clave] [respuesta]*.
Continuando puede añadir una respuesta o acción específica a la respuesta.

Con una pregunta abierta puede añadir una label a las respuestas y programar una respuesta que es enviada a los participantes  una vez que respondieron la pregunta.
Note que no es posible adjuntar acciones a preguntas abiertas.


**Preguntas multi-palabra clave**

Esta opción es útil cuando solo hay dos respuestas posibles a la pregunta. 
Define la palabra clave como la opción de respuesta. Así cuando se le pregunta a un participante por su sexo, su respuesta no tiene que ser *sexo femenino* o *sexo masculino* sino que es suficiente con *femenino* o *masculino*.


**Otras opciones**


**Fije el número de respuestas sin coincidencia**

Esta opción limitará la cantidad de respuestas erróneas que el participante puede enviar.
Cuando fije esta cantidad en 3 (por ejemplo) y la pregunta es *Qué edad tiene? Responda con edad [espacio] su edad* alguien que continúamente responda así:

- 19
- Tengo 19 años 
- edad 19

Pasará. Sin embargo, si alguien contesta con: 

- 19
- Tengo 19 años
- mi edad es 19
- edad 19

Vusion ya no registrará esta respuesta como valida y el participante ya no recibirá más mensajes.
Si el participante no responde con la palabra clave Vusion ya no registrará esta respuesta como "respuesta sin coincidencia" ya que no se reconoce nada en la respuesta.

**Respuesta sin coincidencia**

Los Participantes no recibirán respuesta si su mensaje no es reconocido por Vusion. 

**Respuesta por defecto a mensaje sin coincidencia**

Vusion enviará un mensaje estándar. Puede configurar esto en la opción de configuración del programa.

**Mensaje personalizado para los mensajes sin coincidencia**

Acá puede configurar que mensaje recibirán los participantes si su respuesta no es reconocida por Vusion.

**Recordatorio**

Acá es donde puede definir recordatorios para su pregunta.
Tiene que definir el número de recordatorios y cuando serán enviados. 
Es importante notar que cuando todos los Mensajes Recordatorios ya fueron enviados y el participante todavía no respondió, ya no será posible que responda la pregunta posteriormente.
Puede solucionar este problema adjuntando una acción 'opt-out' y enviando un mensaje al participante diciendo que esta siendo dado de baja debido a la falta de respuesta a las preguntas que se le envió, dentro del marco de tiempo designado.
Si la persona quiere participar nuevamente en el programa deberá realizar un opt-in nuevamente. Otras acciones también pueden ser adjuntadas a la función del recordatorio.

Cuando *el número máximo de respuestas sin coincidencia* y *recordatorios* ya están ambos configurados y uno de los *límites/fechas* es sobrepasado, el otro expirará automáticamente.














