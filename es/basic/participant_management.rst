Administraci�n de los Participantes
+++++++++++++++++++++++++++++++++++
Esta secci�n cubre la administraci�n de los participantes en Vusion. Administrar los participantes de forma eficiente es muy importante, especialmente en programas con gran cantidad de participantes. Vusion tiene numerosas herramientas a disposici�n para ayudarlo en las tareas varias que posiblemente necesite realizar.


Los participantes son una parte muy importante del sistema Vusion. Un participante es identificado por su n�mero de celular. En la base de datos de Vusion m�s informaci�n puede ser a�adida al registro del participante, tal como la fecha en la cual el participante fue a�adido a la base de datos, dialogos en los cuales se encuentra registrado (enrolled) y las tags y labels que contienen informaci�n adicional acerca del participante. Toda esta informaci�n junta puede crear un perfil extenso del participante. Esta informaci�n luego puede ser exportada y analizada.

.. figure:: _static/img/part_list.png
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

	La pantalla de Participantes de Vusion 

A�adir participantes
---------------------

Una de las primeras y m�s b�sicas tareas cuando se inicia el uso de Vusion es a�adir participantes a la base de datos de Vusion. Para poder enviar un mensaje necesita tener por lo menos un participante en su base de datos.

A�adir un participante
================================
Para a�adir un participante haga click en el bot�n **A�adir**. Ubicado en la parte superior derecha de la pantalla.  

.. figure:: _static/img/part_add.PNG
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

	La pantalla de Adici�n de Participantes de Vusion 

Ahora ver� una pantalla en la cual puede ingresar un n�mero de tel�fono. Ingrese el n�mero telef�nico del participante que quiera a�adir y haga click en el bot�n Guardar. Felicidades! A�adio un participante. Ahora este participante aparecer� en la pantalla de Participantes.


Importar participantes de un archivo
=====================================
En muchos casos a�adir participantes uno por uno no es muy eficiente. Existe otra forma de a�adir participantes y es importarlos de un archivo. Haciendo click en el bot�n **Importar** se podr� acceder a la pantalla de Importaci�n de Participantes. Aca podr� escoger un archivo del cual quiera que Vusion importe los contactos.

.. figure:: _static/img/part_import.PNG
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

	La pantalla de Importaci�n de Participantes de Vusion 

Puede importar de un archivo CSV o XLS. La primera columna deber� contener los n�meros de celulares. Las otras columnas en la primera fila ser�n vistas como labels de los participantes, en la cual el nombre de la label ser� el nombre asignado a cada columna de esta primera fila.

.. figure:: _static/img/part_excel.PNG
	:width: 400px
	:align: center
	:alt: image19.png
	:figwidth: 800px

	La primera entrada de la primera columna , celda A1 en Excel, deber� siempre contener el texto "phone". Otras columnas pueden contener Labels para los participantes


En la pantalla de Importaci�n de Participantes tambi�n puede a�adir autom�ticamente un tag a los participantes importados. Escriba el tag que quiera a�adirles a los participantes en el espacio "Tag imported participants". Cuando seleccione el archivo correcto y el tag que quiera a�adir, haga click en **Subir**. El archivo ser� subido y los participantes ser�n a�adidos a la base de datos con el tag adjuntado.


Administraci�n de los Participantes 
------------------------------------

La administraci�n de sus participantes puede hacerse de dos maneras diferentes. Si necesita hacer un cambio a un solo participante, o solamente a algunos, puede hacerlo individualmente. Tambi�n puede realizar acciones a grupos de participantes al primero seleccioanr el grupo que se quiere modificar y luego realizar la acci�n para todo el grupo.

Administraci�n de Participantes Individuales
=============================================
Hay casos en los cuales necesita realizar una acci�n a un solo participante. Puede Ver, Editar o Eliminar participantes de forma individual con los botones mostrados a la derecha de cada participante. 



- El bot�n **Mostrar** lo llevar� a una pantalla que mostrar� los detalles acerca del participante. Mostar� informaci�n b�sica del participante como su n�mero de tel�fono, labels y tags. Tambi�n muestra el historial del participante, aqu� podr� ver el historial de toda la comunicaci�n entre Vusion y el participante. Tambi�n tenemos opciones para Editar o Eliminar el participante
- El bot�n **Editar** lo llevar� a una pantalla en la cual podr� cambiar la informaci�n de los participantes. Cosas que puede cambiar aqu�: N�mero de tel�fono, Labels, Tags y los di�logos en los cuales el participante esta subscrito (enrolled). 
- El bot�n **Eliminar**, eliminar� al participante de la base de datos, incluyendo el historial del participante. Esta acci�n es permanente y no puede ser deshecha, por favor tenga precauci�n.

