# K8s cluster Architecture

![k8s cluster](https://d33wubrfki0l68.cloudfront.net/152c845f25df8e69dd24dd7b0836a289747e258a/4a1d2/docs/tutorials/kubernetes-basics/public/images/module_02_first_app.svg)

## Master
管理nodes

## Deployment
一個config，告訴k8s如何create和update應用程式instances

## Node (worker)
一個VM或是實體的電腦，在K8s cluster裡當worker，run應用程式。
每個node都有一個 **Kubelet** 作為agent，用來管理node、跟master溝通

## Pod
含有一個或多個應用程式containers(ex: Docker image)，以及以下resources：
1. Shared storage: Volumes
2. Networking: unique cluster IP
3. 其他資訊：image version, port號等等