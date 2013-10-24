# adapa
Adapa is a simple ansible+vagrant setup for playing with the cluster services etcd and serf

## services

### supervisord
[supervisord](http://supervisord.org/) lets you turn simple processes into init-style services
this lets us turn ordinary commands into monitored and manageable daemons
adapa uses supervisord to manage the etcd and serf daemons

### etcd
[etcd](https://github.com/coreos/etcd#etcd) is a distributed key/value store with a simple http interface
You can use etcd as a foundation for shared data across systems

### serf
[serf](http://serfdom.io/) is a decentralized system for service orchestration
nodes participate in a simple message based event system
custom handlers can be registered against the serf agent to handle custom events
this means you can send out events such as 'supervisorctl restart etcd' 

## getting started

If you have vagrant and virtualbox installed:

```
git clone https://github.com/eggsby/adapa
cd adapa
vagrant up
vagrant ssh [oannes|adapa]
```

Then poke around with the etcdctl and serf binaries

You may need to edit ansible/host_vars to match your vms public ips
Have fun!
