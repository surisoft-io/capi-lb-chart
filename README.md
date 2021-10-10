[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

# CAPI Gateway Helm Charts

### Prerequisites
  - Kubernetes 1.9.2+
  - Helm v3.3.1

### Test with default localhost self signed certificates
```sh
helm install capi-gateway ./capi-charts
```

### Check if CAPI is running
```sh
kubectl get svc
```

Ouput:
```sh
NAME         TYPE           CLUSTER-IP       EXTERNAL-IP   PORT(S)                                        AGE
capi         LoadBalancer   10.111.249.46    localhost     8380:30988/TCP                                 4h9m
capi-rest    LoadBalancer   10.96.49.226     localhost     8080:31293/TCP                                 4h9m
grafana      LoadBalancer   10.108.115.248   localhost     3000:31073/TCP                                 4h9m
kafka        LoadBalancer   10.101.68.186    localhost     9092:30829/TCP                                 4h9m
keycloak     LoadBalancer   10.99.2.144      localhost     8443:31981/TCP,9990:31361/TCP                  4h9m
kubernetes   ClusterIP      10.96.0.1        <none>        443/TCP                                        4d
mongo        LoadBalancer   10.108.75.56     localhost     27017:30233/TCP                                4h9m
prometheus   LoadBalancer   10.97.22.85      localhost     9090:31291/TCP                                 4h9m
zipkin       LoadBalancer   10.100.191.219   localhost     9411:30057/TCP                                 4h9m
zookeeper    LoadBalancer   10.106.123.93    localhost     2181:31171/TCP,2888:31428/TCP,3888:31307/TCP   4h9m
```