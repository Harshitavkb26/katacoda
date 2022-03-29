## 2. Install basic tools

Kubernetes is written in Go. Building and developing Kubernetes requires a very recent version of Go.[This table](https://github.com/kubernetes/community/blob/master/contributors/devel/development.md#go) lists the required Go versions for different versions of Kubernetes. 
### Installing GO
first we download the tarball archive of the go compiler.
`sudo curl -O https://storage.googleapis.com/golang/go1.17.linux-amd64.tar.gz`{{execute}} 

The next step is to extract the contents of the archive. We can use the command as:

`sudo tar -xvf go1.17.linux-amd64.tar.gz`{{execute}} 

The command above should extract the archive and create a directory called to go.

The next step is to set the path for go. This allows the go executable to be accessible outside the main go directory or without an absolute path.
 also remove any previous installation of go.

`sudo rm -rf /usr/local/go`{{execute}}

For convenience, we can move the go directory to a more reasonable directory as:

`sudo mv go /usr/local`{{execute}}

### Installing make (Ubuntu/Debian)

 to install essential files run the following command:-
 
`sudo apt-get install build-essential`{{execute}}