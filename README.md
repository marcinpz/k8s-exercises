# k8s-exercises

Kubernetes exercises - using [runme](https://runme.dev/).

## What is Kubernetes?
- **Definition**: Kubernetes (K8s) is an open-source platform for automating deployment, scaling, and management of containerized applications.
- **Purpose**: Simplifies orchestration of containers, ensuring high availability, scalability, and resilience.
- **Origin**: Developed by Google, open-sourced in 2014, maintained by the Cloud Native Computing Foundation (CNCF).

## Core Concepts
- **Cluster**: A set of nodes running containerized applications managed by Kubernetes.
- **Pod**: Smallest deployable unit, containing one or more containers sharing storage/network.
- **Node**: Worker machine (physical or virtual) running Pods.
- **Control Plane**: Manages the cluster (e.g., API Server, Scheduler).
- **Workload Resources**:
  - **Deployment**: Manages stateless apps with replicas and updates.
  - **StatefulSet**: Manages stateful apps with persistent identities.
  - **DaemonSet**: Runs a Pod on every node.

## Key Features
- **Self-Healing**: Restarts failed containers, reschedules Pods, kills unresponsive ones.
- **Auto-Scaling**: Horizontal Pod Autoscaler (HPA) adjusts Pod count based on CPU/memory.
- **Service Discovery & Load Balancing**: Routes traffic to Pods automatically.
- **Storage Orchestration**: Mounts storage (local or cloud) to Pods.
- **Declarative Configuration**: Define state in YAML/JSON, applied via `kubectl`.

## Architecture
- **Control Plane Components**:
  - **API Server**: Exposes Kubernetes API, cluster control frontend.
  - **etcd**: Distributed key-value store for cluster data.
  - **Scheduler**: Assigns Pods to nodes based on resources.
  - **Controller Manager**: Runs controllers to maintain desired state.
- **Node Components**:
  - **Kubelet**: Ensures containers in Pods are running.
  - **Kube-Proxy**: Manages network rules.
  - **Container Runtime**: Runs containers (e.g., Docker, containerd).

## Basic Commands
- `kubectl get pods`: Lists all Pods.
- `kubectl apply -f file.yaml`: Applies a configuration file.
- `kubectl describe pod <pod-name>`: Shows Pod details.
- `kubectl scale deployment <name> --replicas=3`: Scales a Deployment.
