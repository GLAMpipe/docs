---
title: 'Tutorial 7: Using REST API'
visible: true
---

GLAMpipe has a full API, which means that everything that can be done via user interface, can be done via API also. Unfortenately the REST API is not currently well documented.

#### Task 1
- get list of all projects in GLAMpipe.

##### Background information
The api endpoint is **/api/v1/projects**. If you want to get only the names of the projects, then you can use /api/v1/projects/titles

##### Solution

	curl http://demo.glampipe.org/api/v1/projects/titles

#### Task 2 
- Create a project called "Hello World".

##### Background information 
The api endpoint is **/api/v1/projects**. You need to make a post request with "title" parameter.

##### Solution

	curl -X POST -d "title=Hello World" http://localhost:3000/api/v1/projects
 
 Note that this creates a project without any collections. In order to add collection you must create it as follows:
 
 	curl -X POST -d "{'params': {'title':'my collection'}}" http://localhost:3000/api/v1/projects/5b217d24951720000816fe85/nodes/collection_basic?type=collection
    
#### Task 3
- Create a script that fetches the Helsinki City Orchestra concert data, makes it browseable by composer and year, and shows 10 the most popular composers at the end.

##### Solution
There is a python script that: 
https://github.com/GLAMpipe/python-api-examples

Basically the code is like this:

    # create online csv read node
    data = {'params': params_csv, 'collection': collection_id}
    csv_read = addNode('source_web_csv', data, project_id);

    #create extract node
    data = {'params': params_extract_year, 'collection': collection_id}
    extract_year = addNode('process_field_extract', data, project_id);

    #create facet view node
    data = {'params': {}, 'collection': collection_id}
    facet = addNode('view_facet', data, project_id);

    # run csv read node
    print("Reading CSV...")
    runNode(csv_read, settings_csv)

    # run csv read node
    print("Extracting years... this takes a while...")
    runNode(extract_year, settings_extract_year)

    # run facet node
    print("Creating facet view...")
    runNode(facet, settings_facet)
    print("Done!")

You can exceute the code like this:

	python csv-read-project.py 