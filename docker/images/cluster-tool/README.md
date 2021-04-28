#### What is the cluster tool ?

Terracotta Server supports a distributed in-memory data-storage topology, which enables the sharing of data among multiple caches and in-memory

The cluster tool is a command-line utility that allows administrators of the Terracotta Server Array to perform a variety of cluster management tasks. 
For example, the cluster tool can be used to:

- Obtain the status of running servers
- Dump the state of running servers
- Stop running servers
- Take backup of running servers


#### How to use this image: QuickStart

0. You can run a terracotta server using (provided you built the terracotta image) :

<<<<<<< HEAD
       docker run -e ACCEPT_EULA=Y -d -p 9410:9410 --name terracotta terracotta-server:10.11.0-SNAPSHOT
=======
       docker run -e ACCEPT_EULA=Y -d -p 9410:9410 --name terracotta terracotta-server:10.7.0-SNAPSHOT
>>>>>>> a072e15b3b95bba03aeb6c4fcb0bdc2133d8f654


1. Obtain the `status` of running servers:


<<<<<<< HEAD
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.11 status -s terracotta
         
   Or, to get the status of the entire cluster:
    
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.11 status -n tc-cluster -s terracotta
=======
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.7 status -s terracotta
         
   Or, to get the status of the entire cluster:
    
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.7 status -n tc-cluster -s terracotta
>>>>>>> a072e15b3b95bba03aeb6c4fcb0bdc2133d8f654
         
2. `Dump` the state of running servers:

        
<<<<<<< HEAD
         docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.11 dump -s terracotta
        
   Or, to dump the entire cluster:
        
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.11 dump -n tc-cluster -s terracotta
=======
         docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.7 dump -s terracotta
        
   Or, to dump the entire cluster:
        
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.7 dump -n tc-cluster -s terracotta
>>>>>>> a072e15b3b95bba03aeb6c4fcb0bdc2133d8f654
        
4. `Stop` running servers:


<<<<<<< HEAD
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.11.0-SNAPSHOT stop -s terracotta
        
   Or, to stop the entire cluster:
    
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.11.0-SNAPSHOT stop -n tc-cluster -s terracotta
=======
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.7.0-SNAPSHOT stop -s terracotta
        
   Or, to stop the entire cluster:
    
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.7.0-SNAPSHOT stop -n tc-cluster -s terracotta
>>>>>>> a072e15b3b95bba03aeb6c4fcb0bdc2133d8f654
        
5. Take `backup` of the cluster:

        
<<<<<<< HEAD
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.11.0-SNAPSHOT backup -n tc-cluster -s terracotta
=======
        docker run -e ACCEPT_EULA=Y --link terracotta:terracotta terracotta-cluster-tool:10.7.0-SNAPSHOT backup -n tc-cluster -s terracotta
>>>>>>> a072e15b3b95bba03aeb6c4fcb0bdc2133d8f654


#### How to build this image

To build this Dockerfile

<<<<<<< HEAD
    $ cd terracotta-10.11.0-SNAPSHOT
    $ docker build --file docker/images/cluster-tool/Dockerfile --tag terracotta-cluster-tool:10.11.0-SNAPSHOT .
=======
    $ cd terracotta-10.7.0-SNAPSHOT
    $ docker build --file docker/images/cluster-tool/Dockerfile --tag terracotta-cluster-tool:10.7.0-SNAPSHOT .
>>>>>>> a072e15b3b95bba03aeb6c4fcb0bdc2133d8f654
