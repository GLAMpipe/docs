# Installation

Using **Docker Compose** is the easiest way to get GLAMpipe running. For alternatives, see alternative installation methods.

## requirements

- Docker For [Ubuntu](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/) | [Debian](https://docs.docker.com/engine/installation/linux/docker-ce/debian/) | [Mac](https://docs.docker.com/desktop/mac/install/) | [Windows](https://docs.docker.com/docker-for-windows/install/)
- [Git Version Control](https://git-scm.com/)


##Installing with Docker Compose


First, fetch source code:

	git clone https://github.com/GLAMpipe/GLAMpipe.git

Enter into newly-created GLAMpipe directory:

	cd GLAMpipe

Next fetch GLAMpipe nodes:

	git clone https://github.com/GLAMpipe/nodes

Then build and run.

	docker-compose up

Then aim your browser to <a target="_blank" href="http://localhost:3000">http://localhost:3000</a>

## Stopping and Starting

If you kept terminal open, then you can just press Ctrl + C in order to stop containers. If you closed terminal, then cd back to GLAMpipe directory and type

	docker-compose down

You can start GLAMpipe again by typing

	docker-compose up
