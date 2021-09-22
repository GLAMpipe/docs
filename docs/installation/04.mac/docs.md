---
title: 'Native install on Mac'
---

If you can't to use Docker (too old hardware), you can install node and MongoDB via [Homebrew.](https://brew.sh/) 

1. Install node and mongodb

		brew install node
        brew install mongodb
        
	Then start mongodb:

		brew services start mongodb
        
    Check that mongo is really running by typing:
    
    	mongo

2. Fetch GLAMpipe code from GitHub

        git clone https://github.com/artturimatias/GLAMpipe.git
        cd GLAMpipe

3. Create data directory for GLAMpipe and set it as dataPath in config/config.js.


        mkdir /Users/YOUR_USERNAME_HERE/GLAMpipe-data 
        
    Then edit "datapath" in config/config.js:

        // DATAPATH
        // - where GLAMpipe can strore project data
        // default: ""
        var dataPath = "/Users/__YOUR_USERNAME_HERE__/GLAMpipe-data ;

4. Install node dependencies

        npm install

5. Try to run

        node glampipe.js

    You should see something like this:
    
        ********************* G L A M p i pe *************************
        * DATA PATH: /home/arihayri/GLAMpipe_DATA
        * NODE PATH: 
        * STATUS:    running on http://127.0.0.1:3000
        ********************* G L A M p i pe *************************
        
    You can stop GLAMpipe by pressing CTRL + C