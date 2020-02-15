---
title:  Using docker
layout: page
---



## Starting docker for the first time

Create a running docker container named `mid`:

    docker run -ti --name mid -v $(pwd):/workspace neelsmith/hmteditor

This will build and start the container, and run a bash shell in the container with all the software you need installed.  If you exit the bash shell, the container will still exist:  you can restart it in two steps.

## Restarting

Two steps:


    docker restart mid
    docker exec -ti mid /bin/bash
