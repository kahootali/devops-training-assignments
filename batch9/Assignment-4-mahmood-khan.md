
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

All Labs were Done and commands and output are listed below:

Lab: K8s Minikube setup:

Install minikube from: https://minikube.sigs.k8s.io/docs/start/ for your
specific OS then run
minikube start
kubectl get po -A
Once both commands run successfully, you have a local K8s cluster

>> Below is the output:

ubuntu@ip-172-31-19-1:~$ minikube start --driver=docker
* minikube v1.26.1 on Ubuntu 22.04 (xen/amd64)
* Using the docker driver based on user configuration
* Using Docker driver with root privileges
* Starting control plane node minikube in cluster minikube
* Pulling base image ...
* Downloading Kubernetes v1.24.3 preload ...
    > preloaded-images-k8s-v18-v1...:  405.75 MiB / 405.75 MiB  100.00% 99.43 M
    > gcr.io/k8s-minikube/kicbase:  386.60 MiB / 386.61 MiB  100.00% 53.94 MiB
    > gcr.io/k8s-minikube/kicbase:  0 B [_______________________] ?% ? p/s 5.6s
* Creating docker container (CPUs=2, Memory=2200MB) ...
* Preparing Kubernetes v1.24.3 on Docker 20.10.17 ...
  - Generating certificates and keys ...
  - Booting up control plane ...
  - Configuring RBAC rules ...
* Verifying Kubernetes components...
  - Using image gcr.io/k8s-minikube/storage-provisioner:v5
* Enabled addons: storage-provisioner, default-storageclass
* Done! kubectl is now configured to use "minikube" cluster and "default" namespace by default
ubuntu@ip-172-31-19-1:~$ kubectl get po -A
NAMESPACE     NAME                               READY   STATUS    RESTARTS      AGE
kube-system   coredns-6d4b75cb6d-l8tqr           1/1     Running   0             23m
kube-system   etcd-minikube                      1/1     Running   0             23m
kube-system   kube-apiserver-minikube            1/1     Running   0             23m
kube-system   kube-controller-manager-minikube   1/1     Running   0             23m
kube-system   kube-proxy-9qmgz                   1/1     Running   0             23m
kube-system   kube-scheduler-minikube            1/1     Running   0             23m
kube-system   storage-provisioner                1/1     Running   1 (23m ago)   23m

<<|


--------------------------------------------------------------------------XX

Lab: Single Container. Terminal Output:

ubuntu@ip-172-31-19-1:~/labs-working/k8s-labs/module-1$ ls
backend.yaml            deployment-rolling-update.yaml  external-name.yaml  golang-api.yaml  multi-container.yaml  single-container.yaml
busybox-with-curl.yaml  deployment.yaml                 frontend.yaml       golang-svc.yaml  replicaset.yaml       ui-app.yaml

ubuntu@ip-172-31-19-1:~/labs-working/k8s-labs/module-1$ vi single-container.yaml
ubuntu@ip-172-31-19-1:~/labs-working/k8s-labs/module-1$ kubectl apply -f single-container.yaml
pod/counter created
ubuntu@ip-172-31-19-1:~/labs-working/k8s-labs/module-1$ kubectl get pods
NAME      READY   STATUS    RESTARTS   AGE
counter   1/1     Running   0          12s
ubuntu@ip-172-31-19-1:~/labs-working/k8s-labs/module-1$ kubectl logs counter
0: Fri Aug 19 22:19:41 UTC 2022: Kubernetes single container in 1 Pod
1: Fri Aug 19 22:19:46 UTC 2022: Kubernetes single container in 1 Pod
2: Fri Aug 19 22:19:51 UTC 2022: Kubernetes single container in 1 Pod
3: Fri Aug 19 22:19:56 UTC 2022: Kubernetes single container in 1 Pod
4: Fri Aug 19 22:20:01 UTC 2022: Kubernetes single container in 1 Pod


--------------------------------------------------------------------------XX

