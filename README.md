# k8s
## Reloader

reloader.yaml - Reloader - утилита для перезагрузки сервиса после изменения comfigMap. Образ на DockerHub.

На что обратить внимание:

    Переменная среды окружения KUBERNETES_NAMESPACE. Если не определена, работает со всеми namespace кластера.
    Аргумент командной строки --namespaces-to-ignore - можно перечислить через запятую имена namespace, которые программа будет игнорировать.

## Metrics server

metrics-server.yaml

```YML
Metrics Server - собирает метрики по использованию CPU и RAM. Добавляет metrics API, используемый в инструментах горизонтального масштабирования подов.
```



## Cert-manager
```YML
cert-manager - утилита для управления сертификатами.

kubectl apply -f https://github.com/jetstack/cert-manager/releases/download/v1.2.0/cert-manager.yaml
kubectl get pods --namespace cert-manager

Namespace cert-manager создаётся автоматически.
```
## Persistent Volumes
nfs.yaml
```YML
https://github.com/kubernetes-sigs/nfs-subdir-external-provisioner

Определение классов, постоянных хранилищ и всё что с этим связано.

Необходимо отредактировать деплоймент в части указания правильных параметров nfs сервера
```
