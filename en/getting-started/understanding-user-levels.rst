Understanding user levels
#########################

VUSION provides different user levels. Each user has 1 user level assigned to them. This article briefly describes the various user levels.

First a high level overview of the various levels. An important column is *access to ALL programs*. This column indicates if a certain role allows users to have access to all programs active in the system or not. User levels that do not have access to all programs will only have access to programs if an administrator has granted it to them explicity. This means that when such a user logs in, he or she will only see the programs that he or she has access to, and none of the other programs that are available in the system.

=======================  ========================= ====================== ===============  ====================  ===================  =============  =========
Level                    Modify users & shortcodes Access to ALL programs Create programs  Modify program logic  Manage participants  Send messages  View Data
-----------------------  ------------------------- ---------------------- ---------------  --------------------  -------------------  -------------  ---------
**administrator**           ✔                        ✔                       ✔                ✔                     ✔                   ✔             ✔  
-----------------------  ------------------------- ---------------------- ---------------  --------------------  -------------------  -------------  ---------
**manager**                  ✘                        ✔                       ✔                ✔                     ✔                   ✔             ✔  
-----------------------  ------------------------- ---------------------- ---------------  --------------------  -------------------  -------------  ---------
**program manager**           ✘                        ✘                       ✘                ✔                     ✔                   ✔             ✔  
-----------------------  ------------------------- ---------------------- ---------------  --------------------  -------------------  -------------  ---------
**partner manager**        ✘                        ✘                       ✘                ✘                     ✔                   ✔             ✔  
-----------------------  ------------------------- ---------------------- ---------------  --------------------  -------------------  -------------  ---------
**partner**                  ✘                        ✘                       ✘                ✘                     ✘                   ✘             ✔  
=======================  ========================= ====================== ===============  ====================  ===================  =============  =========

Now we will discuss the different user levels in a bit more detail.


Administrator
=================

The administrator is the user with access to everything. There are only very few users with this access level. This access level is especially important for creating, modifying and deleting users of the system. Also, this user can modify shortcodes and their associated settings. 

In the context of a multi-user, multi-country system deployment this will be the system administrators at the company or organisation that is responsible for running and maintaining the system.

Manager
=================
This user cannot modify users or shortcodes but has access to all other parts of the system. This user role is especially useful for creating new programs and managing all existing programs in the system, since a manager has access to all programs in the system.

Program manager
================
The name says it all. This user can do everything *inside* a program. Change the logic, send messages, manage participants, etcetera. However, a user on this level will only be able to do so for the programs he has access to, since this user will not have access to all programs in the system.

Partner manager
=================
The parner manager has only access to one or more specific programs to which they have explicit access. Within these programs (s)he can send separate messages and manage participants. However, the partner manager is *not* able to change any of the program logic, ie; dialogues or requests.

Partner
=======
A partner can only view data of one or more specific programs to which they have explicit access. This user level is useful for monitoring program progress.

