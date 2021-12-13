# kube-csvserver

Pre-requisite : Kubernetes cluster up and running 

Unique Cname for csvserver :

csvserver-ss-0.csvserver-h.default.svc.cluster.local

Handy commands for creating/deleteing csvserver objects -

**Config maps**:
---------------------------------------------------------------
Create

```
kubectl create -f env-config-map.yml

kubectl create -f inputfile-config-map.yml

kubectl create -f prometheus-config-map.yml
```

Delete

```
kubectl delete -f env-config-map.yml

kubectl delete -f inputfile-config-map.yml

kubectl delete -f prometheus-config-map.yml
```
---------------------------------------------------------------

**CsvServer** :
---------------------------------------------------------------
Create

```
kubectl create -f csvserver-statefulset.yml

kubectl create -f csvserver-app-service.yml

kubectl create -f csvserver-headless-service.yml
```

Delete

```
kubectl delete -f csvserver-statefulset.yml

kubectl delete -f csvserver-app-service.yml

kubectl delete -f csvserver-headless-service.yml
```
---------------------------------------------------------------

**prometheus** :
---------------------------------------------------------------
Create

```
kubectl create -f prometheus-deploy.yml

kubectl create -f prometheus-service.yml
```


Delete

```
kubectl delete -f prometheus-deploy.yml

kubectl delete -f prometheus-service.yml
```
---------------------------------------------------------------
