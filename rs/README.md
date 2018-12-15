# How to use ReplicaSets

* Creare a rs from go-demo2.yml
```shell
  kubectl create -f go-demo2.yml
```

* Delete rs from go-demo2.yml
```shell
  kubectl delete -f go-demo2.yml --cascade=false
```
This operation don´t delete containers, just the rs itself.

* Get rs
```shell
  kubectl get rs
```

* Use save-config for laters definition updates for objects
```shell
  kubectl create -f go-demo-2.yml --save-config
```

* Updating rs
```shell
  kubectl apply -f go-demo-2-scaled.yml
```

* Get pods/objects names
```shell
  kubectl get pods -o name
```

* Remove label from rs/obkect
```shell
  kubectl label $POD_NAME service-
```

In order to delete a label, suffix the label with -

* Show pods labels
```shell
  kubectl get pods --show-labels 
```
