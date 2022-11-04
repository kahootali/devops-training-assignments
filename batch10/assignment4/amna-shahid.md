KUBERNETES ARCHITECHURE	
**************************************************

There are two main parts of k8s
**************************************************

1. Control Plane
2. Worker

1. CONTROL PLANE
====================
Control plane, also known as master node, is responsible to control the worker nodes. It has follwoing components:

a. API SERVER
--------------
This is the main part of k8s and user can communicate with k8s using this api server. it is restful api. this server is stateless. Api server saves states in ETCD.

API Server process request in following steps.

1 authentication Plugin
When a  request is arrived at API SERVER, the Authentication plugin(can be one or more) verify the request.

2.Authorization plugin
If all the authentication plugins pass the request, then authoriztion plugin(can be one or more) checks if the requesting user has access to requested resourse.

3.Addmission Controller
After authentication and authorization, the admission controller comes in action. this is the step where the k8s distinguist the type of request (PUT,GET ,DELETE etc.). 

b. ETCD
-----------
ETCD is key value storage. There can be more than one instances. More than one instances can provide the high performance.

c. SCHEDULER 
-------------
Scheduler watches for newly created PODs which are not assigned to any node, then scheduler assigns it to a node. Once the POD is assigned to a node, a kubelet  in node is notified for the change.

d. CONTROLLER MANAGER
----------------------
Controller run the cloud. it regulates the state of k8s cluster. communicates the scheduler and tries to change the current state to desired state.s

*****************************************************************************************************************************************************

2. WORKER NODE
===============
This part is responible to execute the request. It mainly contains the application for which user has requested. Code is executed and response is send. It has following componenets.

a.KUBELET
----------
Kubelet is reponsible for all actions taking place in worker node. it runs the POD

b. KUBE PROXY
-------------
When a POD is assigned to a node then kube proxy, an ip is assigned to it and it is saved in IPTABLE

c. CONTAINER RUNTIME
--------------------
Container runtime is responsible for running the containers.




