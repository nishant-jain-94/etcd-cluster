# ETCD Cluster Setup

1. Create a discovery token using the following command 
	`curl https://discovery.etcd.io/new?size=3`
2. Copy the generated token in cl.conf > etcd.discovery
3. Use the Cloud Config transpiler and execute `ct --platform=vagrant-virtualbox < cl.conf > config.ign`
4. Run `vagrant up` to run all the containers
5. Run `vagrant ssh core-01` to ssh into the vm
6. Run `etcdctl cluster-health` to check the overall health status of the etcd cluster 
