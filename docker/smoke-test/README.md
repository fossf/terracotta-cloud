# Smoke test for Terracotta Docker images

After you've locally build the images, you want to quickly check whether they seem to be working or not.

## What those scripts do

Those scripts will help you find out, they basically:

* Run a Terracotta Server
* Configure it with the config tool
* Run a Terracotta Management Console (TMC)
* Assert the tmc "sees" the servers and its resources
* Run an ehcache client and assert the TMC can "see" the caches
* Run an store client and assert the TMC can "see" the datasets

## How to run them

```bash
<<<<<<< HEAD
export VERSION=10.11.0-SNAPSHOT
=======
export VERSION=10.7.0-SNAPSHOT
>>>>>>> a072e15b3b95bba03aeb6c4fcb0bdc2133d8f654
./smoke-test.sh
```