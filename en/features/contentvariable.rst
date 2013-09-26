Content variable
===========================

When selecting Content Variables in the left menu dynamic content can be edited.
The interface comes up with two fields in the current version. Key and Value.

The key is the name of your dynamic content, for example 'Temperature'. The value is the actual content, so for example 10 degrees.
When you want to access this content in a message, reply, dialogue use the following syntax:

*[contentVariable.key]*

So in this case that would come down to

*[contentVariable.Temperature]*.

**Caution**

Pay attention to the capitalization of contentVariable. If other capital letters are applied it won't work.
The key is also capitol sensitive, so if you use 'temperature' in stead of 'Temperature' the message will not be delivered. 


Participant variable
=================================

When participants have a label this can also be used in a message.
If participants for example have a label Name and you want to greet them use the following syntax

*Hello [participant.name]*

If the participant does not have a label called 'name' the message will not be sent. You can easily see this in the program history, it will show missing-date under status of the message.

