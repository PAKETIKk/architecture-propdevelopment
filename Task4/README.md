| Роль  | Права роли | Группы пользователей |
| --- | --- | --- |
| security-admin | Просмотр, создание, изменение и удаление pods, services, configmaps, deployments, replicasets и statefulsets. Чтение секретов. Изменение секретов не разрешено. | Администраторы ИБ |
| viewer | Просмотр pods, services, configmaps, events, deployments, replicasets и statefulsets в development. Без доступа к секретам | Руководители, менеджеры |
| writer | Просмотр, создание, изменение, удаление pods, services, configmaps, events, deployments, replicasets и statefulsets в development. Без доступа к секретам | Администраторы, DevOps |

1. Старт minikube
```
minikube start
```

2. Создание namespace
```
kubectl create namespace development
```

3. Создание ресурсов в кубе
```
kubectl apply -f ./Task4/users.yaml
kubectl apply -f ./Task4/roles.yaml
kubectl apply -f ./Task4/role-bindings.yaml
```