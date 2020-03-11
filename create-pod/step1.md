## Check that Minikube is started
Minikube should be started at this point. Test it by trying
to get some information from kubectl.
`kubectl get all`{{execute}}
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