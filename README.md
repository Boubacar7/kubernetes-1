# kubernetes Bare Metal
Kubernetes install bare metal

## 1. File docker-compose on Kubernetes Master
## SET variables of the file docker-compose-kube-master.yml
```
- ETCD_SERVER=<dns_name_etcd_server>
- APISERVER_IP=<dns_name_api_kubernetes>
- CLUSTER_NAME=<cluster_name>
```

## 2. File docker-compose on Kubernetes Worker (Minion)
## SET variables of the file docker-compose-kube-master.yml
```
hostname: <hostname_minio>
- ETCD_SERVER=<dns_name_etcd_server>
- ETCD_PREFIX=<prefix_network_etcd>
- CLUSTER_NAME=<cluster_name>
- APISERVER_IP=<dns_name_api_kubernetes>
- HOSTNAME_OVERRIDE=<hostname_minio>
```