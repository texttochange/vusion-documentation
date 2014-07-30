API Separate Message
-----------------

Create
=========

**Action URL**
::
	… /programUnattachedMessages/add ...

**Mandatory Parameters**

* *content* (String) the message content
* *send-to-type* (String) the type of sending. Possible values: all, phone, match.
* *type-schedule* (String) the scheduling type. Possible values: immediately, fixed-time

*only for send-to-type=phone*

* *send-to-phone* (Array) the list of phone number to be send to as an array of phone number with the international prefix such as '256701601398' for a Ugandan number. If the phone number is not present in the participant list, a new participant will be created.

THERE IS NO VALIDATION THAT THE LISTED PHONE NUMBERS ARE OPTIN. //add more

Example, to send a message to a list of participants, the request parameter should be: 

================   ============
Keys               Values
================   ============
content            Hello guys!
send-to-type       phone
send-to-phone[0]   256788601461
send-to-phone[1]   256788601462
type-schedule      immediately 
=================  =============


*only for send-to-type=match*

* *send-to-match-operator* (String) the operator between the conditions. Possible value: all, any
* *send-to-match-conditions* (Array) a condition in terms of participant’s tags or labels. This field can be present multiple time to specify multiple conditions

Example, to send a message to participants with tag FISHERMAN or with label gender equal to Male, the request parameter should be: 

============================ =================
Keys                         Values
============================ =================
content                      Hello guys!
send-to-type                 match
send-to-match-operator       any
send-to-match-conditions[0]  FISHERMAN
send-to-match-conditions[1]  gender:Male
type-schedule                immediately
============================ ==================

  
**Optional parameters**

* *name* a unique name for this message. If not defined, Vision will generate a name from the content and the scheduled time of the message.
* *fixed-time* date/time at which the message should be send in the timezone of the program. The date/time format is ISO such as 2013-11-20T20:08:05. This will result in scheduling the message for the future date/time. This this field is not provide, the message will be send immediately.

**Response**

In case the action is successful, the following fields will be provided: name and id.
::
	{
	    "status":"ok",
	    "id":"53be9860e9cea51b505f8ee3",
	    "name":"10\/07\/2014 16:42:56 Hello"
	}


In case the action has failed, the body of the response will contain the field: validationErrors.
::
	{
	    "status": "fail",
	    "message": "The Message could not be saved.",
	    "validation-errors": {
	        "send-to-type": [
	            "Send To option not allowed."
	        ]    }
	}
