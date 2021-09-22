---
title: ''
body_classes: ''
order_by: ''
order_manual: ''
---

To get started, you need access to GLAMpipe. You have two options:
1. Try demo version. (Sorry, demo version not currently available)
2. Install GLAMpipe on your computer. Try quick install first (see below).

Note: this installs a *development version* of GLAMpipe

##Quick install on Linux and Mac

Before you can install GLAMpipe, you need a [Docker](https://www.docker.com) for  [Ubuntu](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/) / [Debian](https://docs.docker.com/engine/installation/linux/docker-ce/debian/) / [Mac](https://www.docker.com/docker-mac) / [Windows](https://docs.docker.com/docker-for-windows/install/) installed and running on your computer. 

Open terminal, make a directory for GLAMpipe data and fetch install script:

	mkdir glampipe && cd glampipe
    
Linux:

	wget https://raw.githubusercontent.com/artturimatias/GLAMpipe/dev/install_glampipe.sh
    
Mac:
	
    curl -O https://raw.githubusercontent.com/artturimatias/GLAMpipe/dev/install_glampipe.sh
    
Make the script executable:

    chmod u+x install_glampipe.sh
    
Execute script

	./install_glampipe.sh



##Quick install on Win

There is no install script for Windows yet.