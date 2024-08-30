# 🚀 K8s Introduction
Kubernetes (often abbreviated as K8s) is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications. Originally developed by Google, it is now maintained by the Cloud Native Computing Foundation (CNCF).

## 📦 Key Concepts of Kubernetes
### 1. Containerization🐳

Containers are lightweight, portable units that package an application along with its dependencies, ensuring consistency across different environments. Kubernetes helps manage these containers at scale.

### 2. Cluster Architecture

#### Master Node🧠: 
The control plane of a Kubernetes cluster. It manages the state of the cluster, orchestrates the scheduling of containers, and handles the API requests
#### Components:
**kube-apiserver: 
The front-end for the Kubernetes control plane, responsible for handling API requests.

**etcd: 
A key-value store that holds the state and configuration data of the cluster.

**kube-scheduler: 
Determines on which node a newly created Pod should run based on resource availability and other constraints.

**kube-controller-manager: 
Runs various controllers that ensure the desired state of the cluster (e.g., node management, replication, etc.).

**cloud-controller-manager: 
Manages cloud-specific control logic.

#### Worker Nodes⚙️: 
The nodes where the application workloads run. Each node runs at least one container runtime (like Docker), and the following Kubernetes components:

**kubelet: 
An agent that runs on each worker node, ensuring containers are running as expected.

**kube-proxy: 
Manages network rules on each node, ensuring that communication to and from containers happens as intended.

**Container Runtime: 
Software that runs the containers, e.g., Docker, containerd.
Pods

### 3. Pods🎯

The smallest and simplest Kubernetes object. A Pod represents a single instance of a running process in a cluster and can contain one or more containers. Pods are ephemeral and designed to be replaceable.

### 4. Services📡
An abstraction that defines a logical set of Pods and a policy for accessing them. Services enable communication between Pods and can expose them to the external world.

### 5. Volumes📂
A directory accessible to containers in a Pod, used for data storage. Different types of volumes exist, including Persistent Volumes, EmptyDir, and HostPath.

### 6. Deployments🚀

A higher-level abstraction for managing Pods. A Deployment ensures a specified number of Pod replicas are running and provides mechanisms for rolling updates and rollbacks.

### 7. ReplicaSets📈

A Kubernetes controller that ensures a specified number of Pod replicas are running at any given time. ReplicaSets are usually managed by Deployments.

### 8. Namespaces 🏷️

Provide a mechanism to divide cluster resources between multiple users (via resource quotas) or to isolate environments, e.g., dev, staging, production.

### 9. ConfigMaps and Secrets🔐

ConfigMaps: Used to inject configuration data into Pods in a decoupled manner.
Secrets: Similar to ConfigMaps but specifically designed to store sensitive information like passwords, API keys, etc.

### 10.Ingress🌐

Manages external access to services in a cluster, typically HTTP/HTTPS. Ingress controllers (e.g., NGINX, Traefik) manage this functionality.


### 11. KubeDNS/CoreDNS🧭

Provides internal DNS services to allow Pods to discover services by name.

### 12. Helm🛠️

A package manager for Kubernetes that helps in managing Kubernetes applications with Helm Charts, which are pre-configured Kubernetes resources.

## Benefits of Kubernetes

**Scalability📈: Automatically scale your applications based on demand.

**High Availability🟢: Ensures that your applications are highly available by automatically replacing failed Pods.

**Portability🏗️: Run your workloads consistently across different environments (on-premises, cloud, hybrid).

**Self-Healing💪: Automatically replaces and reschedules containers that fail, are unresponsive, or don’t meet the health check requirements.

**Declarative Configuration📝: Manage and automate your infrastructure using declarative YAML or JSON files.

## Use Cases

**Microservices🧩: Orchestrating and scaling microservices-based applications.

**CI/CD Pipelines🔄: Running continuous integration and continuous deployment pipelines.

**Big Data & Machine Learning🧠: Scaling workloads like big data processing and machine learning model training.

**Hybrid and Multi-Cloud☁️: Managing applications across on-premises and multiple cloud environments.