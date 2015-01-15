API History
--------------

index
=======
**Method**
GET

**Action URL**
::
    .../programHistory/index...

**Format**

* json
* csv
* html

**Optional Parameters**

* **page** the page number to show, default 1
* **limit** the numnber of participants per page, default 20, maximum 500
* filter parameters can also be used see below

Example of request

http://vusion-test.texttchange.org/myprogram/programHistory/index.csv/page:2/limit:300

**Filter Parameters**
Vusion provides a filtering mechanism that consist of 

* **filter_operator** the logical operator between the filter_param. Possible values "all" or "any". 
* **filter_param**: stack of filters, it's 2 dimenstional array with "filter_param[X][Y]" with X being the Xth filter, and Y the 2 or 3 element describing the filter. "filter_param[X][1]" is the type of filter, "filter_param[X][2]" is the filter operator, "filter_param[X][3]" is a comparaison parameter. "filter_param[X][3]" could be optional depending on the filter parameter.

TODO: add a description of all the filter type

Example of filters parameters

* ...filter_operator=all&filter_param[1][1]=answer&filter_param[1][2]=matching... #get only matching answer
* ...filter_operator=all&filter_param[1][1]=phone&filter_param[1][2]=is&filter_param[1][3]=+256666667... #get all message from/to +256666667
* ...filter_operator=all&filter_param[1][1]=date&filter_param[1][2]=from&filter_param[1][3]=2015-01-01... #get all message send or received afte the 1st of January 2015

Full request example

http://vusion-test.texttchange.org/myprogram/programHistory/index.json/limit:100/filter_operator=all&filter_param[1][1]=date&filter_param[1][2]=from&filter_param[1][3]=2015-01-01


listHistory
==============
To list all histories, the hard coded limit is set to 10000

**Method**
Get

**Action URL**
::
    .../programHistory/listHistory...

**Format**

* json
* csv

**Optional Parameters**

* same filter parameters of index can also be used