# Master | control-plane components :-

API Server → It is the core of the Kubernetes control plane allowing users to manage and interact with Kubernetes clusters.

Schedules →  It is a control plane process which assign pods to Nodes.

etcd → It is a key-vale store that stores and manages configuration data for Kubernetes cluster.

Controller Manager → It is a demon that monitors & manages the State of Kubernetes clusters.

Cloud-controller manager →  It is a tool that integrates a Kubernetes cluster with a cloud providers infrastructure.

Cubectl →  It is command line tool that allows user to control Kubernetes cluster.

----------------------------------------------------------------------------------------


# Node components :-
	
Kubelet → It works as node level agent to help with container management & orchestration within a kubernetes cluster.

 
Kube Proxy → It is responsible For managing rules & facilitating communication between  services And Pods by translating service addresses to the underlying Pod IPs.


Container runtime → It is the software component responsible for managing the lifecycle of container including pulling images from registry creating and running them, and monitoring their execution on the host system.

 ---------------------------------------------------------------------------------
