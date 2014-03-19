Solicitudes
++++++++++++

En Vusion existen diferentes formas de interaccionar con los participantes. Una de esas formas es a tr�ves de las Solicitudes. Usar una Solicitud es una forma de que se aplique una acci�n autom�tica cuando un mensaje ingresa con cierta Palabra Clave. Cuando se configura una Solicitud se escoge una Palabra Clave que la active, y tambi�n se elige una acci�n que quiera que Vusion realize si se ingresa esa Palabra Clave.

Para administrar las Solicitudes del programa, haga click en Solicitudes en el men� del programa. Esto lo llevar� a la pantalla de Solicitudes. Ac� puede ver una lista con las Solicitudes activas y sus respectivas Palabras Claves, Respuestas y Acciones.

.. figure:: _static/img/req_list.png
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

	Pantalla de Solicitudes 

Como puede ver hay un n�mero de Solicitudes actualmente activas. Cada Solicitud tiene su propia Palabra Clave, con respuestas y acciones diferentes. 


Para crear una nueva Solicitud, haga click en el bot�n de Nueva Solicitud. Ac� puede a�adir una Solicitud a su programa. Hay 3 cosas que necesitan configurarse antes de crear una Solicitud.

 1. La Respuesta debe tener una Palabra Clave �nica para que los mensajes puedan ser reconocidos.
 2. La Respuesta puede tener una o m�s respuestas. Una Response (Respuesta) es una respuesta autom�tica para cuando entre un mensaje que contenga una Palabra Clave.
 3. La Respuesta puede tener una o m�s Acciones. Vusion puede realizar un n�mero de Acciones, desde simples como a�adir un tag al participante a m�s complicadas como activar eventos o mensajes programados. Las Acciones se explican a mayor detalle en la parte de abajo.

Esta es la pantalla en la cual se a�aden nuevas Solicitudes.

.. figure:: _static/img/req_add.png
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

	La pantalla para a�adir Solicitudes, aqu� puede crear una nueva solicitud 


Las caracter�sticas a configurar son:

Palabras Clave
===============

Lo primero al crear una Solicitud es crear una Palabra Clave. La Palabra Clave se usa como identificador. Todos los mensajes que comiencen con una palabra clave ser�n procesados como una Solicitud por Vusion. Para que los mensajes puedan ser identificados y procesados correctamente es necesario que las Palabras Claves sean �nicas para cada solicitud. Una buena caracter�stica de Vusion es que de forma autom�tica revisa si la Palabra Clave que quiere usar esta disponible o ya est� siendo usada en otra Solicitud.

.. nota:: 
	En Vusion las Palabras Claves no diferencian entre may�sculas y min�sculas por lo que la palabra *REGISTRAR* coincidir� con *registrar* y tambi�n con *REgisTRAR*. 
	Es importante notar que las Palabras Clave tienen que ser �nicas, es decir no repetirse, no solamente en el programa sino en todo el c�digo corto en el cual funciona el programa. En la mayor�a de los pa�ses solo tenemos a disposici�n uno o dos c�digos cortos, mientras manejamos muchos m�s programas. Esto significa que diferentes programas tienen que funcionar en el mismo c�digo corto. Vusion se asegurar� que no se use una Palabra Clave que ya este siendo usada, pero de todas formas es importante tener este punto en mente cuando se esta configurando la Palabra Clave.

Para configurar la Palabra Clave simplemente debe ingresar la palabra en el campo de *Palabra Clave*.

El recuadro para seleccionar (tickear) debajo del campo de Palabra Clave afecta como ciertos mensajes de texto coinciden con la Palabra Clave. Es importante entender exactamente que hace ya que los efectos son bastante sutiles. Tienen que ver con que si Vusion coincidir� la Palabra Clave con el mensaje completo o solamente con la primera palabra. Por ejemplo:


El administrador de un programa esta configurando la Palabra Clave "REGISTRO" para un programa. 

Caso 1: El recuadro para seleccionar no esta seleccionado 
Vusion har� coincidir los mensajes que contengan **solo** la Palabra Clave. Por ejemplo Vusion har� coincidir el mensaje:
	
	*Registro*

Sin embargo Vusion **no** har� coincidir:

	*Registro por favor, quiero mi registro!*


Caso 2: El recuadro para seleccionar esta seleccionado 
Ahora Vusion tratar� de hacer coincidir todo el mensaje a una Palabra Clave. Sin embargo cuando esto falla, tratar� de hacer coincidir la primera palabra del mensaje con la Palabra Clave. Por ejemplo Vusion todav�a har� coincidir el mensaje:

	*Registro*

Y **tambi�n** coincidir� el mensaje: 

	*Registro por favor, quiero mi registro!*

