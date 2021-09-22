---
title: Introduction
---

### How does GLAMpipe differ from other tools?

There are many tools for data manipulation, and they all do things differently. GLAMpipe is created with GLAM data in mind. GLAMs are memory institutions – Galleries, Libraries, Archives and Museums – that have collections of items. Transformations and processing of GLAM data differs, let's say, from transforming scientific data. Typically GLAM data has:

- multiple values for one field
    - language versions (language codes)
    - multiple authors, types etc.
- inconsistent data
    - data itself is created over the years

### Different ways of making transformations

#### Spreadsheet editing

Often GLAMs work with spreadsheets to manipulate collection data. Although spreadsheet editing is the easiest way for non-programmers to transform data, this approach has several problems:

- it requires lot of work
- complex processing is tricky
- multiple values per cell are not really multiple values
- spreadsheets can not operate with files or uploads
- repeating a process automatically with another data set is not possible

#### Writing scripts

For programmers, the usual way of making data transformations or data uploads is to write *ad hoc* scripts. This works, but it also has some downsides:

- Scripts are usually not documented and therefore re-using them might be tricky. 
- Writings scripts requires technical expertise.
- It is difficult to make manual fixes to data between transformations. 

#### GLAMpipe

GLAMpipe is trying to combine the strengths of scripting and spreadsheet editing.  

- real multiple values are possible for one field (arrays)
    - especially important for GLAM-data (multiple authors etc.)
- manual editing is easy  (like in spreadsheet editing)
    - it is possible to fix values manually if necessary
- graphical user interface
    - usable by non-programmers
- extensible
    - new functionality can be added by writing new nodes
- re-usable pipeline
    - once the pipeline is constructed, it can be re-used for similar cases
    - also via REST API (without GUI)








