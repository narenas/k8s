# How to work with services.

## Expose a port
```shell
kubectl expose rs go-demo2 \
  --name=go-demo-2-svc \
  --target-port=28017 \
  --type=NodePort
```
NOTE: you can expose a Deployment, a Service, a ReplicaSet, a ReplicationController or a Pod.

```shell
PORT=$(kubectl get svc go-demo-2-svc \
-o jsonpath="{.spec.ports[0].nodePort}")
```


## Check endpoints of a service
```shell
kubectl get ep go-demo-2 -o yaml
```

## Get all objects in namespace
```shell
kubectl get all
```
