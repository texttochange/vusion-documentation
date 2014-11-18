API Participant
------------------

Create
=======
Add a participant who is optin. The optin date is set at the time the function is called.

**Action URL**
::
	… /programParticipants/add ...

**Mandatory Parameters**

* *phone* (String) the phone number of the new participant. The phone number MUST have it’s international prefix. The + or 00 or 0 prefix are not necessary. Example 25673453213 (256 being Uganda’s prefix) is correct. The other example 73453213 is not correct as the international prefix is missing.

**Optional Parameters**
* *tags* the tags to be set for this participant. Tags are separated by comma. This field can be present multiple time to define multiple tags.
* *profile* a labels to be set for this participant. The format of label are “[label_name]:[label_value]” for example “name:Sandra”

**Note about validation**

* *tags* have to comply to the following regular expression /^[a-z0-9A-Z\s]+$/
* *labels* have to comply to the following regular expression /^[a-z0-9A-Z\s]+:[a-z0-9A-Z\s\.]+$/

Example of parameters of the request

========== =======================================
Keys       Values
========== =======================================
phone      25673453213
tags       farmer, top user
profile    gender:female, name:Olivia, age: 29.5
========== =======================================

**Response**
In case the action is successful, a response is provided containing the phone number of this participant.
::
	{
	    "status": "ok",
	    "phone": "+25673453213"
	}

In case the phone number is already created, the error response will be
::
	{
	    "status": "fail",
	    "message": "The participant could not be saved.",
	    "validation-errors": {
	        "phone": [
	            "This phone number already exists in the participant list."
	        ]
	    }
	}
 

Edit
======

**Action URL**
::
	… /programParticipants/edit ...

**Mandatory Parameters**

* *phone* the phone number of the participant to edit

**Optional Parameters**

The same parameters apply than Creating Participant action

**Response**
In case the phone number belong to a participant, the same responses Creating Participant action. 

Optin
=======
Optin a participant who is Optout WON’T modify the tags and profile information of this participant.  

**Action URL**
::
	… /programParticipants/optin ...

**Mandatory Parameters**

* *phone* the phone number of the participant

**Response**

In case the action is successful, the regular response is provided.

Optout
========
Once a participant is optout, vusion will stop sending any message to this participant. The participant can at any time be Optin again. 

**Action URL**
:: 
	… /programParticipants/optout ...

**Mandatory Parameters**

* *phone* the phone number of the participant

**Response**

In case the action is successful, the regular response is provided.


Run Actions
============

This call run actions associate with an question interaction (closed/open question or multi-keywords).

**Action URL**
::
	… /programParticipants/runActions ...

**Mandatory Parameters**

* *phone* the phone number of the participant
* *dialogue-id* the id of the dialogue
* *interaction-id* the id of the interaction
* *answer* the answer to be consider to the interaction (this should not include any KEYWORD)

**Response**
A validation is run on all the parameters, if the phone, dialogue-id, interaction-id or answer is not existing in the program, a validation error will be returned.