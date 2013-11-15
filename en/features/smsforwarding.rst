Sms forwarding
##############

Use Case
----------
Consider following use case: An Organization is setting up a Alert and Rescue service. Participant can request help from the member of this organization simply by sending HELP to a shortcode.
The SMS will be automatically forwarded to different member of the organization who will then make sure someone in the neighborhood will visit urgently this participant. 

The drawing below show how this use case would work.

.. image:: _static/img/smsforwarding_use_case.jpg


**1 :** The participant sends out an Alert message.

**2 :** Vusion create a notification message to all participants who are tagged **Alert**. The message can be customized to include information from the participants, the time or even the Alert message content. 

**3 :** Tagged participants are receiving the notification message.


How To Set a SMS Forward
------------------------

Either in a Request or a Dialogue, you can select the action *SMS Forward* from the list of actions. Two fields appear as shown below:
 
.. image:: _static/img/smsforwarding_action.png

**Receiver Tag:** 
In this textbox, you enter the tag of participant to will receive the message. Please make sure that some partipants are currently opt-in and are tagged with this tag otherwise nobody will be notified.

**Content:** 
In this textarea, you enter the notification message that will be send. For more details on how to customize this message, see the next section.


Notification Message
--------------------

This is an example of notification message. In this example we assume that the send of the alert has been created on the program with 2 label:

#. name:Tom
#. address:3rd av behind city mall mombasa

So with this notification message content:

| "Alert **[participant.name]** (**[participant.phone]**) at **[participant.address]** say '**[context.message]**' at **[time.H]**:**[time.M]**"

* **[participant.name]**      will show the name of the participant sending the Alert message.
* **[participant.phone]**     will show the phone number of the participant sending the Alert message.
* **[participant.address]**   will show the address of the participant sending the Alert message.
* **[context.message]**       will show the message context sent by the participant.
* **[time.H]**                will show the hour the participant sent the Alert message.
* **[time.M]**                will show the minutes the participant sent the Alert message.

if participant sent "Alert help" where "Alert" is the keyword. The participant tagged to receive this message will reveive the message below 
**"Alert Tom (+2567702222) at 3rd av behind city mall mombasa says 'Alert help' at 10:50"**
