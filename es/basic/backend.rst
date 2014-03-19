Dise�o del Programa Vusion
+++++++++++++++++++++++++++

Est� gu�a explicar� el dise�o del sistema (plataforma) Vusion. Para poder enviar un mensaje de Vusion al celular de un participante se usa mucha arquitectura (dise�o y desarrollo de sistema). Desde el software Vusion en un servidor, la nube a trav�s de la red m�vil de nuestros socios a los celulares de los participantes, todas las partes involucradas necesitan entregar el mensaje exitosamente.

Vista General
--------------

El diagrama de abajo muestra una vista sistem�tica del sistema y arquitectura Vusion. La arquitectura de Vusion consiste de dos partes. En la izquierda puede ver el servidor Vusion con el software Vusion funcionando. Aqu� es donde la informaci�n acerca del programa es almacenada.
En la parte derecha puede ver a los agregadores y las redes. Esta secci�n maneja el transporte de mensajes desde los servidores Vusi�n a los participantes y de regreso. Los participantes son las personas con celulares, quienes son contactados por los programas asociados a Text to Change.

.. figure:: _static/img/overview.png
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

	Vista sistem�tica de la arquitectura de Vusion.



Servidor Vusion
----------------

Primero nos enfocaremos en la parte izquierda de la imagen: el servidor Vusion. El servidor Vusion es un sistema de software que funciona en un servidor virtual en la nube. El sistema de software puede realizar un n�mero de tareas.

Primeramente ofrece un sitio web a trav�s del cual el administrador del programa puede crear programas. El administrador del programa crea y configura el programa.  Una vez que se crea el programa, el adminsitrador puede realizar seguimiento del progreso y recolectar resultados, todo a trav�s de la interface de la web. Puede encontrar una introducci�n a est� interface web aqu�: :doc:`Vusion introduction<login>`

El software Vusion est� dise�ado para posibilitar el env�o de SMS a n�meros telef�nicos del sistema. Esta es una caracter�stica central de los programas que ejecutamos. Al enviar mensajes, se pueden alcanzar personas. Vusion ahce eso posible. Los mensajes pueden ser enviados porque Vusion est� conectado a las redes de las compa��as telef�nicas. La siguiente secci�n contiene mayor informaci�n acerca del rol de las telef�nicas.

Finalmente, adem�s de enviar mensajes el software tambi�n puede recibir mensajes. Esto significa que los mensajes recibidos tambi�n pueden ser almacenados. Lo que lo hace a Vusion especial es que no solamente se puede enviar y recibir mensajes, sino tambi�n procesar el contenido de los mensajes y tener respuestas espec�ficas de acuerdo al contenido. Cuando se recibe un mensaje que contiene cierta palabra, Vusion puede realizar cierta acci�n. Esto le da al administrador del programa la posibilidad de crear interacciones complejas entre el participante y Vusion. De esta forma programas interactivos son creados.

El servidor Vusion con el software Vusion en el, es el cerebro del sistema. Es el lugar desde el cual todo es controlado y desde donde se toman las decisiones.


Integrador (Red de Transporte) y Operadores Telef�nicos 
--------------------------------------------------------

En la anterior secci�n se habl� acerca del sistema de software Vusion. En est� secci�n se cubrir� como Vusion env�a un mensaje y este llega a la persona correcta (deseada).

Para que los mensajes vayan de Vusion a los participantes de ida y vuelta, se usa un integrador. Vusion es una plataforma de SMS por lo tanto toda la comunicaci�n va a trav�s de redes de operadores m�viles. En cada pa�s funcionan cierto n�mero de operadores de red m�vil. Algunos muy conocidos son:

* Movilgate
* Orange
* Airtel
* Vodacom
* Vodafone

Hay muchas m�s de estas compa��as. El rol del integrador y las telef�nicas reside en que ellos tienen bases de red GSM a trav�s de todo el pa�s. Ellos conectan los celulares a la red de modo que los usuarios puedan recibir mensajes de texto y llamadas telef�nicas. Normalmente estos operadores env�an y reciben mensajes a y desde las redes a otras compa��as telef�nicas. Al hacer tratos con estas compa��as, Vusion tambi�n est� conectada a estas redes. Esto significa que Vusion es capaz de enviar y recibir mensajes de texto a trav�s de las redes conectadas.

Puede que esto suene sencillo, pero existe un n�mero de asuntos que lo hacen ligeramente complejo.

En casi todos los pa�ses hay varios operadores m�viles, cada uno con su red de estaciones base. Mobile phones are connected to these networks. One of the problems we face is that not all phones connect to all networks. For example if someone has an Orange phone, it only connects to the Orange mobile network. This means that If we want to communicate with that person, we need to make a deal with Orange. If we want to be able to connect to all users, we need to make deals with all the mobile network operators active in a country. This can be a very time-consuming process, but luckily there is a solution: Aggregators.

Un integrador es una compan�a local que tiene conexi�n con algunas o todas las redes de telefon�a de un pa�s. Hacer un trato con un integrador nos da acceso a multiples redes de telefon�a al mismo tiempo. De esta forma podemos alcanzar m�s gente con nuestros programas.


.. nota::
	**C�digos Cortos**

	Normalmente los n�meros de telefon�a celular tienen alredeor de 10 d�gitos. Estos son demasiados n�meros para que la gente los recuerde r�pidamente. En muchas campa�as las personas pueden enviar un mensaje de texto con una palabra a un n�mero para recibir informaci�n o para suscribirse a un programa, si tienen que recordar un n�mero muy largo esto no funciona. Para resolver este problema, las telef�nicas ofrecen un servicio llamado **c�digo corto**. Un c�digo o n�mero corto es especial, puede ser asignado a un servicio. Usualmente tiene de 4 o 5 d�gitos, lo cual significa que es f�cil para la gente recordarlo.
	Cuando alguien env�a un mensaje de texto al c�digo corto, el mensaje es remitido al destino al cual el c�digo corto est� registrado. En nuestro caso, Vusion. 




