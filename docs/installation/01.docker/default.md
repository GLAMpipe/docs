---
title: Docker
---

Make sure that you have [Docker](https://www.docker.com/) installed and running. You'll also need "make" tool available. Linux has it by default but I'm not sure about Mac/Win. 

# Legacy version 2018

1. Fetch GLAMpipe source codes and GLAMpipe nodes

		git clone https://github.com/glampipe/GLAMpipe.git
		cd GLAMpipe
        git checkout dev
        git clone https://github.com/glampipe/nodes.git
        

2. Create docker network,start MongoDB and build GLAMpipe image

		make create_network
        make build_mongo
        make build_glampipe
        
3. Start mongo and Nodejs (GLAMpipe) containers

		make start_mongo
        make start_glampipe
        
4. Start GLAMpipe inside Nodejs container

		node glampipe.js
        
        
# New version (2020-beta)

1. Fetch GLAMpipe source codes and GLAMpipe nodes

		git clone https://github.com/glampipe/GLAMpipe.git
		cd GLAMpipe
        git checkout rewrite
        git clone https://github.com/glampipe/nodes.git
        cd nodes
        git checkout rewrite
        cd ..
        

2. Create docker network,start MongoDB and build GLAMpipe image

		make create_network
        make build_mongo
        make build_glampipe
        
3. Start mongo and Nodejs (GLAMpipe) containers

		make start_mongo
        make start_glampipe
        
4. Start GLAMpipe inside Nodejs container

		node glampipe.js