# Kubernetes

## 1. Kubernetes Components 

## 2. Networking / Service

> Service is a resource that defines a logical set of Pods and a policy to access those Pods. It provides an abstract way to expose an application as a set of accessible endpoints.

### 3. Types of services
- `ClusterIP` Exposes the Service on a cluster-internal IP. Choosing this value makes the Service only reachable from within the cluster. This is the default that is used if you don't explicitly specify a type for a Service. You can expose the Service to the public internet using an *``Ingress``* or a *``Gateway``*.
- `NodePort` Exposes the Service on each Node's IP at a static port (the NodePort). To make the node port available, Kubernetes sets up a cluster IP address, the same as if you had requested a Service of type: ClusterIP.
- `LoadBalancer` Exposes the Service externally using an external load balancer. Kubernetes does not directly offer a load balancing component; you must provide one, or you can integrate your Kubernetes cluster with a cloud provider.
- ``ExternalName`` Maps the Service to the contents of the externalName field (for example, to the hostname api.foo.bar.example). The mapping configures your cluster's DNS server to return a CNAME record with that external hostname value. No proxying of any kind is set up.

### 2. Deployment vs. StatefulSet vs. DaemonSet 
- `Deployment`
  - in Kubernetes is used to manage distributed applications. It defines how applications are deployed and updated.
  - It's useful for applications that do not maintain a specific state or need to be easily scalable. For example, web applications, RESTful services, etc.
  - A Deployment manages a replicated set of Pods (one or more instances) and allows for zero-downtime updates, version rolling, and rollback to previous versions.
- `StatefulSet` 
  - in Kubernetes is a controller used for applications that require persistent storage and unique identity.
  - It provides ordering guarantees and unique identities for each instance of the application (like a database), allowing each to have a stable, persistent name.
- `DaemonSet` 
  - is a controller used to ensure that all (or some) nodes in the Kubernetes cluster run a specific copy of a Pod.
  - It's useful for infrastructure tasks like log collection, monitoring, network storage, which need to run on every node or a specific set of nodes.
  - It ensures that a specific Pod runs on each node and can be used for low-level system tasks needed on all nodes in the cluster.



