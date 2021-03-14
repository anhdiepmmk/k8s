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

# II. Declarative
## 