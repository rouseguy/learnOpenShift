# Introduction to OpenShift


### What is OpenShift?
(TODO)

**Installing OpenShift client**

We will use the Python client `powershift`

    $ pip install powershift
    $ powershift client versions   # This will list all openshift versions available via powershift
    $ powershift client install v1.5.0-rc.0 # Install the recent version
    $ export PATH=~/.powershift/tools:$PATH  # Add oc to PATH environment variable
    $ oc version # This will tell what version of oc has been installed. 


**Login to the OpenShift cluster**

    $ oc login https://HOST:8443      # Replace HOST with the cluster name
    
**Create a new project** 

    $ oc new-project oc-test-1
