## Deployments
It is a kubernetes object which the declarative updates for Pods and ReplicaSets

### Create Deployment

```
kubectl create -f https://raw.githubusercontent.com/ssts-alg/kubernetes/master/deployments/deployments.yml --record=true
```

### Check status of the current deployment

```
kubectl rollout status deployment myapp
```

### Updating deployment
For example we want to change number of replicas, change replicas in yaml and run following command

```
kubectl apply -f https://raw.githubusercontent.com/ssts-alg/kubernetes/master/deployments/deployments.yml  --record=true
```

### Kubernetes Deployment revisions
Kubernetes maintains deployment state of all versions

inorder to see deployment revision history

```
kubectl rollout history deployment myapp
```

### Undo recent deployment

```
kubectl rollout undo deployment myapp
```

### rollback to specific deployment revision

```
kubectl rollout undo deployment myapp --to-revision=1
```