Filtrado de Participantes
==========================
Cuando es necesario aplicar las acciones a grupos m�s grandes de participantes, los controles de la parte superior hacen sencillo manejar grupos grandes. Acciones que se pueden realizar con los grupos de participantes son: Exportar, Tag, Untag y Eliminar. Antes que pueda realizar una acci�n a un grupo de participantes, la primera tarea a realizar es seleccionar el grupo que quiera modificar. Es muy importante seleccionar el grupo correcto, de otra forma el proceso puede ir mal f�cilmente. Para seleccionar el grupo debe usar el bot�n de filtrado.

Cuando hace click en el bot�n de filtro, un recuadro amarillo grande aparecer�. 

.. figure:: _static/img/part_filterbox.PNG
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

	Esta es la interface de Filtro. 


En la interface de Filtrado puede crear filtros para seleccionar registros con cierta informaci�n. Por ejemplo: como dijimos antes, todos los participantes importados de un archivo son autom�ticamente asignados con el tag: **imported**. Al usar el filtro podemos seleccioanr participantes con este tag. Para crear un filtro que seleccione a todos los participantes con el tag **imported**, primero haga click en Filtrar. Ahora puede ver el recuadro amarillo de filtrado. La primera l�nea con las opciones "all" y "any" no son relevantes por ahora. Se volvera a eso luego. Por ahora, haga click en la pesta�a vacia y seleccione "tagged". Ahora 2 recuadros extras aparecer�n. Estos tres recuadros forman una regla de filtrado. Para seleccionar todos los participantes con el tag "imported", seleccione un filtro con::
	
	tagged | con | imported

Now click Filter. The page will reload and show all records of participants with the tag "imported". Using this same method you can filter on a number of other characteristics. At the moment you can filter on:
 - **phone**: filtre por n�mero de tel�fono.
 - **optin**: filtre por fecha de opt-in (ingreso o activaci�n a la plataforma).
 - **optout**: filtre por opt-out (salida o desactivaci�n de la plataforma).
 - **enrolled**: filtre por los di�logos en los cuales el participante est� registrado (enrolled in).
 - **tagged**: filtre en base a los tags que tiene el participante.
 - **labels**: filtre en base a las labels que tiene el participante.

Luego de seleccionar la opci�n en base a la cual quiera filtrar, recuadros especiales aparecer�n a lado del primer recuadro para hacer el filtro m�s espec�fico. 
El ejemplo de arriba muestra como seleccionar un filtro. La mayor�a de las veces una regla de filtrado ser� suficiente para seleccionar lo que necesita, pero algunas otras veces necesitar� filtros m�s complejos. En Vusion es posible crear m�s de una regla de filtrado al solamente hacer click en el bot�n "+" que se encuentra en la parte superior derecha del recuadro de filtrado. Esto generar� otra l�nea en la cual podr� ingresar otra regla de filtrado. Cuando se ingresa m�s de una regla de filtrado es cuando la diferencia entre "all (todo)" y "any (alguno)" en la primera l�nea del recuadro de filtrado cobra mucha importancia. 

Suponga que tiene dos reglas de filtrado, regla A y regla B y el filtro esta seleccionado para "Coincidir all (todo)". Ahora solo se mostrar�n los participantes (registros) que coincidan con la regla A **y** la regla B. Cuando el filtro este seleccionado para para "Coincidir any (alguno)", todos los participantes (registros)  coincidan con la regla A **O** la regla B ser�n seleccionados. En otras palabras, cuando se selecciona "all (todo)", **ambas** reglas tienen que cumplirse, y cuando se selecciona "any (alguno)", **por lo menos una** regla tiene que cumplirse. 

En Vusion es posible crear filtros con m�ltiples reglas de filtrado. Cuando se trabaja con m�ltiples reglas de filtrado, es muy importante entender la diferencia entre elegir la coincidencia de "all (todas)" o "any (algunas)" de las reglas de filtrado.

Para estudiar m�s detenidamente las opciones de filtrado de Vusion, por favor dir�jase al :doc:`History Filtering guide <filtering-history>`

Realizar acciones en grupos de participantes 
=============================================
Cuando se haya hecho la selecci�n correcta, puede aplicar acciones a todos los participantes seleccioandos. Las acciones disponibles son:

 - **Tag**: A�adir un Tag a todos los participantes seleccionados. Un tag es un texto corto que puede ser usado para marcar a ciertos participantes.
 - **Untag**: Remueve un Tag de todos los participantes seleccionados.
 - **Exportar**: Desacarga a su computadora un archivo CSV, que contiene los participantes seleccionados por el filtro aplicado. El archivo contiene todos los detalles de los participantes, como tags y labels. Los archivos exportados pueden ser analizados en Excel o en otros programas de an�lisis.
 - **Eliminar**: Elimina a los participantes seleccionados de la base de datos. Cuando se eliminan participantes, son removidos de forma permanente. Esta acci�n no puede ser deshecha.

Es muy importante recordar que estas operaciones se realizar�n en todos los participantes que hayan sido seleccionados. Esto significa que tiene que ser muy cuidadoso, especialmente cuando se eliminen grupos de participantes.







