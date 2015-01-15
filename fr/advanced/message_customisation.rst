Personnalisation de message
----------------------------

L'idée derrière le message de personnalisation est de définir un message qui sera adaptée pour le participant au moment où il est envoyé à lui. Par exemple, je veux envoyer un message de bienvenue personnalisé pour tout participant avec leur nom.

Un besoin de créer seulement un message séparé avec le contenu
::
	"Hello [participant.name]"

De sorte que chaque participant recevra:
:: 
	"Hello Olivier"


Il ya 4 type de message personnalisable que nous appelons *domaine*: 

#. Contenu de variable
#. Participant
#. Temps
#. Contexte


Contenu dynamique
=================
Vous pouvez utiliser toutes les variables de contenu définis dans le programme pour personnaliser votre message. Une variable contenu manquant entraînera une erreur et le message ne sera pas envoyé. Une erreur apparaît dans l'historique du programme.**

**Clé/Valeur**

* *[contentVariable.<key>]* will retrun the value of this key.

Donc si la variable contenu 'température' est égale à '26C',
::
	"Hello today [contentVariable.Temperature]" 

Ce sera :
::
	"Hello today it's [contentVariable.Temperature]".

**Tableau**

* *[contentVariable.<key1>.<key2>]* will return the value associate this key1 and key2.
 

Dans le cas de la table, chaque valeur dispose de 2 touches. Donc, si un contenu table des variables est :

======= ======
Item    Price
======= ======
chicken 300KES
fish    200KES
======= ======

Ainsi, le contenu:
::
	"Hello today price of fish is [contentVariable.fish.price]"

deviendra:
::
	"Hello today price of fish is 200KES"

	

Participant
============
Lorsque les participants ont un tag cela peut aussi être utilisé dans un message. Si les participants ont par exemple un label Nom et que vous voulez saluer utilisent la syntaxe suivantes :
::
	"Hello [participant.name]"

sera personnalisé comme :
::
	"Hello olivier"   // depending of each participant value for 'name'

Si le participant n'a pas de label appelé «nom» le message ne ​​sera pas envoyé. Vous pouvez facilement voir dans l'historique du programme, il affiche manquant jour sous le statut du message.


Temps
=====
Temps vous donnera accès à l'heure à laquelle le SMS est envoyé dans le programme défini le fuseau horaire.

* *[time.H]* affichera l'heure le participant a envoyé le message d'alerte.
* *[time.M]* affiche les minutes, le participant a envoyé le message d'alerte.
* *[time.d]* affiche le jour du mois en nombre le participant a envoyé le message d'alerte.
* *[time.m]* affichera le mois de l'année en nombre le participant a envoyé le message d'alerte.
* *[time.y]* affichera l'année sans le siècle.


Contexte
========
Le contexte est seulement valable quand il est déclenché par un SMS entrant. Par exemple, dans une demande ou à une réponse de dialogue. Cependant, il n'est pas disponible dans un message séparé ou une annonce de dialogue.

Actuellement le contexte est utilisé uniquement avec "message".

**[context.message] notation**

Une notation évoluée est disponible afin de manipuler facilement le message entrant.

**Un seul mot**

On veut utiliser seulement un certain mot du message.

* *[context.message.1]* va afficher le 1er mot du message
* *[context.message.2]* affichera le 2ème mot du message

Pour illustrer, prenons l'exemple d'un retour de l'action. Envie de transmettre le deuxième mot seulement.
::
	"Welcome [context.message.2]"

si le message initial de +2568473262 est "Nom Olivier"
::
	"Welcome Olivier"

**Jeu de mots: après**

On peut utiliser la notation après d'ajouter tous les mots après une certaine position de mot.

* *[context.message.after.1]* affichera le message de tout à l'exception du premier mot
* *[context.message.after.2]* affichera le message de tout sauf le 2 premier mot

Pour illustrer, prenons l'exemple d'une action de SMS transférée. Envie de transmettre le message de l'expéditeur initial sans le mot clé.
::
	"[participant.phone] sent: [context.message.after.1]"

si le message initial de +2568473262 est "Docteur je suis malade"
::
	"+2568473262 sent: je suis malade"

**Jeu de mots: avant**

On peut utiliser la notation avant d'ajouter tous les mots avant une certaine position de mot.

* *[context.message.before.1]* pour ne rien afficher comme il n'y a rien avant le 1er mot.
* *[context.message.before.2]* affichera le 1 mot du message.

Pour illustrer, prenons l'exemple de SMS avant d'aviser le gestionnaire à chaque fois un médecin répond à un patient.
::
	"Doctor [participant.phone] [context.message.before.3]"

si le message initial de +2568473262 est "Réponse +2561111111 s'il vous plaît venez à la clinique d'urgence"
::
	"Doctor +2568473262 Answer +2561111111"
