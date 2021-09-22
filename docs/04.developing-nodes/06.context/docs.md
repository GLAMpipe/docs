---
title: Context
---

When node scripts are executed (via vm.runInNewContext), an context object is passed to a node. Here is what it contains:


* **context.doc**

    Contains current record. Properties of the record can be accessed normally. 

    For example, the title of the record: 


        var title = context.doc.title;

* **context.data**

    For API nodes (API source and API lookup) context.data holds the request response. 

* **context.node**

    Contains node object itself (params and settings).

* **context.doc_count**

    Contains total record count.

* **context.count**

    Contains loop counter (i.e. how many records have been processed).


----
## How about output?

Nodes communicate with outer world via "out" object.

* **out.url**

    Some nodes (like API lookup) must provide URL.

* **out.value**

    This is what is stored to database. It can be an object
    
* **out.say**

    This allows node to communicate directly to the user via websocket. Following styles are available:
 
    * hello

    * news

    * progress

    * error

    * finish


    out.say("progress", "processed 200 of 234");

    

## views
Nodes have three different kind of views. View consists of HTML and possible javascript.

* **params**

    params view is displayed to the user when s/he *creates* a node. Values user inserts are then strored to the node in a form params.input_name.

    So, if you have an input named "prefix" in params view, the value is then later accessible in node scripts via context object like this:

        var pre = context.node.params.prefix;

* **settings**

    settings view is displayed to user when the node is selected in a project view. 

    If node has input named "separator" in settings view, the value is then later accessible in node scripts via context object like this:

        var sep = context.node.settings.separator;


