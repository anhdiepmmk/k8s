# I. Imperative
## 1. build docker image
```
docker build -t anhdiepmmk/kub-first-app .
```
## 2. push image to docker hub
```
docker push anhdiepmmk/kub-first-app
```
## 3. create deployment
```
kubectl create deployment first-app --image=anhdiepmmk/kub-first-app
```

## 4. expose deployment
> Service help us can communicate with pods
```
kubectl expose deployment first-app --type=LoadBalancer --port=8080
```

## 5. access our service
```
minikube service first-app
```

## 6. make our service HA
```
kubectl scale deployment/first-app --replicas=5
```

## 7. update deployment
> k8s just update image if the new image have diffrence tag
```
kubectl set image deployment/first-app kub-first-app=anhdiepmmk/kub-first-app:latest
```

## 8. view current update status
```
kubectl rollout status deployment/first-app
```

## 9. rollback deployment
```
kubectl rollout undo deployment/first-app
kubectl rollout undo deployment/first-app --to-revision=1
```

## 10. rollout history
```
kubectl rollout history deployment/first-app
kubectl rollout history deployment/first-app --revision=3
```

## 11. delete service
```
kubectl delete service first-app
```

## 12. delete deployment
```
kubectl delete deployment first-app
```

# II. Declarative
## 