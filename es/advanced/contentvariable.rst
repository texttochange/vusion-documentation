Contenido de Variables (Content Variables)
==========================================

Cuando se seleccione Contenido de Variables en el Menú de Navegación, se puede editar contenido dinámico.
La interface aparece con dos campos en la versión actual. Key y Values.

La key (llave) es el nombre de su contenido dinámico, por ejemplo 'Temperatura'. El value (valor) es el contenido específico, por ejemplo 10 grados.
Cuando quiera acceder a este contenido en un mensaje, respuesta o diálogo escriba de la siguiente forma:

*[contentVariable.key]*

En este caso en particular se escribiría:

*[contentVariable.Temperature]*.

**Precausión**

Preste atención a las mayúsculas y minúsculas del contentVariable. Ya que si no se escribe correctamente no funcionará.
La key también es sensible a la diferencia entre mayúsculas y minúsculas, por lo cual si se escribe 'temperatura' en lugar de 'Temperatura' el mensaje no será entregado. 


Variable Participante
======================

Cuando los participantes ya fueron etiquetados (tienen una label), esto también puede ser usado en un mensaje.
Por ejemplo si los participantes tienen una etiqueta (label): Nombre y quiere saludarlos de forma personal, podría escribir de la siguiente forma:

*Hola [participant.Nombre]*

Si el participante no tiene una etiqueta (label) denominada 'Nombre' el mensaje no será enviado. Puede verificar esto en el Historial fácilmente, mostrará 'missing-date' (datos faltantes) debajo del estatus del mensaje.

