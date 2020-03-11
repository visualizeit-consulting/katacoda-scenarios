#Creating a Naked Pod.

This scenario walks through creating and running a single pod without
a deployment. The point is to do it as fast as possible.

## Create a pod yaml file
The following template can be found at [Pod Templates](https://kubernetes.io/docs/concepts/workloads/pods/pod-overview/#pod-templates)
```
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod
  labels:
    app: myapp
spec:
  containers:
  - name: myapp-container
    image: busybox
    command: ['sh', '-c', 'echo Hello Kubernetes! && sleep 3600']
```