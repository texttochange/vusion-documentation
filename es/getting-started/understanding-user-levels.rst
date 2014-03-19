Entendiendo lo niveles de Usuario
##################################

VUSION provee diferentes niveles de usuarios. Cada usuario tiene 1 nivel de ususario asignado. Este artículo describe brevemente los varios niveles de ususario.

Primero una visión general de los niveles. Una columna importante es *Acceso a TODOS los programas*. Esta columna indica cierto rol que permite a los usuarios tener acceso a todos los programas activos en el sistema o no. Los niveles de usuario que no tengan acceso a todos los programas solamente tendrán acceso a un programa si el administrador se lo concede explicitamente. Esto significa que cuando dicho usuario inicia sesión, solamente podrá ver los programas a los cuales tenga acceso, y ninguno de los otros programas disponibles en el sistema.

=============================  =================================== ============================ ===============  =============================  =========================  ===============  =========
Level                          Modificar usuarios & códigos cortos Acceso a TODOS los programas Crear programas  Modificar lógoca del programa  Administrar Participantes  Enviar Mensajes  Ver Datos
-----------------------------  ----------------------------------- ---------------------------- ---------------  -----------------------------  -------------------------  ---------------  ---------
**Súper administrador**                           ✔                             ✔                      ✔                      ✔                           ✔                   ✔               ✔  
-----------------------------  ----------------------------------- ---------------------------- ---------------  -----------------------------  -------------------------  ---------------  ---------
**Manager**                                       ✘                             ✔                      ✔                      ✔                           ✔                   ✔               ✔  
-----------------------------  ----------------------------------- ---------------------------- ---------------  -----------------------------  -------------------------  ---------------  ---------
**Administrador de Programa**                     ✘                             ✘                      ✘                      ✔                           ✔                   ✔               ✔  
-----------------------------  ----------------------------------- ---------------------------- ---------------  -----------------------------  -------------------------  ---------------  ---------
**Administrador Socio**                           ✘                             ✘                      ✘                      ✘                           ✔                   ✔               ✔  
-----------------------------  ----------------------------------- ---------------------------- ---------------  -----------------------------  -------------------------  ---------------  ---------
**Socio**                                         ✘                             ✘                      ✘                      ✘                           ✘                   ✘               ✔  
=============================  =================================== ============================ ===============  =============================  =========================  ===============  =========

Ahora veremos cada nivel con un poco más de detalle.


Súper Administrador
====================

Tiene acceso a todo. Hay muy pocos usuarios con este nivel de acceso. Este nivel de acceso es especialmente importante para crear, modificar y eliminar usuarios del sistema. Este usuario también puede modificar códigos cortos y su configuración asociada. 

En el contexto de un multi-usuario, un sistema de despliegue multi-país de la organización que será responsable de la administración, funcionamiento y mantenimiento del sistema. 

Manager
=================
Este ususario no puede modificar otros usuarios o códigos cortos pero tiene acceso a todas las otras partes del sistema. Este nivel de ususario es especialmente útil para crear nuevos programas y administrar los programas existentes en el sistema, ya que un manager tiene acceso a todos los programas en el sistema.

Administrador de Programa
===========================
Este usuario puede hacer todo *dentro* de un programa. Cambair la lógica, enviar mensajes, administrar participantes, etc. Sin embargo, un usuario de este nivel solo podrá hacer en el programa hasta donde se le de acceso, ya que este usuario no tiene acceso a todos los programas en el sistema.

Administrador Socio
====================
Este usuario solo puede ver los datos de uno o más programas específicos a los cuales tiene acceso explícito. En estos programas puede enviar mensajes y administrar participantes. Sin embargo, *no* puede cambiar la lógica del programa, por ejemplo: diálogos o solicitudes.

Socio
=======
Un socio solo puede ver los datos de uno o más programas específicos a los cuales tiene acceso explícito. Este nivel de usuario es útil para monitorear el progreso de un programa.

