L�mite de Funciones
++++++++++++++++++++

General
--------

Est� es una herramienta para delimitar la duraci�n de un programa y la cantidad de mensajes que un programa genera. El l�mite se establece en la p�gina de configuraci�n del programa.
Primero seleccione si se contaran solo los mensajes salientes o ambos entrantes y salientes. En el campo que indica Total ponga el n�mero de mensajes m�ximo permitido.
En los campos debajo del Inicio y Final del Programa se puede establecer la fecha. Cuando se establecen, el programa no enviar� ning�n mensaje fuera de ese per�odo de tiempo.

..
	Es una herramienta para delimitar la duraci�n de un programa y la cantidad de mensajes que un programa genera. 
	Niveles de usuario de administrador o m�s altos pueden configurar esto. Otros pueden verlo pero no editarlo.

Solo el adminsitrador o niveles de usuario m�s altos pueden editar las funciones de limites. Otros usuarios pueden ver la configuraci�n pero no cambiarla.

Escenarios
-----------
* 	Alguien se registra y le tienen que llegar 2 mensajes de respuesta. Solo le queda un cr�dito. El primer mensaje se enviar�, el segundo no.

	El historial mostrar� un estatus de **sin-cr�dito**. Si ajusta el l�mite para 50 mensajes m�s, el mensaje no enviado anteriormente no ser� enviado ahora. Deber� reprogramar el mensaje para que se envi� ahora.

..
	* 	Se lleg� al l�mite de tiempo pero todav�a tiene cr�ditos; no se enviar�n m�s mensajes. Todo el programa est� **cerrado**

* 	Un mensaje recibido est� esperando respuesta, pero el programa a�n no inicio, o ya termin�. En este caso el mensaje saliente tendr� un estatus de **no-credit-timeframe** y no ser� enviado.

**Nota:** En ambos casos el mensaje rechazado no ser� reprogramado para reenvi� autom�ticamente. Cuando hayan cr�ditos disponibles nuevamente, o cuando el programa alcance el marco de tiempo definido, los mensajes rechazados no ser�n reenviados.

