Solicitudes
#########################

General
=================

Una solicitud permite que los participantes interactuen con Vusion. La parte m�s importante de una solicitud es la palabra clave.
Esto le permitir� al sistema clasificar el mensaje de texto del participante y as� darle una respuesta apropiada o activar una acci�n requerida.
El signo verde significa que la palabra clave a�n no est� en uso, si aparece una cruz roja significa que la palabra clave est� siendo usada por otro programa. Tendr� que escoger otra palabra clave.
Puede escribir varias palabras claves y separarlas con una coma, en ese caso todas las palabras claves escritas activaran la misma respuesta. Esto puede utilizarse para prever posibles variaciones o errores de escritura que el usuario final pueda tener al enviar la palabra clave.


.. image:: _static/img/request1.PNG

La casilla para marcar que dice *'En el caso de que no coincidan las solicitudes, trate de coincidir solamente la primera palabra del mensaje.'*.
Esta opci�n sirve para aumentar la posibilidad de que a�n cuando el participante no responda con la palabra clave pero con alg�n mensaje similar, el participante todav�a recibir� una respuesta en lugar de ser un error.
En la pr�ctica esto significa que cuando un usuario env�e INFO en lugar de INFO 1 coincidir� con la palabra clave INFO 1. La coincidencia completa tendr� siempre prioridad ante la coincidencia parcial, por lo cual INFO 1 coincidir� con INFO 1 y no con INFO.

Ejemplo 1:

- Solicitud: INFO
- Casilla para marcar: no
- Usuario env�a: INFO 1
- **Vusion no procesar� la coincidencia** 

Ejemplo 2:

- Solicitud: INFO
- Casilla para marcar: si
- Usuario env�a: Info si quiero info
- **Vusion procesar� la coincidencia** 


Una response (respuesta) es lo que la persona que env�o el mensaje con la palabra clave al n�mero corto recibir� de forma inmediata luego de enviar el mensaje. 
Las respuestas no deben exceder los 160 car�cteres, l�mite de un mensaje de texto. 

.. image:: _static/img/request2.PNG

Cuadno haya dise�ado una response (respuesta) puede a�adir una acci�n a la solicitud. Esto es algo que pasar�
cuando alguien env�e un mensaje de texto con la palabra clave al n�mero corto.

.. image:: _static/img/request3.PNG

Es importante notar que **todos** los participantes necesitar�n tener el estado opt-in (activado) para poder participar en el programa.
Notar tambi�n que la acci�n enroll autom�ticamente le da al participante el estado opt-in. 


Una vez que hizo todo esto, guarde su solicitud.


Para una explicaci�n en la diferentes acciones disponibles por favor vaya a la p�gina: acciones.