---
title: 'Native install on Linux'
---

This will guide you through native nodejs install on Linux (Debian-based distros like Ubuntu). These instructions should get you going with GLAMpipe if you have a Linux box or if you can run Linux in virtual machine. 

1. First install and git, curl and some compiling packages

         sudo apt-get install git curl build-essential
 
2. Install MongoDb > 3.6 (all features might not work with older versions)

    See instructions: [https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/)
    
    Then test your installation
    
        mongo
    You should see something like this:
    
        MongoDB shell version v3.6.3
        connecting to: test
        > 

     Press CTRL + C to exit MongoDB Shell.


2. Then install nodejs. Nodejs in repositories is quite old so it is better to install from nodesource: https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions

    fetch nodejs setup script, execute it and install node:

        curl -sL https://deb.nodesource.com/setup_8.x -o nodesource_setup.sh
        sudo bash nodesource_setup.sh
        sudo apt-get install nodejs



4. Fetch GLAMpipe code and nodes from GitHub

        git clone https://github.com/glampipe/GLAMpipe.git
        cd GLAMpipe
        git clone https://github.com/glampipe/nodes.git
        git checkout dev



5. Install node dependencies

        npm install

6. Try to run

        node glampipe.js

    You should see something like this:
    
        ********************* G L A M p i pe *************************
        * DATA PATH: /home/arihayri/GLAMpipe_DATA
        * NODE PATH: 
        * STATUS:    running on http://127.0.0.1:3000
        ********************* G L A M p i pe *************************
        
    You can stop GLAMpipe by pressing CTRL + C



