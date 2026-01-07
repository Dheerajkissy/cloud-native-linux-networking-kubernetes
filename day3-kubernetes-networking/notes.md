## Day 3 – Kubernetes Networking

### Objective
Understand Kubernetes cluster networking, pod communication,
and service discovery.

### Concepts Learned
- Pod-to-pod communication without NAT
- Cluster IP addressing
- kube-proxy and service routing
- CNI (Container Network Interface) role

### Commands Practiced
- kubectl get nodes -o wide
- kubectl get pods -A
- kubectl exec -it <pod> -- /bin/sh
- kubectl describe pod
- kubectl logs

### Commands Used
```bash
sysctl -w net.ipv4.ip_forward=1
ip route
```
### Practical Work
- Deployed multiple pods
- Verified pod IP allocation
- Tested inter-pod communication using ping
- Observed DNS resolution behavior
- Used kubectl exec for debugging

## Tasks Performed
- Created a privileged Linux router pod
- Enabled IP forwarding
- Tested inter-pod connectivity

### Issues Faced
- kubectl segmentation fault issue
- DNS name resolution failure
- Pod restarts during testing

### Key Takeaways
- Every pod gets a unique IP
- Kubernetes networking is flat and scalable
- Debugging requires understanding Linux + Kubernetes together
