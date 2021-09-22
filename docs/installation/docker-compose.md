---
title: ''
body_classes: ''
order_by: ''
order_manual: ''
---

### Docker Compose (currently not up to date!)

GLAMpipe can be installed via [Docker compose](https://docs.docker.com/compose/). So first you need to install Docker:
https://docs.docker.com/engine/installation/


1. Clone GLAMpipe repository:

        git clone https://github.com/GLAMpipe/GLAMpipe.git
        cd GLAMpipe



2. Then install GLAMpipe.

    First, build from source:

        docker-compose build

    And finally:

        docker-compose up


This takes a while at first time but next time the start up is almost instant. Finally you should see something like this:


        ********************* G L A M p i pe *************************
        * DATA PATH: /home/arihayri/GLAMpipe_DATA
        * NODE PATH:
        * STATUS:    running on http://0.0.0.0:3000
        ********************* G L A M p i pe *************************



 Just type http://localhost:3000 in your browser and you should have GLAMpipe in front of you.
 You can stop GLAMpipe by pressing **CTRL + C** and start it again by typing **docker-compose up**
