Cloning a GitHub repository creates a local copy of the remote repo. When we clone a repository, all the files are downloaded to the local machine but the remote git repository remains unchanged.

This allows you to make all of your edits locally rather than directly in the source files of the origin repo.
 To clone a repository we can use `git clone` command

 Here's the command to clone kubernetes repository.

 `git clone https://github.com/kubernetes/kubernetes `{{execute}}

 NOTE :- Kubernetes is a large project, and compiling it can use a lot of resources. We recommend the following for any physical or virtual machine being used for building Kubernetes.

   * 8GB of RAM
   * 50GB of free disk space

   when you clone repository  on local machine  wait for some time (40-50 minutes expected).


but if hardware recommandation are not fullfilled then you can use `--depth` flag it will generate a shallow repository which doesn't require any specific system configuration.
you can use the following command to create a shallow clone.

`git clone https://github.com/kubernetes/kubernetes --depth 1`

after cloning change the directory
`cd kubernetes`{{execute}}