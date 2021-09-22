---
title: 'Saving data'
---

Node scripts can not directly insert data to the database. Instead, they must use out object.


### out.value

If node parameters has a field called "out_field", then whatever the script places to out.value is stored in the current document. 

	out.value = "Hello World!"

### out.setter

If node need to output severla fields, then it must use out.setter. 

	out.setter["some_field"] = "Hello world";

### out.url

Some nodes (like API lookup) must provide URL to GLAMpipe.


### out.say


This allows node to communicate directly to the user via websocket. Following styles are available:

- progress
- error
- finish


	out.say("progress", "processed 200 of 234");