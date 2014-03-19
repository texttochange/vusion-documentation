Creaci�n de Di�logo
###################

Opciones
--------------

**Tiene prioridad**


**Inscripci�n Autom�tica**
Esta opci�n inscribir� autom�ticamente a todos los participantes que se encuentren en la base de datos en este di�logo as� tambi�n a todos los participantes 
que reci�n hicieron el opt-in. **Precauci�n** Tan pronto como se presione *Guardar*, el di�logo comenzar� para todos los participantes que se encuentren en el programa.

**Interacciones**


Tiempo
-----------

**Fixed Time (Tiempo Programado)**
Esta opci�n enviar� un mensaje en un tiempo determinado, aseg�rese que la zona horaria en la que se encuentra coincide con la zona horaria del pa�s en el cual sus participantes viven.

**Offset days**
El mensaje ser� enviado x d�as despu�s de que el participante env�e por �ltima vez un mensaje.  


**Offset time**
El mensaje ser� enviado x minutos despu�s de que el participante env�e por �ltima vez un mensaje. 

**Respuesta Requerida**

Cuando esta opci�n es seleccionada los participantes no recibir�n la pregunta/mensaje que este creando actualmente, **a no ser que** la pregunta que seleccione del men� es respondida.
Esto es �til cuando quiera forzar a los participantes a seguir cierta manera espec�fica de usar su programa.

Mensajes Diferentes
--------------------

**Anuncio**

Un anuncio es la opci�n m�s sencilla. Es un mensaje que ser� enviado al participante a cierta hora. 




**Pregunta**

Una pregunta consiste en el contenido de la pregunta (por ejemplo. Cu�l es su sexo?) y la palabra clave.
La palabra clave permite a Vusion reconocer que pregunta est� respondiendo el participante. (por ejemplo. sexo)
Hay dos clases de preguntas. Abiertas y cerradas. 

En una pregunta cerrada todas las respuestas necesitan estar definidas. 
Puede aplicar una label a todas las respuestas que son recibidas como respuestas a esta pregunta. (por ejemplo. sexo)
Si define masculino como la respuesta, los participantes deber�n responder escribiendo en el mensaje de texto *sexo masculino*.
As� el mensaje entrante de los participantes siempre tendr� la forma: *[palabra clave] [respuesta]*.
Continuando puede a�adir una respuesta o acci�n espec�fica a la respuesta.

Con una pregunta abierta puede a�adir una label a las respuestas y programar una respuesta que es enviada a los participantes  una vez que respondieron la pregunta.
Note que no es posible adjuntar acciones a preguntas abiertas.


**Preguntas multi-palabra clave**

Esta opci�n es �til cuando solo hay dos respuestas posibles a la pregunta. 
Define la palabra clave como la opci�n de respuesta. As� cuando se le pregunta a un participante por su sexo, su respuesta no tiene que ser *sexo femenino* o *sexo masculino* sino que es suficiente con *femenino* o *masculino*.


**Otras opciones**


**Fije el n�mero de respuestas sin coincidencia**

Esta opci�n limitar� la cantidad de respuestas err�neas que el participante puede enviar.
Cuando fije esta cantidad en 3 (por ejemplo) y la pregunta es *Qu� edad tiene? Responda con edad [espacio] su edad* alguien que contin�amente responda as�:

- 19
- Tengo 19 a�os 
- edad 19

Pasar�. Sin embargo, si alguien contesta con: 

- 19
- Tengo 19 a�os
- mi edad es 19
- edad 19

Vusion ya no registrar� esta respuesta como valida y el participante ya no recibir� m�s mensajes.
Si el participante no responde con la palabra clave Vusion ya no registrar� esta respuesta como "respuesta sin coincidencia" ya que no se reconoce nada en la respuesta.

**Respuesta sin coincidencia**

Los Participantes no recibir�n respuesta si su mensaje no es reconocido por Vusion. 

**Respuesta por defecto a mensaje sin coincidencia**

Vusion enviar� un mensaje est�ndar. Puede configurar esto en la opci�n de configuraci�n del programa.

**Mensaje personalizado para los mensajes sin coincidencia**

Ac� puede configurar que mensaje recibir�n los participantes si su respuesta no es reconocida por Vusion.

**Recordatorio**

Ac� es donde puede definir recordatorios para su pregunta.
Tiene que definir el n�mero de recordatorios y cuando ser�n enviados. 
Es importante notar que cuando todos los Mensajes Recordatorios ya fueron enviados y el participante todav�a no respondi�, ya no ser� posible que responda la pregunta posteriormente.
Puede solucionar este problema adjuntando una acci�n 'opt-out' y enviando un mensaje al participante diciendo que esta siendo dado de baja debido a la falta de respuesta a las preguntas que se le envi�, dentro del marco de tiempo designado.
Si la persona quiere participar nuevamente en el programa deber� realizar un opt-in nuevamente. Otras acciones tambi�n pueden ser adjuntadas a la funci�n del recordatorio.

Cuando *el n�mero m�ximo de respuestas sin coincidencia* y *recordatorios* ya est�n ambos configurados y uno de los *l�mites/fechas* es sobrepasado, el otro expirar� autom�ticamente.














