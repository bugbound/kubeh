# kubeh
we are b0rg

An example of seting up a simple 1 node Kubernetes instance in AWS and using it to run bug bounty/pentesting tools.
This could be used to run from home hardware but not recommended due to the extra task of proxying out data, when you start automation from your ip it will get blocked by akamai/cloudflare at some point...dont get your home ip blocked!
I tried wrapping go programs around proxychains but go managed to bypass and connect out directly.
If we run one node in aws it can qualify under the free tier mode as long as you dont send more than 15gb of data a month!

In this example we run k3s, a stripped down lighter version of the full blown Kubernetes.
In future i may try k8s as suggested by ssh banner upon login of aws node.
kubectl should still work the same.

## kubectl commands
```
kubectl get nodes
kubectl get pods
kubectl get pods --watch
kubectl get pods --all-namespaces
kubectl logs -f <pod-name>
kubectl get services
kubectl get jobs
kubectl get deployments
```

### run a new pod and execute bash
```kubectl run- my-shell --rm -i --tty --image golang:1.13 -- bash```

### run command on existing pod and execute bash
```kubectl exec --stdin --tty pod-name-here-1234 -- /bin/bash```

### Apply Manifest
```kubectl apply -f 0100-SimpleHTTPServer.yaml```

### Remove Manifest (kills pods)
```kubectl delete -f 0100-SimpleHTTPServer.yaml```

