# kubectl commands

## Pods
```
kubectl get pods

kubectl run --help

kubectl run nginx --image=nginx

kubectl describe pod pod-name

kubectl get pods -o wide

kubectl delete pod pod-name

kubectl run redis --image=redis123 --dry-run=client -o yaml > redis.yaml

kubectl create -f redis.yaml

kubectl apply -f redis.yaml
```

## ReplicaSets
```
kubectl create -f replicaset-definition.yaml

kubectl get replicaset

kubectl delete replicaset myapp-replicaset # also deletes all underlying pods

kubectl replace -f replicaset-definition.yaml

kubectl scale -f replicaset-defintion.yaml --replicas=5
```

## Deployments
```
kubectl create -f deployment-definition.yaml

kubectl get deployments

kubectl describe deployment myapp-deployment

kubectl edit deployment myapp-deployment --record

kubectl set image deployment/nginx-deployment nginx-pod=nginx:1.23 --record

kubectl rollout status deployment/nginx-deployment

kubectl rollout history deployment/nginx-deployment
```

## Services
```
minikube service myapp-service --url
```

## Commmon
```
# delete all kubernetes components from current namespace
kubectl delete all --all

# delete all kubernetes components from specific namespace
kubectl delete all --all -n namespace
```