:index:`Content variable`
---------------------------

Content Variables aims to be use for message customisation. It allow to change the content of MT messages by only modifying the used Content Variable. The Content Variables are reusable over the all program: Request, Separate Message , Dialogue, ...

There are 2 type of content variable:

* *key/value* a simple key-value pair 
* *table* a two dimension table, it's looking like an Excel sheet. 

Key/Value
==========
The key is the name of content, for example 'Temperature'. The value is the actual content, so for example 10 degrees.

Example of key/value pair:

=============  ========
Key            Value
=============  ======== 
temperature    25C
chicken price  300KES
...            ...
=============  ========

When you want to access the content variable in a Request/Dialogue/Separte Message, in the message content use the following syntax:
::
	"Hello [contentVariable.<key>]

**Caution**

Pay attention to the capitalization of contentVariable. If other capital letters are applied it won't work. The key is also capital sensitive, so if you use 'Temperature' in stead of 'temperature' the message will not be delivered. 

See more about :doc:`Message Customisation </advanced/message_customisation>`

Table
==========

In the case of table, one can store a excel-like table. The right column and the top row being the keys to access the values. 

Example
======= ======
Item    Price
======= ======
chicken 300KES
fish    200KES
======= ======

To use it to customise a message, one would use:
::
	"Hello today price of fish is [contentVariable.fish.price]"

See more about :doc:`Message Customisation </advanced/message_customisation>`




