:index:`Requêtes`
++++++++++++++++++

Dans Vusion il ya différentes façons de mettre en œuvre l'interaction avec le participant. Un de ces moyens est le cadre de demandes. Utilisation de demandes est un moyen d'effectuer automatiquement une action quand un message arrive qui contient un certain mot-clé. Lorsque vous configurez une demande de choisir un mot-clé pour correspondre, et vous pouvez également choisir une action que vous souhaitez effectuer Vusion si ce mot clé est reconnu.

Pour gérer les demandes du programme, cliquez sur demande dans le menu du programme. Cela vous mènera à l'écran requête. Ici vous pouvez voir une liste des requêtes actives avec des mots clés, des réponses et des actions. 

.. figure:: _static/img/req_list.png
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

	The Requests screen

Comme vous pouvez le voir, il ya un certain nombre de requêtes actuellement actif. Chaque requête a son propre mot-clé, avec des réponses différentes et différentes actions.


Pour créer une nouvelle demande, cliquez sur le bouton Nouvelle Requête. Ici, vous pouvez ajouter une requête à votre programme. Il ya 3 choses qui doivent être mis en place lors de la création d'une requête.

 1. La requête doit avoir un mot clé unique afin que les messages puissent être reconnus.
 2. La requête peut avoir une ou plusieurs réponses. Une réponse est une réponse automatique quand un message arrive contenant le mot clé.
 3. La requête peut avoir une ou plusieurs actions. Vusion peut faire un certain nombre d'actions, des plus simples comme l'ajout d'un tag à un participant à d'autres plus complexes qui déclenchent des événements ou des messages d'horaire. Les possibilités sont expliquées plus en détail ci-dessous.

L'écran Ajouter requête vous permet de configurer une nouvelle requête.

.. figure:: _static/img/req_add.png
	:width: 800px
	:align: center
	:alt: image19.png
	:figwidth: 800px

	The Add Requests screen, here you can create a new request


Il ya un certain nombre de choses qui doivent être mis en place.

:index:`Mots-clés`
==================

La première chose à mettre en place lors de la création d'une requête est le mot clé. Le mot clé est utilisé comme identifiant. Tous les messages commençant par le mot clé seront traités dans Vusion comme une requête. Afin d'être capable d'identifier correctement et traiter les messages, les mots clés doivent être uniques. Heureusement Vusion vérifie automatiquement si le mot clé que vous souhaitez utiliser est déjà utilisé par une autre requête.

.. note:: 
	Dans Vusion mots-clés ne sont pas sensibles à la casse si le mot-clé STATUS correspondra également au statut. Important à noter est que les mots clés doivent être uniques, non seulement pour le programme, mais pour le shortcode le programme est exécuté. Dans la plupart des pays, il ya seulement un ou deux numéros courts à notre disposition, tandis que nous utilisons beaucoup plus de programmes. Cela signifie différents programmes doivent s'exécuter sur le même numéro court. Vusion assurera toujours que vous n'utilisez pas un mot-clé qui est déjà en cours d'utilisation, mais il est toujours important de garder cet état d'esprit lors de la configuration de Mots-clés.

Pour configurer le mot clé que vous pouvez simplement entrer dans le champ Mot-clé.

La case à cocher en dessous du champ Mot-clé affecte la façon dont certains des messages texte sont adaptés à la mots-clés. Il est très important de comprendre exactement ce qu'il fait que les effets sont assez subtils. Il est à voir si Vusion doit correspondre au mot clé pour le message complet ou seulement le premier mot.


Par exemple: Un gestionnaire de programme est de mettant en place un mot-clé "STATUS" pour un programme.

Cas 1: La case n'est pas cochée Vusion ne correspondra les messages à cette demande qui ne contient que le mot clé. Donc Vusion correspondra le message: 
	
	*Status*

Mais Vusion ne correspondra pas:

	*Status s'il vous plaît, je veux mon état​​!*


Cas 2: La case est cochée Maintenant Vusion essaie d'abord de faire correspondre l'ensemble du message à un mot-clé. Cependant, quand cela échoue, il va essayer de faire correspondre le premier mot du message aux mots-clés. Dans ce cas, Vusion correspondra toujours 

	*Status*

Et il sera également correspondre :

	*Status s'il vous plaît, je veux mon état​​!*

