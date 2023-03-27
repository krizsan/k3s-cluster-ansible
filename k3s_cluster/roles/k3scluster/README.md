K3S Cluster
===========
Creates a K3S cluster running in Multiapss virtual machines.

Requirements
------------
Multipass (https://multipass.run/) is required to create and manage the virtual machines the K3S cluster will run in.

Role Variables
--------------

Dependencies
------------
None.

Example Playbook
----------------
Please refer to the example playbook k3s-cluster-playbook.yml in the project root.

Usage
-----
A K3S cluster can be started using Molecule whe, developing the role:<br/>
1. ```cd k3s_cluster/roles/k3scluster```<br/>
2. ```molecule destroy --all```<br/>
3. ```molecule converge```<br/>
4. Finally, to delete the K3S cluster and the Multipass virtual machine it runs in:<br/>
```molecule destroy --all```<br/>

License
-------
Apache 2.0

Author Information
------------------
Ivan Krizsan
https://ivankrizsan.se
