Sms farwarding
##############
When selecting action sms forward radio button from the list of actions. An interface comes up with two fields as shown below:
 
.. image:: _static/img/smsforwarding_action.png

**Receiver Tag:** 
In this textarea you enter the tag for participant in your program who are ment to receive the Alert message.

**Content:** 
In this textarea you enter the message format the tagged participants will receive when an alert is sent by participant.

ie
----

"Hello **[participant.name]** (**[participant.phone]**) at **[participant.address]** say **[context.message]** at **[time.H]**:**[time.M]**"

Here **[participant.name]**      will show the name of the participant sending the Alert message.


     **[participant.phone]**     will show the phone number of the participant sending the Alert message.
     
     
     **[participant.address]**   will show the address of the participant sending the Alert message.
     
     
     **[context.message]**       will show the message context sent by the participant.
     
     
     **[time.H]**                will show the hour the participant sent the Alert message.
     
     
     **[time.M]**                will show the minutes the participant sent the Alert message.
     
consider the use case  in the image  below:

.. image:: _static/img/smsforwarding_use_case.jpg




