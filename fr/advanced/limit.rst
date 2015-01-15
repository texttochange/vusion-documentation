:index:`Fonction de limite`
+++++++++++++++++++++++

Général
-----------

La fonction de limite est un outil pour limiter la durée d'un programme et le nombre de messages générés par un programme. La limite est fixée à la page des paramètres du programme. Sélectionnez d'abord si seuls les messages sortants doivent être comptés ou entrant et sortant. Dans le domaine de la limite totale entrez le nombre maximal de messages autorisés. Dans les champs ci-dessous début et la fin de la date du programme peut être réglé. Lorsque ceux-ci sont définis, le programme ne sera pas envoyer des messages à l'extérieur de cette période.

Seulement gestionnaire et les niveaux d'utilisation plus élevés sont autorisés à modifier les paramètres de limites. Les autres utilisateurs peuvent afficher les paramètres mais ne peut pas les changer.

Scenarios
----------
* 	Quelqu'un optein et est censé obtenir deux messages retours. Vous n'avez qu'un seul crédit. Le premier message est envoyé, le second ne sera pas.

	L'historique montrera un statut de non-crédit. Si vous réglez la limite de 50 messages plus, le message ne ​​sera pas envoyé par la suite. Vous aurez besoin de reprogrammer le message.



* 	Un message entrant attend une réponse, mais le programme n'a pas encore commencé, ou il a déjà terminé. Dans ce cas, le message sortant obtient un statut de non-crédit planifié et ne sera pas envoyé.

**Note:** Dans les deux cas, les messages rejetés ne seront pas reportées automatiquement. Lorsque, à un moment, il ya plus de crédits disponibles, ou lorsque tout d'un coup le programme n'atteint les délais impartis, les messages rejetés ne seront pas renvoyés.

