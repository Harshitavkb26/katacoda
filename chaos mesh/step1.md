With this environment the Kubernetes nodes are already configured with `kubeadm` which has been set and configured.

To launch a running kubernetes cluster.
`launch.sh`{{execute}}

after kubernetes cluster started. 

You can get nodes with `kubectl get nodes`{{execute}}

# Great! Now you should have running kubernetes cluster deployed

In the next step, we will learn how to install Chaos Mesh using Helm.