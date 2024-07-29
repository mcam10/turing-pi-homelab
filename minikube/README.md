# Local Pihole Instance using Minikube

## Preqs

Minikube + Ingress + Metallb Addons.

Nginx ingress: https://minikube.sigs.k8s.io/docs/tutorials/custom_cert_ingress/

Metallb for L4 load balancer:

https://kubebyexample.com/learning-paths/metallb/install

Mkcert for local certs:
https://github.com/FiloSottile/mkcert


## Installation

Follow the guide for helm [chart](https://github.com/MoJo2600/pihole-kubernetes) to install Pihole.

```bash
helm repo add mojo2600 https://mojo2600.github.io/pihole-kubernetes/
helm repo update
```

## Usage

```bash
helm install local-pihole mojo2600/pihole -f pi-hole-helm-values.yaml
``
