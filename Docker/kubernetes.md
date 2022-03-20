# Docker Swarm

- - - -

## Table of Contents

* [Overview](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Docker/kubernetes.md#overview)
* [History](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Docker/kubernetes.md#history)
* [General concepts](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Docker/kubernetes.md#general-concepts)
* [kubectl](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Docker/kubernetes.md#kubectl)

## Overview

* Kubernetes (also called K8s) is an open source system for automating deployment, scaling and management of containerized applications
* Kubernetes is often described as orchestrating these containers
* Kubernetes can manage:
  * Load balancing
  * Storage orchestration
  * Automated rollouts and rollbacks
  * Self healing
  * Secret and configuration management
  * Horizontal scaling
* Benefits of using Kubernetes include:
  * Environment consistency
  * Shipping software faster
  * Eliminate app conflicts
  * Zero-downtime deployments
  * Orchestrates containers
  * Self-healing

## History

* Container and cluster management system was needed
* Internally used by Google for 15 years before being donated to the Cloud Native Computing Foundation
* It is now an open source project and supported by all major cloud platforms
* Allows for declarative configuration, e.g. I want `n` number of instances of this particular container running at all times

## General concepts

* One or more master nodes manage the worker nodes
* Worker nodes can be VMs or physical servers
* Together the worker and master node create a cluster
* Worker nodes contain Pods
* Pods "package" containers
* __etcd store:__ Data store for everything the master node needs to track
* __Controller manager:__ Manages incoming requests using Scheduler
* Worker nodes each have:
  * Kubelet which is used for communicating to the master node
  * Container run time
  * Kube-Proxy

## kubectl

* kubectl is a command line tool for sending requests to master node
* Master node then uses the scheduler for enacting requests

### Commands

* `kubectl cluster-info` : View cluster information
* `kubectl get all` : Get all information about Kubernetes pods, deployments, services and more
* `kubectl run <podName> --image=nginx:apline` : Run the nginx:apline container in a Pod
* `kubectl port-forward <podName> 8080:80` : Pods and containers are accessible within the Kubernetes cluster only by default. This exposes a container port externally

## Pods

* A pod is a basic execution unit of a kubernetes application
* It is the smallest /simplest unit in the Kubernetes object model you can create and deploy
* A Pod is an environment for containers
* You can organise parts of applications into pods (e.g. server, caching, APIs, database each in their own Pod)
* Each has a Pod IP, memory, volumes etc, shared across containers
* Pods scale horizontally by adding Pod replicas
* Pods live and die but never come back to life
* Pods do NOT span multiple nodes
* Pod containers share the same network namespace (IP/ port)
* Pod containers have the same loopback network interface (localhost)
* Container processes need to bind to different ports within a pod
* Can run a pod via they kubectl command line or with a YAML file
* If you delete a Pod, a new one will be recreated because of the Kubernetes deployment
* You would need to delete the deployment which is managing the Pods first of all
