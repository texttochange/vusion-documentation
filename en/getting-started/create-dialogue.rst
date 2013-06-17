Create Dialogue
###############

Options
--------------

**Has priority**


**Automatic enrollment**
This option will automatically enroll all participants already in the database in this dialogue as well as all the participants
that are newly opted in. **Caution** So as soon as you hit save, the dialogue will start for everyone already in the program.

**Interactions**


Time
-----------

**Fixed time**
This option will send a message at a fixed time, make sure the time-zone matches the time-zone of the country your participants live in. 

**Offset days**
The message will be sent x days after the participant last sended a text. (?)


**Offset time**
The message will be sent x minutes after the participant last sended a text. 

**Answer required**

Different messages
----------------

**Announcement**

An announcement is the easiest option. This contains of a message that will be send to the participant at the programmed time. 




**Question**

A question consists of the content of the question (e.g. What is your gender?) and the keyword.
The keyword enables Vusion to recognize to what question the participant is answering. (e.g. gender)
There are two different kind of questions. An open question and a closed question.

With a closed questions all of the answer options need to be defined. 
You can apply a label to all the replies that are received as answers to this question. (e.g. gender)
If you define the answer male, people will have to respond by texting *gender male*.
So the input from the participants is always of the form: *[keyword] [answer]*.
Continuing you can add a specific feedback or action to the answer.

With an open question you can add a label to the answers and program a feedback that is send to the participants once they have answered this question.
Note that it is not possible to attach actions to open questions.


**Question multi-keyword**
This option comese in handy when there are only two answer options available to your question.
It defines the keyword as the answer option. So when asking what gender someone is they don't have to reply with *gender male* or *gender female* but just with *male* or *female*.


**Other options**


**Set maximum number of accepted unmatching answers**
This option will limit the amount of wrong answers a participant can send back.
When you set this number to 3 for example and the questions is *What age are you? Reply with age [space] yourage* someone who consecutively replies with
* 19
* i am 19 years old
* age 19

will go through. However, if someone answers with 
* 19
* i am 19 years old
* my age is 19
* age 19

Vusion will nog longer register this answer as valid and the participant will no longer receive any messages.
If the participant does not reply with the keyword Vusion will not register this answer as an unmatchable reply since it is not recognized at all.

**No unmatching feedback**
Participants will get no feedback if their reply is not recognized by Vusion.

**Default program unmatching feedback**


**Custom unmatching message**
Here you can configure what message the participants will receive if their reply is not recognized by Vusion.

**Reminder**
This is where you can define reminders for your question. 
You have to define the number of reminders and how long it takes before they are sent. 
It is important to realize that when all the reminders are sent and the participant still has not replied he/she will no longer be able to answer this particular question.
You can bypass this problem by attaching an action 'opt-out' and sending a message that the participant has been opted oud due to failure of answering a question within the designated timeframe.
If he/she still wants to participate in the program he/she has to opt-in again. Other actions can be attached to the reminder function as well.

When *maximum number of accepted unmatching answers* and *reminder* are both configured and one of the *deadlines/limits* is surpassed, the other deadline will automatically expire.














