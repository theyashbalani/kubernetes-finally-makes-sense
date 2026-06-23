# Kind Cluster Setup [Local]

[kind](https://kind.sigs.k8s.io/) is a tool for running Kubernetes clusters locally using Docker container as “nodes”.

## Installation [Linux]

Install Docker

```
./installation/docker-install.sh
```

Reboot Server

```
sudo reboot now
```

Check Docker Status

```
systemctl status docker
```

Authenticate Docker

```
docker login
```

Install kind

```
./installation/kind-install.sh
```

Install kubectl

```
./installation/kubectl-install.sh
```

Create a cluster (config is in setup/kind-config.yml)

```
kind create cluster --config setup/kind-config.yml
```

Verify the cluster

```
kubectl cluster-info --context kind-my-k8s-cluster
```