Cette différence dans les deux cas est importante de comprendre. Elle est basée sur la différence entre la totalité du message correspondant à celles d'un premier mot du message. Lors de la mise en place d'une requête, vous devriez soigneusement décider lequel afin de parvenir à un résultat correct.

Lorsque le mot clé a été adapté avec succès, Vusion peut faire deux choses. Envoyer une réponse au participant, et effectuer une action.

:index:`Réponse`
==================

La réponse est utilisée pour répondre automatiquement au participant. Pour ajouter un message de réponse à une demande, cliquez sur le bouton Ajouter de réponse. Une boîte jaune apparaît dans laquelle vous pouvez définir un message qui sera envoyé au participant.

Vous pouvez ajouter plus d'une réponse à une demande en cliquant simplement sur les multiples fois sur le bouton Ajouter de réponse. Vous pouvez supprimer une réponse en cliquant sur le X dans le coin supérieur droit de la boîte de réponse jaune.


:index:`Actions`
==================

Suivant à l'envoi automatique d'une réponse comme expliqué ci-dessus, nous pouvons faire beaucoup plus de demandes. Il est également possible de faire des demandes de déclencher des actions. C'est là que la plate-forme Vusion montre vraiment sa polyvalence et ses possibilités. C'est aussi là que la configuration Vusion se complique, parce que les actions peuvent planifier et déclencher d'autres événements. Il ya beaucoup de différentes actions actuellement mises en œuvre dans Vusion que vous pouvez utiliser.

- **opt-in**: Cela inscrire l'expéditeur en tant que participant du programme. L'expéditeur sera mis dans la base de données des participants. Un participant a opt-in pour Vusion pour pouvoir envoyer des messages aux participants.
- **opt-out**: Cette action annule l'opt-in action décrite ci-dessus. Il mettra l'adhérent dans un état d'opt-out. Les participants qui sont à l'état de l'opt-out ne seront pas recevoir de messages du programme et elles seront de couleur rouge dans l'écran des participants.
- **enroll**:  enrolement: Cette action met le participant dans un dialogue. Pour plus d'informations sur les dialogues, voir :doc:`le guide des Dialogues </advanced/dialogues>`
- **enrolement retardé**: Exécute l'action Inscrivez-avec un retard. Vous pouvez sélectionner un délai d'un certain nombre de jours, et vous pouvez également sélectionner l'heure à laquelle l'inscription doit avoir lieu.
- **tag**: Ajouter un tag pour le participant. Un tag peut être utilisé pour, par exemple, marquer un participant comme propre ou impropre pour le programme.
- **reset**: Effectuez un opt-out suivi d'un opt-in. Il va supprimer toutes les labels et les tags et mettre le participant dans la base de données en tant que participant propre.
- **feedback**: envoie une réponse automatique à l'adhérent. Ceci est très similaire à l'option de réponse.
- **tag proportionnel**: Cela vous donne la possibilité de marquer automatiquement une partie des participants avec un tag et le reste avec un autre tag. Cette fonction est utilisée pour diviser les participants au hasard en groupes, par exemple, si vous voulez prendre 5% de vos participants pour un prix, vous pouvez utiliser l'option tag proportionnel pour marquer ce groupe en tant que gagnant. En savoir plus sur le tag proportionnel dans le :doc:`guide tag proportionnel </advanced/proptag>`

- **url transferé**: Transfère le message entrant une URL. Quand vous faites un projet de collecte de données, le partenaire pourrait vouloir analyser les résultats pour eux-mêmes en temps réel. Utilisation de cette action, les messages seront encore en Vusion mais ils seront également transmis directement à un autre serveur.
- **sms transferé**: Cette action envoie un message SMS à tous les participants avec un certain tag. Le contenu du message peut être généré dynamiquement. Plus d'informations peuvent être trouvées dans le guide de transfert de SMS


Comme vous pouvez le voir, il ya beaucoup d'actions disponibles. En plus de cela, vous pouvez également ajouter plus d'une action à une demande, en fonction de vos besoins. Ajout de plusieurs actions fonctionne de la même manière que l'ajout de plusieurs demandes. Cliquez sur le bouton Ajouter une action va ajouter une autre action à votre demande. Lors de la conception d'une demande, c'est une bonne première étape pour définir exactement ce qui doit se produire lorsque la demande est déclenchée. Si cela est clairement défini, le choix de la combinaison appropriée d'actions devient beaucoup plus facile.
