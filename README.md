# ansible-elastic-nginx

Ansible playbook to install an Elasticsearch cluster. By default it installs three ES nodes, nginx load balancer and kibana along with the marvel plugin.

### Version
1.0

### Installation

First you need to create the digitalocean droplets:

```sh
$ export DO_API_TOKEN='your_token'
$ ansible-playbook digitalocean.yml
```
When done you can run the site.yml playbook to configure the cluster to the droplets you have just created. There is no need to configure a hosts file, we are using digitalocean dynamic inventory script.
```sh
$ ansible-playbook site.yml
```
### Todos

 - Split ES nodes to master/data/monitoring.
 - Add option to destroy droplets.


License
----

MIT

