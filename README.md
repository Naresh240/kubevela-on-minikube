# kubevela-on-minikube

## Minikube setup

[minikube-setup](https://github.com/Naresh240/kubernetes/tree/main/minikube-setup)

## Enable ingress on  Minikube

```bash
minikube addons enable ingress
```

## Install KubeVela CLI

```bash
curl -fsSl https://kubevela.net/script/install.sh | bash
export PATH=$PATH:/usr/local/bin
```

## Install KubeVela

```bash
helm repo add kubevela https://charts.kubevela.net/core
helm repo update
helm install --create-namespace -n vela-system kubevela kubevela/vela-core --wait
```

## Adding VelaUX to see UI

```bash
vela addon enable velaux
vela addon enable velaux serviceType=NodePort
```

## default username and password:
```bash
username: admin
password: VelaUX12345
```

## Deploy nginx deployment with vela

```bash
vela up -f nginx.yaml
```

## Check pods and services

```bash
kubectl get pods
kubectl get svc
```

## Few kubevela commands

```bash
vela show webservice
vela components list
vela taints list
```
