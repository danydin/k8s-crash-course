# k8s
manage the containers by always checking their status and restarting, increasing, decreasing and so on depends on the needs
resources / components / objects (interchangeable)

# components
## worker node is the computer / brain used to run the contaienrs in our application.
pod is the smallest part in k8s. pod wraps the containers (you can run multiple containers in the same pod if needed)
while pods are running inside a worker node.
* kublet is the service that connects the pod to the worker node for transfering information
* docker is installed and run insside the worker node for the containers to function
* kube-proxy is a service that allows network commuincation inside and outside the worker-node 
## master node
responsible to main the worker nodes
* api server: used to commuincate with the kublet inside the woker node as well as with cli and ui for us to commuincate with the master node
* scheduler: decide where to place/remove pods inside the worker nodes depends on the need
* controller-manager: observe the changes in the worker nodes-pods and inform the scheduler for any changes that occur, like failure or 
## kubernetes cluster 
k8s cluster is the wrapper of everything inside k8s included the master node, the worker node, the pods and all the services that makes it all run together, are all run inside the k8s cluster 
* kubectl: is the cli to interact with k8s cluster and all its services which are mentioned above ^