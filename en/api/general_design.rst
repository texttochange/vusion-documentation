API General Design
-------------------

Authentication and Security
==============================
The authentication mechanism used is HTTP Basic authentication. The credentials have to be provide at each request.

In order to secure the user credentials that are in the http header, the request can be perform with HTTPS. However be aware that the certificate is self-signed.

Load
=======
Queries must be done in a sequential order, ie each HTTP call has to wait for the HTTP response before proceeding the next one. We do not allow parallel call from any partner. In case the partner needs more/faster processing of message we will work to improve the speed or allow multiple message in one request.

Request
=========
The API is design to be accessible by HTTP POST. 

EACH request headers MUST contain: 

#. The Basic Authentication header with Authorization
#. Usual AJAX identification with X-Requested-With 
#. The format of the post body with Content-Type

Here is an example:

================ =================================
Header Keys      Header Values
================ =================================
Authorization    Basic Y2lvZWNAY2lvZWNib2... 
X-Requested-With XMLHttpRequest
Content-Type     application/x-www-form-urlencoded 
================ =================================

**API URLs**

An URL is vusion is composed of 4 parts. The base URL, the program URL, the action URL and the extension. Let’s look at the example of creating a participant:
::
    https://vusion.texttochange.org/myProgram/programParticipants/add.json

In this example the:

* *https://vusion.texttochange.org/* is the base URL. For production, it’s http[s]://vusion.texttochange.org For testing, it’s http[s]://vusion-test.texttochange.org 
* *myProgram/* is the program URL. It is unique url of your program, provide by Text To Change
* *programParticipants/add* is the action URL to be performed
* *.json* is the extension, it describe the format of the response. Only json is available for now.

In the following API description, only the action is mention as the base URL, the programURL and extension are not changing.

**Localisation**

The Vusion API is localized in French and Spanish, English being the default. To get a localized messages, one will have to add the sub domain to the base URL. For example:

* https://spa.vusion.texttochange.org... for Spanish
* https://fre.vusion.texttochange.org... for French  

Note that the localization effort is time consuming and we have limited budget for it. Therefor some messages might not be localized or wrongly translated. If you encounter such issue, please notify us at vusion-issues@texttochange.com


Response
==========

At the HTTP level, the response will always be 200 OK. There are a few exception to this: 

* the Authentication fail. In case the Authentication fail, an HTTP 401 is returned. 
* on an edit action, the item ID is not found (for example a participant’s phone number). In such a case an HTTP 404 is returned.  
* note that server might return a HTTP 500 - internal error - in such a case, contact Vusion support with the following information: URL used, parameters and a copy/past of the response (or screenshot). 

The json responses will contain the field: status. The status value can be either ok or fail. Other field might be included depending of which feature has been used.

For example after a success, the response body would look like:
::
    {
        "status": "ok",
        "id": "53be8fd5e9cea58c4c5f8ee3"
        ….
    }

On the other hand if the action fail, there will be at least two fields: status and message. Such as:
::
    {
        "status": "fail",
        "message": "The Message could not be saved.",
        "validation-errors": {
            "send-to-type": [
                "Send To option not allowed."
            ]
        }
    }
