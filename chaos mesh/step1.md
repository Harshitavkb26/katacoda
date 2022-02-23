With this environment the Kubernetes nodes are already configured with `kubeadm` which has been set and configured.

To launch a running kubernetes cluster.
`launch.sh`{{execute}}

after kubernetes cluster started. 

You can get nodes with `kubectl get nodes`{{execute}}

The expected output is as follows:
`NAME           STATUS   ROLES    AGE   VERSION
controlplane   Ready    master   51s   v1.18.0
node01         Ready    <none>   22s   v1.18.0`

# Great! Now you should have running kubernetes cluster deployed

In the next step, we will learn how to install Chaos Mesh using Helm.