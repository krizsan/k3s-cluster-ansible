K3S Cluster
===========
Creates a K3S cluster running in Multipass virtual machines.

Requirements
------------
Multipass (https://multipass.run/) is required to create and manage the virtual machines the K3S cluster will run in.

Role Variables
--------------
Please refer to the defaults/main.yml file for variables and their default values.

Dependencies
------------
Molecule is required if using Molecule converge and destroy to set up and tear down the K3S cluster.

Example Playbook
----------------
Please refer to the example playbook k3s-cluster-playbook.yml in the project root.

Usage
-----
A K3S cluster can be started using Molecule:<br/>
1. ```cd k3s_cluster/roles/k3scluster```<br/>
2. ```molecule destroy --all```<br/>
3. ```molecule converge```<br/>
4. To delete the K3S cluster and the Multipass virtual machines the nodes of the cluster run in:<br/>
```molecule destroy --all```<br/>

License
-------
Apache 2.0

Author Information
------------------
Ivan Krizsan
https://ivankrizsan.se
