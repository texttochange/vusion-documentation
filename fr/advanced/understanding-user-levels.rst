Understanding :index:`user levels`
###################################

VUSION fournit différents niveaux d'utilisateurs. Chaque utilisateur a le niveau 1 de l'utilisateur qui leur est assigné. Cet article décrit brièvement les différents niveaux d'utilisateurs.

D'abord, un aperçu de haut niveau de différents niveaux. Une importante colonne est l'accès à tous les programmes. Cette colonne indique si un certain rôle permet aux utilisateurs d'avoir accès à tous les programmes actifs dans le système ou non. Niveaux d'utilisateurs qui n'ont pas accès à tous les programmes ne pourront avoir accès à des programmes si un administrateur qu'il a accordée à leur explicitement. Cela signifie que quand un tel utilisateur se connecte, il ou elle ne verra que les programmes qu'il ou elle a accès, et aucun des autres programmes qui sont disponibles dans le système.

=========================  ===================================== ============================= ====================  ================================  ======================  ====================  ================
Level                      Modifier utilisateurs & numéro courts Accéder à tous les programmes Créer les programmes  Modifierxlesxprogrammesxlogiques  Gérer les participants  Envoyer des messages  Voir les données
-------------------------  ------------------------------------- ----------------------------- --------------------  --------------------------------  ----------------------  --------------------  ----------------
**Administrateur**         ✔                                                       ✔                                          ✔                                                 ✔                                                 ✔                                 ✔                               ✔  
-------------------------  ------------------------------------- ----------------------------- --------------------  --------------------------------  ----------------------  --------------------  ----------------
**Manageur**               ✘                                                       ✔                                          ✔                                                 ✔                                                 ✔                                 ✔                               ✔ 
-------------------------  ------------------------------------- ----------------------------- --------------------  --------------------------------  ----------------------  --------------------  ----------------
**Manageur de programme**  ✘                                                       ✘                                          ✘                                                 ✔                                                 ✔                                 ✔                               ✔ 
-------------------------  ------------------------------------- ----------------------------- --------------------  --------------------------------  ----------------------  --------------------  ----------------
**Partenaire manageur**    ✘                                                       ✘                                          ✘                                                 ✘                                                 ✔                                 ✔                               ✔ 
-------------------------  ------------------------------------- ----------------------------- --------------------  --------------------------------  ----------------------  --------------------  ----------------
**Partenaire**             ✘                                                       ✘                                          ✘                                                 ✘                                                 ✘                                 ✘                               ✔ 
=========================  ===================================== ============================= ====================  ================================  ======================  ====================  ================

Maintenant, nous allons discuter des différents niveaux d'utilisateurs en un peu plus en détail.


:index:`Administrateur`
=======================

L'administrateur est l'utilisateur avec accès à tout. Il n'y a que très peu d'utilisateurs avec ce niveau d'accès. Ce niveau d'accès est particulièrement important pour créer, modifier et supprimer des utilisateurs du système. En outre, cet utilisateur peut modifier numéros courts et leurs paramètres associés.

Dans le cadre d'un multi-utilisateurs, le déploiement du système multi-pays ce seront les administrateurs système à l'entreprise ou l'organisation qui est responsable de la gestion et la maintenance du système.

:index:`Gestionnaire`
=================
Cet utilisateur ne peut pas modifier les utilisateurs ou les numéros courts mais a accès à toutes les autres parties du système. Ce rôle d'utilisateur est particulièrement utile pour créer de nouveaux programmes et la gestion de tous les programmes existants dans le système, car un gestionnaire a accès à tous les programmes du système.

:index:`Gestionnaire de programme`
=========================
Le nom dit tout. Cet utilisateur peut tout faire à l'intérieur d'un programme. Changer la logique, envoyer des messages, gestion des participants, etc. Toutefois, un utilisateur à ce niveau ne sera en mesure de le faire pour les programmes qu'il a accès, depuis cet utilisateur n'aura pas accès à tous les programmes du système.

:index:`Partenaire Manager`
==========================
Le partenaire manager a seulement accès à un ou plusieurs programmes auxquels ils ont accès explicite. Au sein de ces programmes (s) il peut envoyer des messages distincts et gestion des participants. Toutefois, le gestionnaire de partenaire n'est pas en mesure de changer tout de la logique du programme, à savoir; dialogues ou des requêtes.

:index:`Partenaire`
===================
Un partenaire ne peut afficher les données d'un ou plusieurs programmes spécifiques auxquels ils ont accès explicite. Ce niveau d'utilisateur est utile pour l'avancement du programme de surveillance.

