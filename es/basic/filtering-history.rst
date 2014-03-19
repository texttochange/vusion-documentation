Filtrado de Historial
======================

El historial del programa provee algunas poderosas herramientas de filtrado. Empiece yendo a la p�gina de "Historial" de un programa y haga click en el bot�n "Filtrar" que se encuentra en la parte superior derecha de la pantalla. Esto le dar� un recuadro amarillo en el cual puede comenzar a definir su filtro o filtros.

La siguiente imagen muestra el recuadro del filtro y la pesta�a que ofrece los varios filtros que pueden ser usados:

.. image:: _static/img/filtering_history_start.png 


Desde aqu� se puede definir el filtro. Pero primero veamos m�s detalladamente la pesta�a del filtro para observar que opciones existen para filtrar.

Coincidir "all" (todas) o "any" (algunas) reglas del filtro
############################################################

.. image:: _static/img/filtering_history_overview.png 

Lo primero que se puede notar es que en la parte superior se puede elegir entre:

* *coincidir* **all** *de las siguientes reglas*
* *coincidir* **any** *de las siguientes reglas*

Si se elige coincidir con **all (todas)** las reglas, los mensajes que apareceran luego del filtrado coincidiran con **all (todas)** las condiciones que se definieron en el filtro. Por lo tanto, si se eligi� el filtro "Incoming Messages (mensajes entrantes)" y mensajes que contienen(messages containing) la palabra *hola*, los mensajes mostrados ser�n solamente los mensajes que sean ambos entrantes (incoming) **y** que contengan la palabra *hola*. Mensajes que **no** sean entrantes y que contengan **no** la palabra "hola" NO ser�n mostrados.

Si se elige coincidir con **any (algunas)** of the rules it works different. Suppose we want to filter on messages containing the word *hello* or messages containing the word *bye*. We would then say we want to match any of the rules, and define described filters. The end result will be a list of all messages containing the word *hello* and all the messages containing the word *bye*.

Si todav�a no est� claro, pienselo de esta forma. Si usamos la regla *all* basicamente estaremos diciendo que cada fila de filtro tiene un **Y** entremedio. Porque la lista resultante de mensajes tendr� que coincidir con el primer filtro **Y** el segundo filtro, **Y** el tercer filtro, etc. Cuando se usa *any* el **Y** es reemplazado por **O**. 

Para definir una regla de filtrado (UN FILTRO)
###############################################

Una vez que se haya decidido si se quiere coincidir *all (todos)* o *any (algunos)* de los filtros, podemos empezar a definir las reglas de filtrado.

Primero se selecciona el tipo de filtro. Los siguientes tipos de filtro est�n disponibles:

* *message direction* - filtre mensajes entrantes (incoming) o salientes (outgoing)
* *message status* - filtre de acuerdo al estado (status) del mensaje
* *date* - filtre en base a las fechas de los mensajes enviados/recibidos
* *participant phone* - filtre por n�mero de tel�fono (o parte de �l)
* *message content* - filtre on any of the words or strings in the message content
* *dialogue source* - filtre los mensajes que se relacionan a un di�logo en espec�fico
* *interaction source* - filtre los mensajes pertenecientes a una interacci�n en espec�fico
* *answers* - filtre en coincidencia o no a respuestas a preguntas realizadas

Una vez que se haya elegido el tipo de filtro que se quiera usar, aparecer�n diferentes opciones para aplicarlo. Para algunos filtros un segundo recuadro aparecer�. 

Este segundo recuadro permite elegir varias opciones para la aplicaci�n del filtro. Por ejemplo, si se elige el filtro *message direction (direcci�n del mensaje)*, un segundo recuadro aparecer� haciendo posible la elecci�n entre mensajes incoming (entrantes) o outgoing (salientes).

Para algunos otros filtros un tercer recuadro estar� disponible en el cual se pueden proveer detalles adicionales. El filtro de date (fecha) es un buen ejemplo. Cuando se elige date (fecha) se obtendr� un segundo recuadro en el cual se podr� elegir entre *until (hasta)* y *since (desde)*, sin embargo, un tercer recuadro tambi�n se presentar�, en este se puede escribir la fecha exacta en la cual se quiere el filtro.

.. image:: _static/img/filtering_history_date.png 

Otro ejemplo es el filtro de contenido de mensaje (message content):

.. image:: _static/img/filtering_history_content.png

Se puede elegir entre tres opciones en el segundo recuadro y el recuadro de texto nos da la posibilidad de escribir una palabra o fila sobre la cual VUSION buscar� la coincidencia.

Se pueden a�adir m�s reglas haciendo click en el bot�n **+** ubicado a la derecha de la regla de filtrado. Esto nos proporcionar� otra l�nea en la cual definir un filtro adicional. A la inversa, las reglas de filtrado pueden ser eliminadas al hacer click en el bot�n **-** que se encuentra al lado del bot�n **+**.

Para obtener los resultados del filtrado
#########################################

Una vez que todas las reglas de filtrado hayan sido definidas haga click en el bot�n *Filter* que se encuentra debajo de las reglas, esto dar� inicio al proceso de filtrado. Luego de un momento de espera los mensajes coincidentes aparecer�n.

Pueded ver todos los mensajes usando las flechas al costado derecho del filtro. Aqui tambi�n podr� ver cuantos mensajes coindicen con su filtro:

.. image:: _static/img/filtering_history_total.png

Si el filtro no provey� los resultados esperados puede hacer click en el bot�n con una flecha peque�a, ubicado en la parte derecha del recuadro amarillo de filtro para empezar a editar el filtro y tratar nuevamente con par�metros de filtrado diferentes.

Es importante notar que una vez definido un filtro se puede guardar f�cilmente, guardando el URL (link o direcci�n de enlace) como favorito (con el marcador de favorito). Luego, yendo al mismo URL (link) puede obtener el mismo filtro nuevamente. Esta es una forma f�cil de volver a ingresar a filtros pasados creados o usados en el pasado.

Tambi�n puede exportar los datos filtrados usando la opci�n **Export History (Exportar Historial)**. Esta opci�n se encuentra en la parte superior derecha de la pantalla. Al exportar se puede realizar mayor an�lisis de los datos usando un programa o aplicaci�n externa, Excel por ejemplo.




