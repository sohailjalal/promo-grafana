# prom-grafana

## This is how to deploy grafana and promethues helm charts

## Deploy Grafana 
```
cd grafana
kubectl create namespace monitoring
helm install --name release1 --namespace monitoring .
```



## Deploy prometheus 
```
cd prometheus
kubectl create namespace monitoring
helm install --name release2 --namespace monitoring .
```


- if you need to modify the retention period just modify the values.yaml file and modify the 
```
  prometheusSpec:
    retention: 35d
```
```
helm upgrade release2 .
```


































