devstack-multinode-nova-network
===============================
Multinode Devstack setup with nova network

Prerequisites:
--------------

- DevStack setup requires to have 1 VM/ BM machine with internet connectivity.
- Setup a fresh supported Linux installation. (Ubuntu/Fedora/CentOs)
- Install Git


Steps for DevStack CONTROLLER Node configuration
------------------------------------------------

Clone devstack from devstack.
```
$git clone https://github.com/openstack-dev/devstack.git
```
Clone devstack localrc for devstack controller from devstack-multinode-nova-network
```
$git clone https://github.com/svashu/devstack-multinode-nova-network
```
Copy the localrc from devstack controller to devstack
```
$cp devstack-multinode-nova-network/localrc devstack/localrc
```
Modify the devstack/localrc for IP and password modifications
Add the local.sh file for required modifications default devstack.
```
$cp devstack-multinode-nova-network/local.sh devstack/
```
Deploy your Devstack
```
$cd devstack && ./stack.sh
```


Steps for DevStack COMPUTE Node configuration
---------------------------------------------

Clone devstack from devstack.
```
$git clone https://github.com/openstack-dev/devstack.git
```
Clone devstack localrc for devstack compute from devstack-multinode-nova-network
```
$git clone https://github.com/svashu/devstack-multinode-nova-network
```
Copy the localrc from devstack compute to devstack
```
$cp devstack-multinode-nova-network/localrc-compute-node devstack/localrc
```
Modify the devstack/localrc for IP and password modifications
Deploy your Devstack
```
$cd devstack && ./stack.sh
```
