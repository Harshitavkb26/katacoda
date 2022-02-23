This step describes how to install Chaos Mesh in the production environment.

To check Helm version, execute the following command:
`helm version`{{execute}}

The expected output is as follows:
`version.BuildInfo{Version:"v3.1.2", GitCommit:"d878d4d45863e42fd5cff6743294a11d28a9abce", GitTreeState:"clean", GoVersion:"go1.13.8"}`

## Step 1: Add Chaos Mesh repository​
Add the Chaos Mesh repository to the Helm repository:

`helm repo add chaos-mesh https://charts.chaos-mesh.org`{{execute}}

## Step 2: View the installable versions of Chaos Mesh​
To see charts that can be installed, execute the following command:

`helm search repo chaos-mesh`{{execute}}

## Step 3: Create the namespace to install Chaos Mesh​
The following command installs Chaos Mesh under the `chaos-mesh` namespace. Alternatively, you can specify any namespace to install Chaos Mesh:

`kubectl create ns chaos-mesh`{{execute}}

## Step 4: Install Chaos Mesh in docker
here we are installing chaos mesh in `docker`

`# Default to /var/run/docker.sock
helm install chaos-mesh chaos-mesh/chaos-mesh -n=chaos-mesh --version 2.1.3`{{execute}}

 Moreover, it can be installed in various other environments as well. Additional details are available at their website.  
 https://chaos-mesh.org/docs/production-installation-using-helm/

 `kubectl wait node/controlplane --for condition=running`{{execute}}

## Verify the installation​
To check the running status of Chaos Mesh, execute the following command:

`kubectl get pod -n chaos-mesh`{{execute}}

The expected output is as follows:

`
NAME                                        READY   STATUS    RESTARTS   AGE
chaos-controller-manager-56d8ddb48d-2fcc9   1/1     Running   0          77s
chaos-controller-manager-56d8ddb48d-85tjk   1/1     Running   0          78s
chaos-controller-manager-56d8ddb48d-fdd7b   1/1     Running   0          77s
chaos-daemon-67znl                          1/1     Running   0          78s
chaos-dashboard-85bd7b5cb4-b548g            1/1     Running   0          78s`

🎉 YAY! Chaos Mesh has been successfully installed.