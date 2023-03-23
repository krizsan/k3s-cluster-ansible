# Ansible Collection - ivankrizsan.k3s_cluster

Usage
-----
From the root of this project:
1. Install the collection:<br/>
   ```ansible-galaxy collection install k3s_cluster --force```
2. Launch a K3S cluster in Multipass VMs as specified in the inventory.ym file in k3s_cluster/roles/k3scluster/tests<br/>
   ```ansible-playbook -i inventory.yml k3s-cluster-playbook.yml```
3. Update kubectl configuration on host as to manage the K3S cluster:<br/>
   ```ansible-playbook -i inventory.yml kubectl-local-install-config.yml```
4. Verify K3S cluster:<br/>
   ```kubectl cluster-info```<br/>
   ```kubectl get nodes```<br/>
