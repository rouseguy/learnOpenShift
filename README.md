# Introduction to OpenShift


### What is OpenShift?
(TODO)

**About the workshop**

I took the material from [here](https://github.com/gshipley/openshift-workshops-1)

Run the following in the repo

```
     $ bundle exec puma
```

Now, in the browser open: [http://localhost:9292/](http://localhost:9292/) to browse the training material that was used to learn/execute the below given commands

**Installing OpenShift client**

We will use the Python client `powershift`

```
     $ pip install powershift  
     $ powershift client versions   # This will list all openshift versions available via powershift  
     $ powershift client install v1.5.0-rc.0 # Install the recent version  
     $ export PATH=~/.powershift/tools:$PATH  # Add oc to PATH environment variable  
     $ oc version # This will tell what version of oc has been installed.   
```

**Login to the OpenShift cluster**

```
    $ oc login https://HOST:8443      # Replace HOST with the cluster name
    $ Username: <Enter username>
    $ Paassword: <Enter password>
```

**Create a new project** 

```
    $ oc new-project oc-test-1
```

Now login to the web-console: [https://HOST:8443](https://HOST:8443)

You should see the project `oc-test-1` listed there.

Click on "Add Project".

Click the "Deploy Image" tab.

And paste the following and press enter

```
     docker.io/openshiftroadshow/parksmap-py:1.0.0
```

Hit "Create"

Click "Overview" on the left-side menu bar and you should see the pod running.

Now, from the command line, let's examine the pod

```
     $ oc get pods

```

The above command will list all pods running in the current project.

Let's examine the content of the pod.

```
     $ oc get pod parksmap-1-pvuip -o yaml
```

The pod name is obtained from the previous command

To know the services defined in the current project, run the following command

```
     $ oc get services
```

The following command gives more information about a service

```
     $ oc get service parksmap -o yaml
```

And this:

```
     $ oc describe service parksmap
```







