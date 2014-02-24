Limit feature
+++++++++++++++

General
-----------

The limit feature is a tool to limit the duration of a program and the amount of messages a program generates. The limit is set in the program settings page. 
First select if only outgoing messages should be counted or both incoming and outgoing. In the Total limit field enter the maximum number of messages allowed. 
In the fields below the program's start and end date can be set. When these are set, the program will not send any messages outside of that time period.

..
	The limit feature is a tool to make sure the limit (amount of messages and time limit) can not be exceeded.
	User levels of manager and higher can configure it. Others can see it but not edit it.

Only manager and higher user levels are allowed to edit limit settings. Other users can view the settings but can not change them.

Scenario's
----------
* 	Someone opts in and is supposed to get 2 messages back. You only have one credit left. The first message will be sent, the second will not.

	History will show a **no-credit** status. If you adjust the limit to 50 messages more, the message will not be send afterwards. You will need to reschedule the message.

..
	* 	Time limit has been reached but there are still credits left; no more messages will be sent. The entire program is **shut down**

* 	An incoming message is expecting a response, but the program has not yet started, or it has already finished. In this case the outgoing message will get a **no-credit-timeframe** status and will not be sent.

**Note:** In both cases the rejected messages will not be automatically rescheduled.  When at some moment there are more credits available, or when all of a sudden the program does reach the allowed timeframe, the rejected messages will not be resent. 

