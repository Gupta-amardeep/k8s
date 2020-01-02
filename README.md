## Welcome to basic kubernetes repo.

You can find basic yaml files related to resouces of kubernetes.
One can clone this repo and run on their own kubernetes cluster.
Hope you find this repo useful in your initial learning phase of K8s.

## BASICS:-

Kubernetes - "an open-source system for automating deployment, scaling, and management of containerized applications".

A Kubernetes cluster is made of a master node and a set of worker nodes. The cluster is all driven via API calls to controllers, both interior as well as exterior traffic.

# Kubernetes has the following main components:

* Master and worker nodes

* Controllers

* Services

* Pods of containers

* Namespaces and quotas

* Network and policies

* Storage

1. Master Node

The Kubernetes master runs various server and manager processes for the cluster. Among the components of the master node are the kube-apiserver, the kube-scheduler, and the etcd database.

* The kube-api-server is central to the opn of k8s cluster. All calls external or internal are handled by this agent and is onle connection to etcd db. We can deploy multi node master cluster to load balance workload via load balancer.

* The kube-scheduler uses an algorithm to determine which node will host a Pod of containers. The scheduler will try to view available resources (such as volumes) to bind, and then try and retry to deploy the Pod based on availability and success. There are several ways youcan affect the algorithm, or a custom scheduler could be used instead. You can also bind a Pod to a particular node, though the Pod may remain in a pending state due to other settings.

* The state of the cluster, networking, and other persistent information is kept in an etcd database.There is a master database along with possible followers. They communicate with each other on an ongoing basis to determine which will be master, and determine another in the event of failure.

* The kube-controller-manager is a core control loop daemon which interacts with the kube-apiserver to determine the state of the cluster. If the state does not match, the manager will contact the necessary controller to match the desired state. There are several controllers in use, such as endpoints, namespace, and replication. 
