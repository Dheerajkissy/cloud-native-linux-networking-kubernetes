## Day 4 – Self-Healing Firewall & Network Debugging

### Objective
Design a firewall pod and understand self-healing behavior in Kubernetes.

### Concepts Learned
- Pod lifecycle and self-healing
- iptables basics inside containers
- Network traffic inspection using tcpdump
- Kubernetes automatically recreates failed pods

### Commands Practiced
- kubectl apply -f <yaml>
- kubectl delete pod <pod-name>
- kubectl get pods -w
- tcpdump
- ss -s
- ip -s link

### Tasks Performed
- Implemented firewall pod using iptables
- Applied traffic filtering rules
- Killed pods manually to test auto-recovery
- Observed traffic using tcpdump and ss
### Practical Work
- Deployed firewall pod
- Tested connectivity between pods
- Captured packets using tcpdump
- Deleted pod and observed auto-recreation
- Verified cluster stability after pod failure

### Issues Faced
- YAML syntax errors
- Permission issues with tcpdump
- DNS resolution failures after pod deletion

### Key Takeaways
- Kubernetes ensures high availability automatically
- Networking failures are easier to debug with Linux tools
- Firewalls can be implemented at pod level
## Commands Used
```bash
iptables -A INPUT -j DROP
kubectl delete pod <pod-name>
tcpdump -i eth0
ss -s
