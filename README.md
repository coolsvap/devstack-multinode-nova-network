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

1. Clone devstack from devstack.
```
$git clone https://github.com/openstack-dev/devstack.git
```

2. Clone devstack localrc for devstack controller from devstack-multinode-nova-network

```
$git clone https://github.com/svashu/devstack-multinode-nova-network
```

3. Copy the localrc from devstack controller to devstack

```
$cp devstack-multinode-nova-network/localrc devstack/localrc
```

4. Modify the devstack/localrc for IP and password modifications

5. Add the local.sh file for required modifications default devstack.

```
$cp devstack-multinode-nova-network/local.sh devstack/
```

6. Deploy your Devstack

```
$cd devstack && ./stack.sh
```


Steps for DevStack COMPUTE Node configuration
---------------------------------------------

1. Clone devstack from devstack.

```
$git clone https://github.com/openstack-dev/devstack.git
```

2. Clone devstack localrc for devstack compute from devstack-multinode-nova-network

```
$git clone https://github.com/svashu/devstack-multinode-nova-network
```

3. Copy the localrc from devstack compute to devstack

```
$cp devstack-multinode-nova-network/localrc-compute-node devstack/localrc
```

4. Modify the devstack/localrc for IP and password modifications

5. Deploy your Devstack

```
$cd devstack && ./stack.sh
```
