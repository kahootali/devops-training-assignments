
        ---------------------------------
        |       Dice Assignment-4       |
        |       Mahmood Khan            |
        |       DevOps - Batch - 09     |
        ---------------------------------

Tasks to be completed by next class

- Complete all the labs
- Try to understand what the commands are doing
- Describe Architecture of Kubernetes and push to Github repo


--------------------------------------------------------------------------XX
--------------------------------------------------------------------------XX

Kubernetees Archtecture:

Api-Server: All comminucation thorugh this, all management.
etcd: is the database for state and evenrything in the cluster.
Controller Mgr: Manages all the controllers.
Scheduler: Checking node availability.
Kublet: Node-leader, is the node manager. checking the health.
Kube-Proxy: Networking brain. Ip add, remove, backend communication,
Container runtime (Docker): Runs the containers.
Pods: Can have one or more containers.


Api server, /etcd, scheduler, controller manager.
Mubelet, container runtime, kube-proxy, pods


Example from Class:
Call from dveeloper to Api server.
Apiserver will perform authorization and authentication, validation, of the menifest.
then send the menifest to "/etcd" to save.
Then send it to "scheduler" and asking where should it be scheduled.
"Scheduler" will check and recommend e.g., node-2
Then api server will contact "Kubelet" of that Node and send the definition.
Kublet will translate the definitions into container definitaion and ask cntainer runtime to run this container with this this specs.
Kube Proxy will assign the IP and also add the Ip into its routing table.



--------------------------------------------------------------------------XX

