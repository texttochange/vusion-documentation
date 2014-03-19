Límite de Funciones
++++++++++++++++++++

General
--------

Está es una herramienta para delimitar la duración de un programa y la cantidad de mensajes que un programa genera. El límite se establece en la página de configuración del programa.
Primero seleccione si se contaran solo los mensajes salientes o ambos entrantes y salientes. En el campo que indica Total ponga el número de mensajes máximo permitido.
En los campos debajo del Inicio y Final del Programa se puede establecer la fecha. Cuando se establecen, el programa no enviará ningún mensaje fuera de ese período de tiempo.

..
	Es una herramienta para delimitar la duración de un programa y la cantidad de mensajes que un programa genera. 
	Niveles de usuario de administrador o más altos pueden configurar esto. Otros pueden verlo pero no editarlo.

Solo el adminsitrador o niveles de usuario más altos pueden editar las funciones de limites. Otros usuarios pueden ver la configuración pero no cambiarla.

Escenarios
-----------
* 	Alguien se registra y le tienen que llegar 2 mensajes de respuesta. Solo le queda un crédito. El primer mensaje se enviará, el segundo no.

	El historial mostrará un estatus de **sin-crédito**. Si ajusta el límite para 50 mensajes más, el mensaje no enviado anteriormente no será enviado ahora. Deberá reprogramar el mensaje para que se envié ahora.

..
	* 	Se llegó al límite de tiempo pero todavía tiene créditos; no se enviarán más mensajes. Todo el programa está **cerrado**

* 	Un mensaje recibido está esperando respuesta, pero el programa aún no inicio, o ya terminó. En este caso el mensaje saliente tendrá un estatus de **no-credit-timeframe** y no será enviado.

**Nota:** En ambos casos el mensaje rechazado no será reprogramado para reenvió automáticamente. Cuando hayan créditos disponibles nuevamente, o cuando el programa alcance el marco de tiempo definido, los mensajes rechazados no serán reenviados.

