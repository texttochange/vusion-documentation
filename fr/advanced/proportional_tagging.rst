:index:`Tagging proportionnel`
+++++++++++++++++++++++++++++++

Tagging proportionnel est une fonctionnalité qui permet aux participants d'être automatiquement attribués aux différents groupes en les taggant avec des tags différents. 

Si les participants sont répartis de manière égale à tous les groupes, tous les poids devraient être fixés à un. Il est également possible de les répartir inégalement. 

En fixant des poids différents à différents groupes, vous pouvez mettre par exemple 1 à 4 participants dans un groupe, tandis que le reste va dans l'autre groupe.




Scenario
-----------

Si vous voulez créer deux groupes égaux, par exemple si vous voulez essayer deux méthodes différentes de questionnement, on crée deux tags proportionnels, "groupe 1" et "2" groupe, à la fois avec un poids 1 Cela se traduira par une répartition équilibrée de les participants entre les deux groupes. Le résultat sera le suivant :


==================   =========   =========
Total population     Group 1     Group 2
==================   =========   =========
10                   5           5
==================   =========   =========



Dans un scénario différent, vous voudrez peut-être sélectionner 20% des participants de gagner un prix. Dans ce cas, on crée un tag proportionnel appelé **gagnant** avec un Poids de 1 et un tag proportionnel, avec un poids de 4 appelé **pas gagnant**. Maintenant, pour chaque participant taggé comme gagnant, quatre seront taggés comme non gagnant, ce qui entraîne:

==================   =========   ===========
Total population     Gagnant     Non Gagnant
==================   =========   ===========
10                   2           8
==================   =========   ===========


 Il est également possible d'utiliser le tag proportionnel pour créer plus de deux groupes différents. Pour ce faire, il suffit d'ajouter plus de 2 tags proportionnels. Si vous souhaitez distribuer les participants aussi, donner les tags proportionnels les mêmes poids. Vous pouvez également utiliser des poids pour faire différentes distributions.


