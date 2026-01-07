# Day 1 – Linux & Kubernetes Environment Setup

## Objective
Set up a local cloud-native lab using Kali Linux and Kubernetes (Minikube) to study Linux networking concepts in an isolated environment.

## Tasks Performed
- Installed and verified Docker
- Installed Minikube and kubectl
- Started Minikube cluster
- Verified Kubernetes node and pod networking

## Commands Used
```bash
minikube start
kubectl get nodes -o wide
kubectl get pods -A
```
## Issues Faced
- kubectl segmentation fault due to corrupted binary
- Fixed by reinstalling kubectl and resetting Minikube
- Key Learnings
- Kubernetes uses Linux namespaces and cgroups
- Pods act as isolated Linux environments
- Minikube simulates cloud control plane locally
