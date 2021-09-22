---
title: Terminology
---

## Node
Nodes are the building blocks of GLAMpipe. The idea of a node is that each node makes one, relatively **simple thing** with the data or file. By chaining nodes one can make different transformations to the data.

There are three groups of nodes:
* Importing data
* Processing the data 
* Exporting the data 

![](glampipe_node_groups.png)

Nodes are mini-applications written in Javascript that can have their own user interface.  

Nodes **do not overwrite** original, imported data. For example, if you use a "split" node for the "author" field, you get a new field called "author_splitted". This makes experimenting easy, since you can not destroy the original data.
    
## Project
A user can create a project that contains everything that is used in the project.

## Collection
A collection is a dataset used in the project. There may be several datasets in a project. They can be used for subsets of data, such as the data for authors or places that are recurrent in the main dataset.


