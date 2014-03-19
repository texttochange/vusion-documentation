Mensajes separados y Mensajes personalizados
+++++++++++++++++++++++++++++++++++++++++++++

Enviar un mensaje a un grupo de personas en Vusion es f�cil. Esta gu�a le explicar� como puede enviar un mensaje a un grupo de personas. Se usa este tipo de mensajes cuando no se requiere interacci�n con los participantes.



Mensajes Separados 
==================

En el men� del programa encontrar� un item llamado Mensajes Separados. Esto lo llevar� a la pantalla de Mensajes Separados. 

.. figure:: _static/img/sep_list.png
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px


En esta pantalla podr� ver una lista de Mensajes Separados enviados previamente con algunos detalles acerca de ellos. La lista tambi�n muestra los mensajes programados. Estos son mensajes que ya fueron creados y est�n listos para ser enviados, esperando que llegue el tiempo para el cual el env�o fue programado. Si el mensaje programado todav�a no fue enviado todav�a se le pueden hacer cambios. Para hacerle cambios, haga click en el bot�n Editar en la parte derecha del mensaje. 

Tambi�n existe la posibilidad de eliminar un Mensaje Separado. Si el mensaje todav�a no fue enviado ser� removido de los mensajes programados. Si el mensaje ya fue enviado, el eliminarlo borrar� el registro del mensaje de Vusion.


.. advertencia:: El recuadro necesita ser tickeado (checking)
.. nota::
	La mayor�a de las caracter�sticas de los mensajes se explican por si solas. Por ejemplo La Hora muestra a que hora fue creado el mensaje. Algo que no es tan sencillo de interpretar es la columna de Delivery (Env�o). En esta columna ver� seis n�meros, de los cuales el significado no es claro inmediatamente. Estos n�meros representan el estado de los mensajes enviados. Estos son detalles t�cnicos que se encuentran muy relacionados a la forma en la cual los mensajes son enviados en Vusion. Imagine que tiene un mensaje con el Delivery Status (Estado de env�o): 6 (5/4/3 -2/1)

	- 6: N�mero total de mensajes enviados

	- 5: N�mero de mensajes aceptados por las compa��as telef�nicas 
	- 4: N�mero de mensajes que todav�a est�n esperando ser aceptados por las compa��as telef�nicas 
	- 3: N�mero de mensajes rechazados por las compa��as telef�nicas 

	- 2: Check
	- 1: Check


Enviar un mensaje separado es f�cil: en la pantalla de Mensajes Separados, haga click en Nuevo Mensaje Separado. Esto lo llevar� a la pantalla A�adir Mensaje Separado. 

.. figure:: _static/img/sep_add.png
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px


En esta pantalla puede crear un Mensaje Separado. Para crear un Mensaje Separado necesita ingresar 4 caracter�sticas.

 - **Nombre**

   Ac� debe ingresar el Nombre que quiere darle a este Mensaje Separado. Use este nombre para reconocer el mensaje. Si es la invitaci�n para un evento le podr�a dar un nombre como:  *Invitaci�n para la Reuni�n de Enero*.


 - **Enviar A**

   Define a quien se enviar� el mensaje. Ac� hay 3 opciones

	 - **Todos los participantes:** Env�e el mensaje a todos los participantes del programa.
	 - **Participante coincidente:** Esta opci�n trabaja de forma similar a la opci�n Filtrado de Participantes. Ac� puede seleccionar una o m�s caracter�sticas para los participantes, en base a los tags (etiquetas) disponibles. Los participantes que coincidan con las caracter�sticas (tags) escogidas recibir�n el mensaje.
	 - **Lista de participantes:** Use los n�mero de tel�fonos de un archivo. Haga click en el bot�n *Seleccionar Archivo* y seleccione el archivo de su ordenador.



 - **Content (Contenido)**

   El contenido del mensaje es el mensaje que los participantes seleccionados recibir�n. Puede usar un mensaje predefinido al seleccionarlo de la pesta�a disponible que se encuentra encima del recuadro para definir el contenido. Esto har� que el mensaje predefinido aparezca en el recuadro de Content (Contenido). M�s adelante se explicar� como crear un Mensaje Personalizado (predefinido).

   Tambi�n puede simplemente escribir el mensaje que desee enviar en el recuadro de Content (Contenido). 


 - **Programaci�n**


   La Programaci�n establece el momento en el cual quiere que Vusion env�e el mensaje. Puede hacer que Vusion haga el env�o inmediatamente, o programar el mensaje para que sea enviado en alg�n punto en el futuro. Para programar un mensaje seleccione *Hora Fija*, y haga click en el c�rculo para seleccionar la opci�n. Un seleccionador aparecer� para ayudarlo a establecer correctamente la  fecha y hora.

   .. nota:: 
      El selector de fecha y hora trabaja estableciendo una fecha y hora absolutos, no fecha y hora relativos. La fecha y hora que ingrese ser�n la fecha y hora en el que el mensaje ser� enviado.


Una vez que est�s caracter�sticas hayan sido establecidas, haga click en *Guardar* para guardar el mensaje creado. Si programa el mensaje para que sea enviado inmediatamente el mensaje ser� enviado inmediatamente. Si programa el mensaje para ser enviado alg�n tiempo en el futuro, el mensaje se guardar� y enviar� en el tiempo definido. En este caso todav�a podr� realizar ajustes a su mensaje antes de su env�o programado.



Mensajes Personalizado 
======================

En el men� del programa, debajo de Mensajer Separados encontrar� un item llamado *Mensajes Personalizados*. En esta pantalla podr� definir y guardar un mensaje que luego podr� usar como Mensaje Separado por ejemplo. Esto puede ser �til si tiene que enviar el mismo mensaje m�ltiples veces.

Cuando haga click en Mensajes Personalizados en el Men� del Programa, ver� la pantalla de Mensajes Personalizados.

.. figure:: _static/img/sep_predefined_list.PNG
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

Ac� puede ver una lista de mensajes actualmente disponibles. Haciendo click en el bot�n Editar puede cambiar (editar) un Mensaje Personalizado. Haciendo click en el bot�n Eliminar podr� borrar el mensaje.

Para crear un Mensaje Personalizados haga click en el bot�n Nuevo Mensaje Personalizado. Esto le dar� una pantalla en la cual podr� escribir el mensaje. 

.. figure:: _static/img/sep_predefined.PNG
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

Esta pantalla es muy simple. Tiene dos recuadros de texto. En el primero debe ingresar el nombre del Mensaje Personalizado. Use un nombre que haga f�cil el reconocer el mensaje. Luego ver� un recuadro en el cual se debe redactar el contenido del mensaje. Este es el texto que eventualmente ser� enviado a los participantes. 

Haciendo click en el bot�n *Guardar*, guardar� su Mensaje Personalizado para que lo pueda usar cuando lo requiera.
