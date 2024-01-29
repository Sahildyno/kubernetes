# KUBERNETES

What is Kubernetes?
Kubernetes is an open-source container orchestration platform designed to automate the deployment, scaling, and management of containerized applications.

## Why we use Kubernetes?
Kubernetes is used for automating and managing the deployment, scaling, and operation of containerized applications, providing efficiency, portability, and scalability across diverse environments

 **Container management**
        -Kubernetes automates the deployment, scaling, and management of containerized               
         applications.
 **Load balancer**
        -In Kubernetes, load balancing is a fundamental component to ensure that traffic is efficiently distributed across multiple instances of a service or application.
 **Auto-scaling**
        -Autoscaling in Kubernetes refers to the ability to automatically adjust the number of running instances (pods) of a deployed application based on the observed demand or specified metrics.
 **Security management**
        -Security management in Kubernetes is crucial to ensure the protection of containerized applications and the overall integrity of the cluster.
 **Auto healing & Auto restart**
        -In Kubernetes, the concepts of auto-healing and auto-restart refer to the platform's ability to automatically recover from failures by restarting or replacing components that are not functioning as expected.        
 **Monitoring**
        -Monitoring in Kubernetes is crucial for gaining insights into the health, performance, and resource utilization of your clusters and applications.
 **Standard DNS service**
        -In Kubernetes, the standard DNS service is provided by a component called CoreDNS. CoreDNS is a lightweight and flexible DNS server that is designed to be a cluster DNS server for Kubernetes.
 **Multi-node cluster**
        -A multi-node Kubernetes cluster consists of multiple machines, each referred to as a node, working together to orchestrate and manage containerized applications. 

## Architecture of Kubernetes

A Kubernetes cluster consists of two main types of nodes: master nodes and worker nodes

**master node** 
        -The master node is the control plane component that manages the overall state and configuration of the cluster. It is responsible for making global decisions about the cluster, scheduling workloads, and maintaining the desired state.
    
    1.API Server
        - The API server is the central management point for the Kubernetes control plane. It exposes the Kubernetes API, which is used by users, administrators, and controllers to interact with the cluster.
    2.ETCD 
        -A distributed key-value store that stores the configuration data of the cluster. It serves as the source of truth for the cluster state, providing a consistent and highly available data store.
    3.Scheduler
        -Responsible for placing newly created pods onto nodes based on resource requirements, constraints, and other policies.
    4.Controller Manager
        -Monitors the state of the cluster and responds to changes. It includes various controllers such as Node Controller, Replication Controller, and Endpoint Controller, ensuring the desired state is maintained.
**Worker node**
        -Worker nodes are the machines where containers run. Each worker node runs a container runtime (such as Docker) and a set of Kubelet, Kube Proxy, and other components.
    
    1.Kublet
        -The Kubelet is the primary node agent that communicates with the API Server and manages containers on the node. It ensures that containers are running in a Pod as expected
    2.Kube proxy 
        - Maintains network rules to allow communication between pods across the cluster. It also performs load balancing for services.
    3.Container engine 
        -In Kubernetes, the term "container engine" typically refers to the software responsible for running containers on the worker nodes of a Kubernetes cluster.
    4.POD 
        -In Kubernetes, a Pod is the smallest and simplest deployable unit in the computing model. A Pod represents a single instance of a running process in a cluster, which may consist of one or more containers. 

## Lifecycle of kubernetes

    1.Development
        -Containerize applications using Docker.
        -Write Kubernetes manifests (YAML or JSON) to define application structure.

    2.Container Image Build
        -Build container images from Dockerfiles.
        -Push images to a container registry.

    3.Cluster Provisioning
        -Set up a Kubernetes cluster using tools like kubeadm or managed services (GKE, EKS, AKS).

    4.Configuration
        -Configure Kubernetes manifests for the target environment.

    5.Deployment
        -Apply manifests to deploy the application on the cluster.

    6.Scaling
        -Dynamically scale resources based on demand.

    7.Service Discovery
        -Use Kubernetes Services for internal communication.

    8.Monitoring and Logging
        -Implement monitoring tools for performance metrics.
        -Set up logging solutions for application logs.

    9.Updates and Rollbacks:
        -Deploy updates through manifest modifications.
        -Rollback mechanisms for recovery.

    10.Secrets and Configurations:
        -Manage sensitive data using Kubernetes Secrets.
        -ConfigMaps for configuration management.

    11.Security Policies:
        -Implement security measures with RBAC, Pod Security Policies, and network policies.

    12.Backup and Disaster Recovery:
        -Establish backup strategies for data and configurations.
        -Plan for disaster recovery scenarios.

    13.Scaling and Optimization:
        -Continuously monitor performance and optimize resource usage.

    14.End-of-Life and Decommissioning:
        -Decommission resources when no longer needed.
        -Archive or delete associated data and configurations.

## K8s Cluster
          
           
    1.Minikube
        -Minikube is a tool designed to run a single-node Kubernetes cluster on your local machine. It is useful for development, testing, and learning purposes, allowing you to experiment with Kubernetes features without the need for a full-scale cluster. Here are some key points about Minikube
    2.Kind
        -KinD, which stands for "Kubernetes in Docker," is a tool designed to run Kubernetes clusters using Docker containers as the underlying nodes.
        -KinD uses Docker containers to simulate individual Kubernetes nodes, making it easy to create multi-node clusters on a single machine.
    3.Kubeadm
        -kubeadm is a command-line tool provided by Kubernetes to simplify the process of setting up and managing a Kubernetes cluster. It is part of the Kubernetes Cluster Lifecycle project and is designed to be a basic building block for creating and configuring Kubernetes clusters. 
    4.EKS
        -Amazon Elastic Kubernetes Service (EKS) is a managed Kubernetes service provided by Amazon Web Services (AWS). It simplifies the deployment, management, and scaling of containerized applications using Kubernetes on AWS infrastructure. EKS abstracts away the complexity of managing the Kubernetes control plane while providing integrations with other AWS services.
    5.GKE
        -Google Kubernetes Engine (GKE) is a managed Kubernetes service provided by Google Cloud Platform (GCP). GKE simplifies the deployment, management, and scaling of containerized applications using Kubernetes.
    6.AKS
        -Azure Kubernetes Service (AKS) is a managed Kubernetes service provided by Microsoft Azure. AKS simplifies the deployment, management, and scaling of containerized applications using Kubernetes on Azure infrastructure. 
...