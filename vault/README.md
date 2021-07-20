В первую очередь создаем сикрет с ключём и сертификатом CA. Что бы не мучиться берем их из текущей версии кубера.

kubectl -n vault create secret tls kube-ca-secret \
--cert=/etc/kubernetes/ssl/ca.crt \
--key=/etc/kubernetes/ssl/ca.key

Изучаем файл certs.yaml. В файле используются CRD, добавленные при установке certmanager.

Применяем файл.

kubectl -n vault get issuers
kubectl -n vault get certificate

