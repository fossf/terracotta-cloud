Copyright (c) 2011-2019 Software AG, Darmstadt, Germany and/or Software AG USA Inc., Reston, VA, USA, and/or its subsidiaries and/or its affiliates and/or their licensors.
Use, reproduction, transfer, publication or disclosure is prohibited except as specifically provided for in your License Agreement with Software AG

#What is the Terracotta Management Console?

The Terracotta Management Console (TMC) is a web-based administration and monitoring application allowing you to monitor and manage your Terracotta products (Ehcache, Tcstore, Terracotta Server Array)

#How to use this image: QuickStart

You can now run the TMC in a container :

<<<<<<< HEAD
     docker run -e ACCEPT_EULA=Y -d -p 9480:9480 --name tmc tmc:10.11.0-SNAPSHOT
=======
     docker run -e ACCEPT_EULA=Y -d -p 9480:9480 --name tmc tmc:10.7.0-SNAPSHOT
>>>>>>> a072e15b3b95bba03aeb6c4fcb0bdc2133d8f654

At this point go to http://localhost:9480/ from the host machine to see the TMC welcome page

#How to use this image: with a Terracotta Server

Of course, having a TMC running only makes sense if you have a Terracotta Server to monitor / manage.

If you have already built the terracotta docker image, then, start it :

<<<<<<< HEAD
    docker run -e ACCEPT_EULA=Y -d -p 9410:9410 --name terracotta terracotta-server:10.11.0-SNAPSHOT

Don't forget to install a license using the cluster tool :

    docker run -e ACCEPT_EULA=Y --link terracotta:terracotta -e "LICENSE_URL=https://server/license.xml" terracotta-cluster-tool:10.11.0-SNAPSHOT configure -n MyCluster -s terracotta

and then re try running the tmc, with :

    docker run -e ACCEPT_EULA=Y -d -p 9480:9480 --name tmc --link terracotta:terracotta tmc:10.11.0-SNAPSHOT
=======
    docker run -e ACCEPT_EULA=Y -d -p 9410:9410 --name terracotta terracotta-server:10.7.0-SNAPSHOT

Don't forget to install a license using the cluster tool :

    docker run -e ACCEPT_EULA=Y --link terracotta:terracotta -e "LICENSE_URL=https://server/license.xml" terracotta-cluster-tool:10.7.0-SNAPSHOT configure -n MyCluster -s terracotta

and then re try running the tmc, with :

    docker run -e ACCEPT_EULA=Y -d -p 9480:9480 --name tmc --link terracotta:terracotta tmc:10.7.0-SNAPSHOT
>>>>>>> a072e15b3b95bba03aeb6c4fcb0bdc2133d8f654

and checkout what's happening with :

    docker logs -f tmc

Now you can create a new connection, and use terracotta://terracotta as your Terracotta server URL

Or else, I suggest you to move on to the orchestration folder and use Docker compose to orchestrate your containers.

#How to build this image

Once Docker is up and running in your environment, from the root folder (/opt/softwareag for example) run this command :

<<<<<<< HEAD
    $ cd terracotta-10.11.0-SNAPSHOT
    $ docker build --file docker/images/tmc/Dockerfile --tag tmc:10.11.0-SNAPSHOT .
=======
    $ cd terracotta-10.7.0-SNAPSHOT
    $ docker build --file docker/images/tmc/Dockerfile --tag tmc:10.7.0-SNAPSHOT .
>>>>>>> a072e15b3b95bba03aeb6c4fcb0bdc2133d8f654
