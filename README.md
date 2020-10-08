# Docker Node MongoDB Example on MiniKube


## Quick Start

```bash
# Run in Docker
docker build -t <dockerRepository>/dockernodemongodb:<tag> .
docker push <dockerRepository>/dockernodemongodb:<tag>

# install MongoDB
helm repo add bitnami https://charts.bitnami.com/bitnami
helm install my-release bitnami/mongodb

# install dockernodemongodb
helm upgrade --install --namespace default dockernodemongodb ./charts/

# port forwarding
kubectl port-forward <pod name> 8080:3000 
```
