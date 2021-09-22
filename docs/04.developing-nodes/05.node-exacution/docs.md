---
title: Execution
slug: node-exacution
---

## What happens when a modify node is executed?

Parameters starting with "out\_" (like "out_field") are node's output fields and those are added for all documents in the collection when the node is created. 


This what happens when the user clicks the "run" button:
1. Glampipe finds all documents from current collection
2. Script run.js is executed for each document (see [asyncloop](https://github.com/GLAMpipe/GLAMpipe/blob/master/app/async-loop.js) in source code)
3. Run.js can access the current document via **context.doc** variable. 
4. Run.js sets the desired output to **out.value** or **out.setter** (multiple output fields)
3. After run.js is executed, the result (out.value or out.setter) is **saved** to document.

#### What happens when a IO node is executed?

If node is a processing (i.e. not source node) node, then the **name of the output field **(or fields) is defined when the node is created. This field(s) is added for all documents in the collection when the node is created. 

However, if the node is an import, export or view node, then there is no output fields. 

This what happens when the user clicks the "run" button (DSpace import node):

1. The nodes's init.js script is called. This outputs an initial search query URL.
2. GLAMpipe executes the request and saves response to context.data.
3. Next GLAMpipe executes run.js, which processes data which is then saved to database.
4. Then run.js exports new url, if there is still data left.

If node is an import node, the collection is emptied from previous records imported by this node. 



