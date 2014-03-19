Contenido de Variables (Content Variables)
==========================================

Cuando se seleccione Contenido de Variables en el Men� de Navegaci�n, se puede editar contenido din�mico.
La interface aparece con dos campos en la versi�n actual. Key y Values.

La key (llave) es el nombre de su contenido din�mico, por ejemplo 'Temperatura'. El value (valor) es el contenido espec�fico, por ejemplo 10 grados.
Cuando quiera acceder a este contenido en un mensaje, respuesta o di�logo escriba de la siguiente forma:

*[contentVariable.key]*

En este caso en particular se escribir�a:

*[contentVariable.Temperature]*.

**Precausi�n**

Preste atenci�n a las may�sculas y min�sculas del contentVariable. Ya que si no se escribe correctamente no funcionar�.
La key tambi�n es sensible a la diferencia entre may�sculas y min�sculas, por lo cual si se escribe 'temperatura' en lugar de 'Temperatura' el mensaje no ser� entregado. 


Variable Participante
======================

Cuando los participantes ya fueron etiquetados (tienen una label), esto tambi�n puede ser usado en un mensaje.
Por ejemplo si los participantes tienen una etiqueta (label): Nombre y quiere saludarlos de forma personal, podr�a escribir de la siguiente forma:

*Hola [participant.Nombre]*

Si el participante no tiene una etiqueta (label) denominada 'Nombre' el mensaje no ser� enviado. Puede verificar esto en el Historial f�cilmente, mostrar� 'missing-date' (datos faltantes) debajo del estatus del mensaje.

