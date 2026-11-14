1. Старт minikube
```
minikube start
```

2. Создание сервисов
```
kubectl run front-end-app --image=nginx --labels=role=front-end --expose --port=80
kubectl run back-end-api-app --image=nginx --labels=role=back-end-api --expose --port=80
kubectl run admin-front-end-app --image=nginx --labels=role=admin-front-end --expose --port=80
kubectl run admin-back-end-api-app --image=nginx --labels=role=admin-back-end-api --expose --port=80
```

3. Применение политики
```
kubectl apply -f ./Task5/non-admin-api-allow.yaml
```