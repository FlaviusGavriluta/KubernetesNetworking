# Kubernetes networking

## Story

The inner workings of how connections are handled in the IT world can be mysterious, let alone in a Kubernetes environment. Not for long! You are about to investigate it. And your journey starts with checking how the url that you need to make a request to changes, based on using a namespace created by you, or using the default namespace.

## What are you going to learn?

- What is a namespace in k8s
- How the different namespaces work in k8s

## Tasks

1. Create namespace named `kubernetes-network`
    - The namespace `kubernetes-network` exists in your cluster.

2. Install nginx with Helm using the Nginx Stable Helm chart in the _kubernetes-network_ namespace.
    - The nginx Helm chart is deployed in the cluster.
    - The nginx is deployed in the _kubernetes-network_ namespace.

3. Create a pod in the _kubernetes-network_ namespace with `curl` installed.
    - The pod that is running the `curl` image is running on the cluster.
    - The pod is deployed in the _kubernetes-network_ namespace.

4. Create a pod in the `default` namespace with `curl` installed.
    - The pod that is running the `curl` image is running on the cluster.
    - The pod is deployed in the `default` namespace.

5. Make `curl` requests to the nginx server from both of the pods.
    - The response from connecting to nginx is sent back.

## General requirements

None

## Hints

- Use `servicename:port` if your services are in the same namespace. If not, use `servicename.namespacename.svc.cluster.local:port` instead.

## Background materials

- <i class="far fa-exclamation"></i> [Nginx Stable Helm chart](https://docs.nginx.com/nginx-ingress-controller/installation/installation-with-helm/)
- <i class="far fa-exclamation"></i> [Get a Shell to a Running Container](https://kubernetes.io/docs/tasks/debug-application-cluster/get-shell-running-container/)
- <i class="far fa-exclamation"></i> [Kubernetes namespaces](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/)
