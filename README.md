# Kestra K8s

Kestra is a workflow orchestrator and scheduler for data pipelines. It is designed to manage and execute complex workflows with ease.

## Description

This project is the deployment of Kestra on Kubernetes. It includes a Helm chart to simplify the deployment.

## Prerequisites

* An ongoing Kubernetes cluster with Traefik configured
* Helm 3
* kubectl

## Installation

1. Download the Kestra Helm chart.

```sh
helm repo add kestra https://helm.kestra.io/
```

2. Run the kestra helm chart.

```sh
helm install my-kestra kestra/kestra -n <kestra-namespace>
```

3. Run the traefik kubernetes ingress.

```sh
kubectl apply -f ingress.yaml
```

You should now find the Kestra website at the following URL: `http://<traefik-external-ip>`.
