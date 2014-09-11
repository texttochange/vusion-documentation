:index:`Proportional Tagging`
+++++++++++++++++++++++++++++++

Proportional tagging is a feature that enables participants to be automatically assigned to different groups by tagging them with different tags.

This feature can be useful to compare group reaction to different set of information. 
Indeed when participants have been tagged, you could auto-enrol them in different dialogues.

If participants are to be distributed equally to all groups, all weights should be set to one.
It is also possible to distribute them unequally.
By setting different weights to different groups you can put for instance 1 in 4 participants in a group, while the rest goes in the other group. 

:warning:
	The distribution will take into account ALL participants (optin and optout) who have been tagged with one of the tag.


Scenario's
-----------

If you want to create 2 equal groups, for instance if you want to try two different methods of questioning, create two proportional tags, **group 1** and **group 2**, both with weight 1.
This will result in an even spread of the participants among the two groups. 
The result will be:


==================   =========   =========
Total population     Group 1     Group 2
==================   =========   =========
10                   5           5
==================   =========   =========



In a different scenario you might want to select 20% of participants to win a prize.
In this case, create a proportional tag called **winner** with a weigth of 1 and a proportional tag with a weight of 4 called **not winner**.
Now for every participant tagged as winner, four will be tagged as not winner, resulting in:

==================   =========   ===========
Total population     Winner      Not winner
==================   =========   ===========
10                   2           8
==================   =========   ===========


It is also possible to use proportional tagging to create more then 2 different groups. To do this, just add more then 2 proportional tags.
If you want to distribute participants equally, give the proportional tags the same weights.
You can also use the weights to make different distributions.

Proportional Tagging vs Labelling
----------------------------------
Both proportional tagging and :doc:`proportional labelling </advanced/proportional_labelling>` allow to group participants. 
However proportional labelling is recommanded as it ease the monitoring of the program overtime. 