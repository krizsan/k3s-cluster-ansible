# k3s-cluster-ansible
Ansible role that automates the creation of a K3S cluster running in Multipass virtual machines.

Usage
-----
From the root of this project:
1. Install the collection:<br/>
   ```ansible-galaxy collection install k3s_cluster --force```
2. Create a K3S cluster running in Multipass VMs as specified in the inventory.yml file in project root:<br/>
   ```ansible-playbook -i inventory.yml k3s-cluster-create.yml```
3. Update kubectl configuration on the local computer as to manage the K3S cluster:<br/>
   ```ansible-playbook -i inventory.yml kubectl-local-config.yml```
4. Verify K3S cluster:<br/>
   ```kubectl cluster-info```<br/>
   ```kubectl get nodes```<br/>
5. Tear down the K3S cluster including deleting the Multipass VMs:<br/>
   ```ansible-playbook -i inventory.yml k3s-cluster-teardown.yml```

<br/><br/>
The K3S cluster is defined in the inventory.yml file. Currently only one master node per cluster is supported.
<br/><br/>
Please refer to the README in the k3scluster role (k3s_cluster/roles/k3scluster/README.md)
for instructions on how to set up a K3S cluster using Molecule.
