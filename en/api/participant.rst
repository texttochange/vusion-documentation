API Participant
------------------

Index
=======
To List participants with pagination.

**Method**
GET

**Action URL**
::
    .../programParticipants/index...

**Format**

* json
* csv
* html

**Options Parameters**

* **page** the page number to show, default 1
* **limit** the numnber of participants per page, default 20, maximum 500. For getting more participants at once use ``listParticipants``.
* filter parameters can also be used, documentation todo

Example of request
http://vusion-test.texttchange.org/myprogram/programParticipants/index.csv/page:2/limit:300

listParticipants
=================
To list participants without pagination, ie with an hard coded maximum limit of 10000. For getting more participants, one can use an asynchronous mechanism that is not documented yet.
For each participant, the information will be 1) the phone number, 2) the tags and 3) the profile.


**Method**
GET

**Action URL**
::
    .../programParticipants/listParticipants...

**Format**

* json
* csv

**Options Parameters**

* **explode_profile** the labels that will be extracted from the profile to stand on their own. In case the participant doesn't have such label, the value is an empty string.
* filter parameters can also be used, documentation todo

Example of request
http://vusion-test.texttchange.org/myprogram/programParticipants/listParticipants.csv?explode_profile=age,gender,name
This request will return a csv file with 6 columns: ``phone,tags,profile,age,gender,name``

Create
=======
Add a participant who is optin. The optin date is set at the time the function is called.

**Method**
POST

**Action URL**
::
	… /programParticipants/add ...

**Format**

* json
* html

**Mandatory Parameters**

* *phone* (String) the phone number of the new participant. The phone number MUST have it’s international prefix. The + or 00 or 0 prefix are not necessary. Example 25673453213 (256 being Uganda’s prefix) is correct. The other example 73453213 is not correct as the international prefix is missing.

**Optional Parameters**

* *tags* the tags to be set for this participant. Tags are separated by comma. This field can be present multiple time to define multiple tags.
* *profile* a labels to be set for this participant. The format of label are “[label_name]:[label_value]” for example “name:Sandra”
* *force-optin* (Boolean), the default behavior when creating an already optout participant is a validation error. However with this parameter, the opted out participant will be opted in again without validation error.

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

**Method**
POST

**Action URL**
::
	… /programParticipants/edit ...

**Format**

* json
* html

**Mandatory Parameters**

* *phone* the phone number of the participant to edit

**Optional Parameters**

The same parameters apply than Creating Participant action

**Response**
In case the phone number belong to a participant, the same responses Creating Participant action. 

Optin
=======
Optin a participant who is Optout WON’T modify the tags and profile information of this participant.  

**Method**
POST

**Action URL**
::
	… /programParticipants/optin ...

**Format**

* json
* html

**Mandatory Parameters**

* *phone* the phone number of the participant

**Response**

In case the action is successful, the regular response is provided.

Optout
========
Once a participant is optout, vusion will stop sending any message to this participant. The participant can at any time be Optin again. 

**Method**
POST

**Action URL**
:: 
	… /programParticipants/optout ...

**Format**

* json
* html

**Mandatory Parameters**

* *phone* the phone number of the participant

**Response**

In case the action is successful, the regular response is provided.


Run Actions
============

This call run actions associate with an question interaction (closed/open question or multi-keywords).

**Method**
POST

**Action URL**
::
	... /programParticipants/runActions ...

**Format**

* json
* html

**Mandatory Parameters**

* *phone* the phone number of the participant
* *dialogue-id* the id of the dialogue
* *interaction-id* the id of the interaction
* *answer* the answer to be consider to the interaction (this should not include any KEYWORD)

**Response**
A validation is run on all the parameters, if the phone, dialogue-id, interaction-id or answer is not existing in the program, a validation error will be returned. 
In both case of success or validation error, the response code will be a HTTP 200. The status of the call is indicate by the *status* in the message body.
See below an example of successfull call:
::
    {
        "status": "ok",
        "message": "The runActions succeed.",
        "program-time":"2014-11-24T18:50:04+0300"
    }

See below an example of fail validation on 2 fields the phone number and the interaction-id are incorrect.
::

    {
        "status": "fail",
        "message": "The runActions failed.",
        "program-time": "2014-11-24T21:35:29+0300",
        "validation-errors": {
            "phone": "No participant with phone: +25666666669.",
            "interaction-id": "The dialogue with id 1 doesn't have an interaction with id a494f3dfae6"
        }
    }

