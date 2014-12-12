:index:`Contenu variable / dynamique`
---------------------------

Le contenu de variables vise à être utilisé pour le message de personnalisation. Il permet de modifier le contenu des messages MT que de modifier le contenu de la variable utilisée. Les variables de contenu sont réutilisables sur la totalité programme: Demande, un message séparé, dialogue, ...

Il ya 2 type de contenu de variable:

* **clé/valeur** une paire clé-valeur simple
* **Un tableau** a deux dimensions, il ressemble à une feuille Excel.

Clé / valeur
==========
La clé est le nom du contenu, par exemple «température». La valeur est le contenu réel, afin pour un exemple de 10 degrés.

Exemple de paire clé / valeur:

==============  ========
Clé             Valeur
==============  ======== 
Température     25C
Prix du poulet  300KES
...            ...
==============  ========

Si vous souhaitez accéder au contenu de la variable dans une Requête/ Dialogue / Message séparé, le contenu du message utilise la syntaxe suivante:
::
	"Hello [contentVariable.<key>]

**Caution**

Faites attention à la capitalisation des contenu/Variable. Si d'autres lettres majuscules sont appliquées, il ne fonctionnera pas. La clé est aussi une case sensible, donc si vous utilisez «Température» au lieu de «température» le message ne ​​sera pas livré.

Voir plus sur un  :doc:`message de personnalisation </advanced/message_customisation>`

Tableau
==========

Dans le cas du tableau, on peut stocker un Excel comme un tableau. La colonne de droite et la rangée supérieure étant les touches pour accéder aux valeurs.

Example
======= ==================
Item    prix de l’article
======= ==================
poulet  300KES
poisson 200KES
======= ==================

Pour l'utiliser, personnaliser un message, on peut utiliser:
::
	"Hello today price of fish is [contentVariable.fish.price]"

Voir plus sur un  :doc:`message de personnalisation </advanced/message_customisation>`




