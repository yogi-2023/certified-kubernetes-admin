## 🔹 Pods
- The smallest deployable unit in Kubernetes
- Multi-container pods (sidecar, adapter, ambassador patterns)
- Pod lifecycle and restart policies
  
A Pod is the basic execution unit of a Kubernetes application—the smallest and simplest unit in the Kubernetes object model that you can create or deploy. A Pod represents one or more processes running on your cluster. Cluster is a set of worker nodes that run containerized applications. A Pod encapsulates an application's container(s), associated storage resources, a unique network identity (IP address), and configuration options that govern how the containers should run. A Pod represents a unit of deployment, a single instance of an application in Kubernetes—which may consist of either a single container or a small number of containers that are tightly coupled and share resources.

#### Create a new POD from Nginx Image
```sh
kubectl run nginx --image=nginx
```

#### List  the PODS that are currently running.
```sh
kubectl get pods
```
#### View Logs of a Specific Pod
```sh
kubectl logs nginx
```

#### Describe Pod Information in Detail
```sh
kubectl describe pod nginx
```
#### Connect inside the POD
```sh
kubectl exec -it nginx  -- bash
```

#### Delete the POD
```sh
kubectl delete pod nginx
```

#### View Node Information
```sh
kubectl get nodes

kubectl describe node <add-node-name-here>
```

#### Create 2 Pods as shown in video

```sh
kubectl run nginx-01 --image=nginx
kubectl run nginx-02 --image=nginx
```

#### View Pods with Output of Wide
```sh
kubectl get pods -o wide
```

#### Delete the Pods Created
```sh
kubectl delete pod nginx-01
kubectl delete pod nginx-02
```
