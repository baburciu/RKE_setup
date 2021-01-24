# RKE_setup
Satisfying Rancher requirements for Kubernetes cluster setup on Ubuntu 18.04 LTS bare metal VMs and have a way to clear leftovers once RKE cluster is deleted

## Apply prerequisites for nodes to be part of manual RKE cluster or RKE cluster created via Rancher server:

[boburciu@r220 ~]$ ` cd /home/boburciu/Rancher_K8s_prereq ` <br/>
[boburciu@r220 Rancher_K8s_prereq]$ <br/>
[boburciu@r220 Rancher_K8s_prereq]$ ` ansible-playbook Rancher_prereq_setup.yml -v `


## Clear leftover containers and dirs after an RKE cluster delete (with either __rke remove__ or via Rancher server UI), following [official guide](https://rancher.com/docs/rancher/v2.x/en/cluster-admin/cleaning-cluster-nodes/)

[boburciu@r220 Rancher_K8s_prereq]$ ` ansible-playbook Rancher_leftovers_remove.yml -v `
