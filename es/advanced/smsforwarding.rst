Env�o de SMS
#############

Caso de Uso
------------
Considere el siguiente caso pr�ctico: Una Organizaci�n est� configurando un servicio de Alerta and Rescate. El participante puede solicitar ayuda a la organizaci�n simplemente al enviar la palabra AYUDA al c�digo corto.
El SMS ser� autom�ticamente reenviado a diferentes miembros de la organizaci�n, los cuales se aseguraran de que alguien en le vecindario se aproxime inmediatamente al participante.

El siguiente dibujo muestra como funiconar�a este ejmplo.

.. image:: _static/img/smsforwarding_use_case.jpg


**1 :** El participante env�a un mensaje de Alerta.

**2 :** Vusion crea un mensaje de notificaci�n para todos los participantes que tengan la etiqueta (tag) **Alerta**. El mensaje puede ser personalizado para incluir informaci�n de los participantes,el tiempo o incluso el contenido del mensaje de alerta.

**3 :** Los participantes con la Etiqueta (Tag) recibir�n un mensaje de notificaci�n.


Como Configurar el Env�o de un SMS
-----------------------------------

Ya sea en una Solicitud o un Di�logo, puede seleccionar la acci�n *SMS Forward* de la lista de acciones. Dos campos aparecer�n como se muestra debajo:
 
.. image:: _static/img/smsforwarding_action.png

**Receiver Tag:** 
En este recuadro para escribir, escriba el tag (etiqueta) de los participantes a los cuales les quiere enviar el mensaje. Por favor asegurese que algunos de los participantes ya est�n registrados y con el tag que escribi� sino nadie ser� notificado.

**Contenido:** 
En este recuadro para escribir, escriba el mensaje que quiera enviar. Para m�s detalles en cuanto a como personalizar el mensaje, vea la siguiente secci�n.


Mensaje de Notificaci�n
------------------------

Este es un ejemplo de mensaje de notificaci�n, en el cual asumiremos que el env�o de alerta fue creado en el programa con 2 etiquetas (labels):

#. nombre:Juan
#. direcci�n:2do anillo diagonal al Cristo

Entonces este mensaje de notificaci�n contiene:

"Alerta **[participant.nombre]** (**[participant.phone]**) en **[participant.direcci�n]** dice '**[context.message]**' a las **[time.H]**:**[time.M]**"

* **[participant.name]**      mostrar� el nombre del participante que env�a el mensaje de Alerta.
* **[participant.phone]**     mostrar� el n�mero de tel�fono del participante que env�a el mensaje de Alerta.
* **[participant.address]**   mostrar� la direcci�n participante que env�a el mensaje de Alerta.
* **[context.message]**       mostrar� el mensaje de Alerta enviado por el participante.
* **[time.H]**                mostrar� la hora en que el participante envi� el mensaje de Alerta.
* **[time.M]**                mostrar� el minuto en que el participante envi� el mensaje de Alerta.

si el participante env�a "Alerta de ayuda" donde "Alerta" es la palabra clave. El participante con el tag para recibir este mensaje recibir� el siguiente mensaje:
**"Alerta Juan (+2567702222) en 2do anillo diagonal al Cristo dice 'Alerta de ayuda' a las 10:50"**
