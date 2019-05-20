# k8s-multi-node-cluster-vagrant-ansible
[Kubernetes Setup Using Ansible and Vagrant](https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/)

### Prerequisites

* Vagrant should be installed on your machine. Installation binaries can be found here.
* Oracle VirtualBox can be used as a Vagrant provider or make use of similar providers as described in Vagrant’s official documentation.
* Ansible should be installed in your machine. Refer to the Ansible installation guide for platform specific installation.

### Steps

Clone the repository
```bash
git clone https://github.com/djmathew/k8s-multi-node-cluster-vagrant-ansible.git
```
Upon cloning the repository with Vagrantfile and playbooks follow the below steps.
```bash
cd /path/to/Vagrantfile
vagrant up
```
Upon completion of all the above steps, the Kubernetes cluster should be up and running. We can login to the master or worker nodes using Vagrant as follows:

```bash
## Accessing master
vagrant ssh k8s-master
vagrant@k8s-master:~$ kubectl get nodes
NAME         STATUS   ROLES    AGE     VERSION
k8s-master   Ready    master   18m     v1.13.3
node-1       Ready    <none>   12m     v1.13.3
node-2       Ready    <none>   6m22s   v1.13.3
```
```bash
## Accessing nodes
vagrant ssh node-1
vagrant ssh node-2
```
