Message Customisation
---------------------

The idea behind message customisation is to define a message that will be customized for the participant at the time it is send to him.
For example, i want to send a customized welcome message to all my participant with their name.

One need to only create a separate message with the content
::
	"Hello [participant.name]"

So that each participant will receive:
:: 
	"Hello Olivier"


There are 4 type of message customisation that we call *domain*: 

#. Content Variable
#. Participant
#. Time
#. Context


Content Variable
=================
You can use all the content variables defined in the program to customize your message. A missing content variable will result in an error and the message will not send. An error will appear in the program's history.**

**key/value**

* *[contentVariable.<key>]* will retrun the value of this key.

So if content variable 'Temperature' is equal to '26C',
::
	"Hello today [contentVariable.Temperature]" 

will become
::
	"Hello today it's [contentVariable.Temperature]".

**table**

* *[contentVariable.<key1>.<key2>]* will retrun the value associate this key1 and key2.
 

In the case of table, each value has 2 keys. So if a content variable table is 

======= ======
Item    Price
======= ======
chicken 300KES
fish    200KES
======= ======

So the content:
::
	"Hello today price of fish is [contentVariable.fish.price]"

will become:
::
	"Hello today price of fish is 200KES"

	

Participant
============
When participants have a label this can also be used in a message.
If participants for example have a label Name and you want to greet them use the following syntax
::
	"Hello [participant.name]"

will be customized as
::
	"Hello olivier"   // depending of each participant value for 'name'

If the participant does not have a label called 'name' the message will not be sent. You can easily see this in the program history, it will show missing-date under status of the message.


Time
=====
Time will give you access to the time at which the SMS is send in the program defined timezone.

* *[time.H]* will show the hour the participant sent the Alert message.
* *[time.M]* will show the minutes the participant sent the Alert message.
* *[time.d]* will show the day of the month in number the participant sent the Alert message.
* *[time.m]* will show the month of the year in number the participant sent the Alert message.
* *[time.y]* will show the year without century.


Context
========
Context is only avalable when triggered by an incoming sms. For example in a Request or in a Dialogue answer. However it's not available within a Separate Message or a Dialogue Announcement.

Currently context is only use with "message".

**[context.message] notation**

An evolved notation is available in order to manipulate easily the incoming message.

One wants to only use a certain word of the message.

* *[context.message.1]* will show the 1st word of the message
* *[context.message.2]* will show the 2nd word of the message

One wants to show the message except the 1st or the second word

* *[context.message.after.1]* will show the all message except the first word
* *[context.message.after.2]* will show the all message except the 2 first word

Let's take the example of a action SMS Forwaring. One want to forward the message from the initial sender without the keyword.
::
	"[participant.phone] sent: [context.message.after.1]"

so if the initial message from +2568473262 is "Doctor i'm sick"
::
	"+2568473262 sent: i'm sick"