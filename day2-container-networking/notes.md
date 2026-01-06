## Day 2 – Container & Linux Networking

### Objective
Understand how containers use Linux networking primitives such as namespaces,
virtual Ethernet pairs, bridges, and routing.

### Concepts Learned
- Network namespaces isolate network stacks
- veth pairs act as virtual cables between namespaces
- Linux bridge enables L2 connectivity
- Containers rely on kernel networking features

### Key Commands Practiced
- ip addr, ip link
- ip netns
- ip route
- ping, traceroute
- brctl / bridge

### Practical Work
- Observed Docker bridge (docker0)
- Analyzed container IP assignment
- Verified container-to-host connectivity
- Inspected routing tables inside namespaces

### Issues Faced
- Permission errors when capturing packets
- Understanding veth interface mapping

### Key Takeaways
- Containers are not VMs; they share the host kernel
- Networking isolation is achieved using namespaces
- Linux networking knowledge is essential for Kubernetes
