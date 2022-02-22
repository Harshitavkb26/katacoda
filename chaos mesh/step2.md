This step describes how to install Chaos Mesh in the production environment.

To check Helm version, execute the following command:
`helm version`{{execute}}

The expected output is as follows:
`version.BuildInfo{Version:"v3.5.4", GitCommit:"1b5edb69df3d3a08df77c9902dc17af864ff05d1", GitTreeState:"dirty", GoVersion: "go1.16.3"}`

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

## Verify the installation​
To check the running status of Chaos Mesh, execute the following command:

`kubectl get po -n chaos-mesh`{{execute}}

The expected output is as follows:

`NAME                                        READY   STATUS    RESTARTS   AGE
chaos-controller-manager-69fd5c46c8-xlqpc   3/3     Running   0          2d5h
chaos-daemon-jb8xh                          1/1     Running   0          2d5h
chaos-dashboard-98c4c5f97-tx5ds             1/1     Running   0          2d5h`

🎉 YAY! Chaos Mesh has been successfully installed.