# Docker Swarm

- - - -

## Table of Contents

* [Overview](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Docker/kubernetes.md#overview)
* [History](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Docker/kubernetes.md#history)
* [General concepts](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Docker/kubernetes.md#general-concepts)

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
