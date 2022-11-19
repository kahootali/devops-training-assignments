# Assignment 4

Tasks to be completed by next class

- Complete all the labs >> Done
- Try to understand what the commands are doing >> Trying to understand the commands by practising.
- Describe Architecture of Kubernetes and push to Github repo
  Ans- An architecture called Kubernetes provides a loosely linked approach for service discovery throughout a cluster.
       One or more computing nodes and one or more control planes make up a Kubernetes cluster.
       In general, the control plane is in charge of controlling the entire cluster, making the application programme interface (API) accessible, and planning the startup and shutdown of compute nodes according to a desired configuration.
       A container runtime like Docker and an agent called kubelet that interacts with the control plane are both installed on each computing node.
       Each node may consist of bare metal servers, virtual computers running on-site or in the cloud, 
       
       Among a Kubernetes cluster's primary elements are:

        Nodes: Containerized apps run on nodes, which are virtual machines or physical servers.
        One or more application instances may be running on each node in a cluster.
        Although a typical Kubernetes cluster will contain numerous nodes, there might be as little as one (and deployments with hundreds or more nodes are not uncommon).
        
        Image Registry: The control plane transfers container images from the registry to nodes for use in container pods.
        
        Applications running in containers are housed in pods.
        They are the lowest unit of deployment for apps in a Kubernetes cluster and can contain one or more containers. 

  
