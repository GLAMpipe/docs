---
title: 'Node development'
---

GLAMpipe reads nodes from **nodes** directory only when the program is started unless the node development mode is enabled. 

### Node development mode
For development you should switch to **node development mode**. When node development mode is enabled, node scripts are loaded dynamically when the node gets executed. This means that you can edit node scripts "live". Make a change and execute node to see the result.

You can enable dev mode by setting the nodeDevMode to true in config.js.example or config.js (config.js does not get overwritten when you pull a new version)

	var nodeDevMode = false;

Node development is a lot easier if you make a native installation (i.e. without Docker).



### Three types of GLAMpipe nodes

- **Modify nodes** (synchronous nodes, like "split" and "search&replace") use current document as an input and create output based on current document and settings and parameters given.

- **IO nodes** (asynchronous nodes, like import or lookup nodes) works in phases. The node first gives "orders" to GLAMpipe of how it should make a certain IO task (for example, make a request to web API). Then the result of this IO task gets back to node which processes it and then outputs the final value.

- **View nodes** creates a separate web application for viewing data. Currently there is only facet view node available.

The distinction between modify and IO nodes is purely technical and the end user should know nothing about it.