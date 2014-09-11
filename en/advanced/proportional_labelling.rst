:index:`Proportional Labelling`
+++++++++++++++++++++++++++++++

Proportional Labelling is a feature that enables participants to be automatically assigned to different groups by labelling them with different label value.

This feature can be useful to compare group reaction to different set of information. 
Indeed when participants have been labelled, you could auto-enrol them in different dialogues.

If participants are to be distributed equally to all groups, all weights should be set to 1. 
It is also possible to distribute them unequally. 
By setting different weights to different groups you can put for instance 1 in 4 participants in a group, while the rest goes in the other group.

:warning:
	The distribution will take into account ALL participants (optin and optout) who have been labelled with one of the label:value.


Scenario's
-----------

If you want to create 2 equal groups, in order to assess two different methods of questioning.
First create a *label name* as **group** then add two proportional labels: **A** and **B**, both with weight 1.
This will result in an even spread of the participants among the two groups. 
The result will be:


==================   =========   =========
Total population     group:A     group:B
==================   =========   =========
10                   5           5
==================   =========   =========



In a different scenario you might want to select 20% of participants to win a prize.
In this case, create a label named **draw**. 
The value of this label can be **won** with a weigth of 1 and a proportional label with a weight of 4 the value **lost**.
Now for every participant tagged as winner, four will be tagged as not winner, resulting in:

==================   =========   ===========
Total population     draw:won    draw:lost
==================   =========   ===========
10                   2           8
==================   =========   ===========


It is also possible to use proportional labeling to create more then 2 different groups.
To do this, just add more then 2 proportional labels.
If you want to distribute participants equally, give the proportional labels the same weights.
You can also use the weights to make different distributions.


Proportional Labelling vs Tagging
----------------------------------
Both proportional labelling and :doc:`proportional tagging </advanced/proportional_tagging>` allow to group participants. 
However proportional labelling is recommanded as it ease the monitoring of the program overtime. 

