# k8s-multi-node-cluster-vagrant-ansible
Kubernetes Setup Using Ansible and Vagrant
```bash
cd /path/to/Vagrantfile
vagrant up
```
Upon completion of all the above steps, the Kubernetes cluster should be up and running. We can login to the master or worker nodes using Vagrant as follows:

```
## Accessing master
vagrant ssh k8s-master
vagrant@k8s-master:~$ kubectl get nodes
NAME         STATUS   ROLES    AGE     VERSION
k8s-master   Ready    master   18m     v1.13.3
node-1       Ready    <none>   12m     v1.13.3
node-2       Ready    <none>   6m22s   v1.13.3
```
```
## Accessing nodes
vagrant ssh node-1
vagrant ssh node-2
```