La diferencia entre estos dos casos es importante de entender. Se basa en la diferencia de buscar la coincidencia dentro del mensaje completo versus buscar la coincidencia con la primera palabra. Cuando se est� configurando la Solicitud deber� decidir cuidadosamente cual elegir para alcanzar los resultados esperados. 

Cuando la Palabra Clave ha coincidido exitosamente Vusion puede llevar a cabo dos acciones. Enviar una respuesta al participante o realizar una acci�n.

Response (Respuesta)
==========

La Response (Respuesta) se usa para contestar autom�ticamente al participante. Para a�adir un mensaje Response (Respuesta) a una Solicitud, haga click en el bot�n de *A�adir Response*. Aparecer� un recuadro amarillo en el cual podr� definir el mensaje que ser� enviado. 

Puede a�adir m�s de una Response (Respuesta) a una Solicitud al simplemente hacer click en el bot�n *A�adir Response*. Cada click a�adir� una Response (Respuesta). Tambi�n puede borrar una Response (Respuesta) al hacer click en el bot�n *X* que se encuentra en la esquina derecha del recuadro amarillo de Response (Respuesta).


Acciones
===========

Luego de autom�ticamente enviar una Response (Respuesta) como reci�n se explic�, se puede hacer mucho m�s con una Solicitud. Tambi�n es posible hacer Solicitudes que activen Acciones. Ac� es donde la plataforma Vusion realmente muestra su versatilidad y posibilidades. Tambi�n es donde configurar Vusion se complica un poco, ya que las Acciones pueden programar y activar otros eventos. 
Actualmente en Vusion hay implementadas varias Acciones que se pueden usar.

 - **opt-in**: Esto registrar� al remitente del SMS como Participante del programa. El remitente ser� a�adido a la base de datos de participantes. Un participante tiene que tener el estado opt-in para que se le puedan enviar mensajes a trav�s de la plataforma Vusion.
 - **opt-out**: Esta Acci�n cancela la acci�n opt-in descrita anteriormente. Pondr� al Participante en un estado opt-out (estado pasivo). Los Participantes que esten en estado opt-out no recibir�n mensajes del programa y apareceran pintados de rojo en la Pantalla de Participantes. Todos los tags y labels ser�n removidos.
 - **enroll**:  Esta Acci�n pone al participante en un di�logo. Para mayor informaci�n acerca de los Di�logos, vaya a la Gu�a de Di�logos. En la parte referencte a Di�logos -> enrolling
 - **delayed enroll**: Realiza la Acci�n de enroll con retraso (programado). Se puede seleccionar el tiempo de un retraso, d�a y hora en la cual el enrrollment (la acci�n) se llevar� a cabo.
 - **tag**: A�ada un tag a un Participante.
 - **reset**: Aplique un opt-out seguido de un opt-in. Remover� todos los tags y labels de la base de datos del Participante y ahora aparecer� como un Participante "limpio".
 - **feedback**: Env�a una respuesta autom�tica al Participante. Esta acci�n es muy similar a la Response (Respuesta).
 - **proportional tag**: Esto le da la posibilidad de autom�ticamente dar un tag a una parte de los participantes y otro tag al resto de los participantes. Esta caracter�stica es usada para dividir aleatoriamente a los Participantes en grupos, por ejemplo si quiere elegir aleatoriamente al 5% de sus participantes para darles un premio, puede usar esta Acci�n para darles el tag al 5% de sus participantes como el grupo ganador.
 - **url forward**: Reenv�a el mensaje entrante a un URL. Cuando se esta haciendo un proyecto de recolecci�n de datos, posiblemente el socio quiera analizar los resultados por su cuenta en tiempo real. Usando esta Acci�n los mensajes todav�a estar�n en Vusion pero tambi�n ser�n reenviados directamente a otro servidor designado.
 - **sms forward**: Esta Acci�n enviar� un SMS a todos los Participantes que tengan un cierto tag. El contenido del mensaje puede ser generado din�micamente. Puede encontrar m�s informaci�n en el :doc:`SMS forwarding guide </advanced/smsforwarding>`


 Como puede ver hay muchas Acciones disponibles. Adem�s de ello puede a�adir m�s de una Acci�n a una Solicitud, dependiendo de sus necesidades. A�adir Acciones m�ltiples funciona de la misma forma que a�adir Solicitudes multiples. Hacer click en el bot�n de a�adir agregar� otra Acci�n a su Solicitud.
 Cuando se est� dise�ando una Solicitud un buen primer paso es definir exactamete que deber�a pasar si se activa la Solicitud. Si eso se define claramente, elegir la combinaci�n apropiada de Acciones se convierte en algo mucho m�s sencillo.
