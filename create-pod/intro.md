# Creating a Naked Pod

This scenario walks through creating and running a single pod without
a deployment. The point is to do it as fast as possible. Updated again. trying to figure out the markdown

```
This is a code block
```

`this is more code`
<pre class="file" data-target="clipboard">
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
</pre>

<pre>
This is inside the pre tag
</pre>

Version 0.1